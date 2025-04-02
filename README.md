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

▶️ [Budget-Friendly Home Lab Series on YouTube](https://www.youtube.com/@YourChannelLink)

## 📺 Episode Guide

| Episode | Title | Notes |
|--------|-------------------------------|---------------------------|
| Ep 1   | Lab Overview & Roadmap        | Intro to the lab goals    |
| Ep 2   | Deploying pfSense Firewall    | Network perimeter setup   |
| Ep 3   | Installing Windows Server 2019| Lays groundwork for AD    |
| Ep 4   | Active Directory & DNS Setup  | Promoting to Domain Ctrlr |
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

## 📜 License

MIT License — use, modify, and share freely.
