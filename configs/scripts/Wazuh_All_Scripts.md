# Wazuh SIEM Home Lab – All Scripts & Commands Used

## 1. Ubuntu Prep & System Updates
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl unzip gnupg2 lsb-release wget -y
```

## 2. Checking Services
```bash
systemctl status wazuh-manager
systemctl status wazuh-indexer
systemctl status wazuh-dashboard
```

## 3. Log Inspection & Disk Troubleshooting
```bash
sudo du -ahx / | sort -rh | head -20
sudo df -h
sudo journalctl -xe
sudo tail -f /var/log/syslog
```

## 4. Clearing Wazuh Queues & Logs
```bash
sudo rm -rf /var/ossec/queue/*
sudo rm -f /var/log/syslog
sudo rm -f /var/log/auth.log
sudo logrotate -f /etc/logrotate.d/wazuh
```

## 5. AppArmor Adjustments
```bash
sudo aa-status
sudo aa-complain /usr/sbin/rsyslogd
sudo aa-enforce /usr/sbin/rsyslogd
```

## 6. Reset & Purge Wazuh Components
```bash
sudo apt remove --purge wazuh-manager wazuh-indexer wazuh-dashboard -y
sudo rm -rf /var/ossec
sudo rm -rf /etc/wazuh*
```

## 7. Wazuh Quick Install Script
```bash
curl -sO https://packages.wazuh.com/4.8/wazuh-install.sh
sudo bash wazuh-install.sh -a
```

## 8. Manually Starting Services
```bash
sudo systemctl start wazuh-manager
sudo systemctl restart wazuh-indexer
sudo systemctl restart wazuh-dashboard
```

## 9. Test Syslog Injection From pfSense/Linux
```bash
logger "TEST-MESSAGE-FW"
```

## 10. Filebeat Template Checks
```bash
curl -XGET "https://127.0.0.1:9200/wazuh-alerts-*/_mapping" -k -u admin:admin
```

## 11. Restarting Filebeat (if using standalone deployment)
```bash
sudo systemctl restart filebeat
```

## 12. Local Wazuh Rule Testing
```bash
/var/ossec/bin/ossec-logtest
```

## 13. SSH Configuration for Windows→Linux File Pull
### Install OpenSSH Server
```bash
sudo apt install openssh-server -y
sudo systemctl enable ssh
sudo systemctl start ssh
```

### PowerShell to Pull Linux File
```powershell
scp wazuh@10.x.x.x:/var/ossec/etc/ossec.conf C:\Users\Aaron\Desktop\ossec.conf
```

## 14. XML Validation
```bash
xmllint --noout /var/ossec/etc/ossec.conf
xmllint --noout /var/ossec/etc/rules/local_rules.xml
```

## 15. Useful Directories
```
/var/ossec/logs/ossec.log
/var/ossec/etc/ossec.conf
/var/ossec/etc/rules/local_rules.xml
/var/ossec/queue/
```

## 16. Wazuh Dashboard Index Searches (Dev Tools)
```json
GET /wazuh-alerts-*/_search
{
  "query": {
    "match_all": {}
  }
}
```

## 17. Visualization Field Examples
```
rule.id
rule.level
agent.name
srcip
location
data.action
```

## 18. Custom Local Rules Template (clean)
```xml
<group name="local">
  <rule id="100001" level="5">
    <if_sid>5716</if_sid>
    <srcip>1.1.1.1</srcip>
    <description>Example SSH Alert</description>
  </rule>
</group>
```

## 19. Common Fixes
### Remove corrupted registry (agents)
```bash
sudo rm -f /var/ossec/queue/db/wdb
sudo systemctl restart wazuh-manager
```

### Recreate log directories after accidental deletion
```bash
sudo mkdir -p /var/log
sudo touch /var/log/syslog /var/log/auth.log
sudo chmod 640 /var/log/*.log
sudo chown syslog:adm /var/log/*.log
```

---

This file contains every major script and command used during the Wazuh SIEM troubleshooting and deployment process.
