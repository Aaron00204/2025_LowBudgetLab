# 🧪 Budget-Friendly Home Lab Series

A low-cost, practical cybersecurity lab environment built entirely with free tools, open-source platforms, and evaluation software — designed to help you level up your skills in system administration, network security, SIEM monitoring, vulnerability management, and more.

This project follows my YouTube series, **"Budget-Friendly Home Lab,"** where each episode walks through deploying, configuring, and integrating components of a realistic enterprise lab on a budget.

## 🧩 Core Components

- **Oracle VirtualBox** – Free hypervisor for running all VMs locally
- **pfSense** – Open-source firewall/router for network segmentation
- **Windows Server 2019** – Evaluation version used for AD DS and DNS
- **Ubuntu/Debian** – Lightweight Linux clients
- **Wazuh** – Open-source SIEM for threat detection, auditing, and compliance
- **Windows/Linux Clients** – For endpoint testing, policy application, and log collection

## 🎯 Learning Objectives

- Build a secure, isolated home lab using VirtualBox
- Understand core network services like DHCP, DNS, NAT, and VLANs
- Deploy and manage Windows Server with AD DS
- Perform basic blue-team activities (alerting, logging, monitoring)
- Practice ethical red-team tools in a controlled space
- Integrate open-source tools to simulate enterprise-level SOC workflows

## 🎥 Watch the Full Lab Series

▶️ [Budget-Friendly Home Lab Series on YouTube](https://www.youtube.com/@aaronthesloth3428)

## 📺 Episode Guide

| Episode | Title | Notes |
|--------|-------------------------------|---------------------------|
| Ep 1   | Lab Overview & Roadmap        | Intro to the lab goals    |
| Ep 2   | Deploying pfSense Firewall    | Network perimeter setup   |
| Ep 3   | Installing Windows Server 2019| Lays groundwork for AD    |
| Ep 4   | AD setup, users, groups, & .. | Promoting to Domain Ctrlr |
| Ep 5   | Deploying Wazuh SIEM          | SOC-style monitoring      |
| Ep 6   | Adding Windows/Linux Clients  | Test endpoints            |
| Ep 7   | Wazuh Agent Deployment        | Endpoint telemetry        |
| Ep 8   | Alerting & Dashboards         | Detection in action       |
| ...    | More to come!                 |                           |

## 🚀 Getting Started

To follow along, you’ll need:

- A host machine with at least 16GB RAM
- Oracle VirtualBox (or your preferred hypervisor)
- Internet connection for downloading ISOs and packages

All instructions assume **VirtualBox** as the hypervisor, but the core principles apply to other platforms like VMware or Proxmox.

## 📁 Repo Structure

This repository will be updated with:

- `/docs/` – Lab setup notes, screenshots, diagrams
- `/configs/` – Sample configurations (pfSense, AD DS, Wazuh, etc.)
- `/scripts/` – Any automation or helper scripts

## Diagram
https://github.com/Aaron00204/2025_LowBudgetLab/blob/main/slothlab_diagram.png

##Inventory
## Host Machine
ADLTS001 - Windows 10 - Host Machine running VirtualBox, manages the lab environment
## Internal Network
FWLin001 - Linux (pfSense) - Firewall managing traffic between Internal, External, and Isolated networks - 192.168.10.1
SIEMLin001 - Linux (Wazuh) - SIEM Server collecting logs and analyzing security events - 192.168.10.50
DCWin001 - Windows Server 2019 - Active Directory Domain Controller managing authentication and group policies - 192.168.10.10
CLIWin001 - Windows 10 Pro - Domain-Joined Windows Client for Administration - 192.168.10.100
WRKLin001 - Linux (Ubuntu/Debian) - Domain-Joined Linux Client for User Environment - 192.168.10.101
WRKWin001 - Windows 10/11 - Domain-Joined Windows Client for User Environment - 192.168.10.102
## External Network
ATKKali001 - Linux (Kali) - Offensive Security machine used for penetration testing and vulnerability assessments
## Isolated Network
MALWin001 - Windows 10 - Malware Analysis VM used to analyze malware behavior in an isolated environment
CuckooLin001 - Linux (Ubuntu/Debian) - Cuckoo Sandbox for automated malware analysis
SIEM-Relay - Linux (Ubuntu/Debian) - Isolated Log Aggregation server that collects logs from malware VMs and forwards to SIEMLin001

## 📜 License

MIT License — use, modify, and share freely.
