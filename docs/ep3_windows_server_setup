# 📘 Episode 3: Deploying Windows Server 2019

## 🎯 Objective
Install and configure Windows Server 2019 as the foundation for your Active Directory Domain Services (AD DS) environment.

---

## 🔧 Tools Used
- **Windows Server 2019 Evaluation ISO**: https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019
- **Oracle VirtualBox**

---

## 🛠️ VM Configuration (DCWin001)
| Setting         | Value                     |
|----------------|---------------------------|
| Name           | DCWin001                  |
| OS Type        | Microsoft Windows         |
| Version        | Windows 2019 (64-bit)     |
| RAM            | 8 GB                      |
| CPU            | 2                         |
| Disk Size      | 100 GB (Dynamic)          |
| NIC            | Internal Network: LabNet  |

---

## 🌐 Static IP Configuration
- IP: `192.168.10.10`
- Subnet: `255.255.255.0`
- Gateway: `192.168.10.1` (pfSense)
- Primary DNS: '127.0.0.1'
- Secondary DNS: `8.8.8.8`

---

## ⚙️ Installation Steps
1. Create the VM in VirtualBox with the config above.
2. Mount the Windows Server 2019 ISO and start the install.
3. Choose **Standard Edition (Desktop Experience)**.
4. Complete installation and set a strong administrator password.

---

## 🔄 Initial Setup After Install
- Rename the server to `DCWin001`
- Set the static IP and DNS settings
- Install updates (optional but recommended)

---

## 📊 Why Windows Server over Samba AD?
| Feature              | Samba AD              | Windows Server 2019        |
|---------------------|-----------------------|-----------------------------|
| AD DS Support        | Basic emulation       | Full native support         |
| Group Policy (GPO)   | Limited               | Full GPO capabilities       |
| GUI Tools            | None (CLI only)       | Server Manager, MMC, etc.   |
| Enterprise Realism   | Partial               | Full enterprise match       |

> Samba is a great learning tool — but Windows Server gives you hands-on experience with enterprise-grade AD environments.

---

## ✅ Outcome
You now have a clean installation of Windows Server 2019 configured and ready to be promoted to a Domain Controller in **Episode 4**.

---
