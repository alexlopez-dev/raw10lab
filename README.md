# 🧱 Raw10Lab — Homelab Infrastructure & DevOps Sandbox

![Last Commit](https://img.shields.io/github/last-commit/alexlopez-dev/raw10lab)
![Repo Size](https://img.shields.io/github/repo-size/alexlopez-dev/raw10lab)
![Contributors](https://img.shields.io/github/contributors/alexlopez-dev/raw10lab)
![License](https://img.shields.io/github/license/alexlopez-dev/raw10lab)

> **Purpose:** My personal homelab environment for hands-on DevOps learning and infrastructure automation.  
> Built to simulate real-world cloud deployments using local hardware, virtualization, and Infrastructure-as-Code.

---

## ⚙️ Architecture Overview

**Hardware Stack**
- Dell R730 Server (Dual Xeon E5-2690 v3, 128GB RAM, 1.92TB SSD)
- Quadro T1000 GPU + 10GbE Daughter Card
- Ubiquiti Cloud Gateway Fiber + U7 Pro XG + Flex XG Switch
- ZimaBoard 2-1664 + Jet KVM for remote access
- MacBook Pro M4 (main workstation)

**Virtualization Layer**
- Proxmox VE (hypervisor)
- VLAN segmentation (172.31.100.0/24)
- Virtual machines for Docker, Ansible control node, and monitoring stack

**Network Services**
- UniFi Network for LAN management
- Pi-hole for DNS-level filtering
- Tailscale for remote secure access

---

## 🧰 DevOps Stack

| Category | Tool |
|-----------|------|
| **IaC** | Terraform |
| **Automation** | Ansible |
| **Containerization** | Docker + Docker Compose |
| **CI/CD** | GitHub Actions |
| **Monitoring** | Prometheus + Grafana (planned) |
| **Version Control** | Git + GitHub |
| **Secrets Mgmt** | SOPS (planned) |

---

## 🧩 Project Layout

```bash
raw10lab/
├─ terraform/
│  ├─ main.tf
│  ├─ variables.tf
│  ├─ outputs.tf
│  └─ README.md
├─ ansible/
│  ├─ playbooks/
│  │  ├─ setup.yml
│  │  ├─ harden.yml
│  ├─ inventory/
│  │  └─ hosts.ini
│  └─ roles/
├─ docker/
│  ├─ compose.yml
│  └─ .env.example
├─ diagrams/
│  └─ network-topology.png
└─ README.md  <-- you are here

