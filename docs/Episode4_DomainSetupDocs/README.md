# Episode 4 – Active Directory Deployment (Windows Server 2019)

This episode walks through the setup and configuration of Active Directory Domain Services (AD DS) in a home lab using Windows Server 2019.

## 🛠️ Lab Overview

- **Host Name:** `DCWin001`
- **OS:** Windows Server 2019
- **Domain:** `slothlab.local`
- **Role Installed:** Active Directory Domain Services (AD DS)
- **IP Address:** Static (e.g., `192.168.1.10`)

## 🔧 Steps Covered

1. Set a static IP address
2. Rename the server to `DCWin001`
3. Install AD DS and promote server to a Domain Controller
4. Configure forward lookup zone (DNS)
5. Create Organizational Units (OUs):
   - `Users`
   - `Groups`
   - `ServiceAccounts`
6. Create sample users:
   - `Aaron T. Sloth`
   - `Britney T. Sloth`
   - `SVC_Wazuh`
7. Create Security Groups:
   - `IT Admins`
   - `HR Users`
   - `Cybersecurity Team`

## 👤 Sample User Details

| Name             | Username       | Group             | OU              |
|------------------|----------------|-------------------|------------------|
| Aaron T. Sloth   | AaronT.Sloth   | Cybersecurity Team| Users           |
| Britney T. Sloth | BritneyT.Sloth | HR Users          | Users           |
| SVC Wazuh        | SVC_Wazuh      | None              | ServiceAccounts |

## 🔒 Security Best Practices

- Enforce password complexity via Group Policy
- Disable built-in local Administrator account after domain join
- Ensure DNS is configured to point to the Domain Controller for all lab VMs

## 📌 Notes

This sets the foundation for upcoming episodes, particularly:
- Episode 5: Wazuh integration
- Episode 6: Sysmon deployment
