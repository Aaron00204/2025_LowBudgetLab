# 📘 Episode 2: Deploying pfSense Firewall

## 🎯 Objective
Set up pfSense as the core firewall in your home lab to control traffic between internal, external, and isolated networks using Oracle VirtualBox.

---

## 🔧 Tools Used
- **pfSense ISO**: https://www.pfsense.org/download/
- **Oracle VirtualBox**: https://www.virtualbox.org/

---

## 🛠️ VM Configuration (FWLin001)
| Setting         | Value                      |
|----------------|----------------------------|
| Name           | FWLin001                   |
| OS Type        | BSD                        |
| Version        | FreeBSD (64-bit)           |
| RAM            | 1024 MB                    |
| CPU            | 1                          |
| Disk Size      | 16 GB                      |
| NIC 1 (WAN)    | NAT or Bridged             |
| NIC 2 (LAN)    | Internal Network: LabNet   |

---

## ⚙️ pfSense Installation
1. Download and mount the pfSense ISO in VirtualBox.
2. Boot the VM and follow the installation wizard.
3. Select **Auto (UFS)** for disk formatting.
4. Reboot and detach the ISO.

---

## 🌐 Interface Setup
| Interface | Adapter | Purpose             |
|-----------|---------|---------------------|
| WAN       | em0     | Connects to internet|
| LAN       | em1     | Connects to LabNet  |

- Set LAN IP to: `192.168.10.1/24`
- Skip DHCP for now

---

## ✅ Outcome
You now have a functional pfSense firewall routing traffic between your internal lab network and the internet.

> **Next Step:** Spin up Windows Server 2019 in VirtualBox (Episode 3).
