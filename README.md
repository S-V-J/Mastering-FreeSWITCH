# Mastering FreeSWITCH

[![GitHub](https://img.shields.io/badge/GitHub-S--V--J%2FMastering--FreeSWITCH-blue)](https://github.com/S-V-J/Mastering-FreeSWITCH)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04.3_LTS-orange)](https://ubuntu.com/)
[![FreeSWITCH](https://img.shields.io/badge/FreeSWITCH-Latest-green)](https://freeswitch.org/)
[![FusionPBX](https://img.shields.io/badge/FusionPBX-v4.5%2B-brightgreen)](https://www.fusionpbx.com/)

> **Goal**: Transform from zero (beginner) to hero (job-ready FreeSWITCH developer) through a structured, hands-on learning plan.  
> This repository documents the entire journey—lab setup, skill-building phases, code, configurations, and progress updates.  
> All files, scripts, and programs created during learning will be hosted here for version control and collaboration.

---

## 🎯 Project Overview: Zero to Hero Journey

This repo is a complete guide to mastering **FreeSWITCH** on **Ubuntu 24.04**.  
We build from basic system verification to an enterprise-grade VoIP platform capable of:

* 1 000-1 500 concurrent calls
* WebRTC integration
* Docker/Kubernetes orchestration
* Azure/WireGuard/Cloudflare cloud deployment

### Why This Project?

* **From Zero** – starts with hardware checks and basic installs.  
* **To Hero** – ends with job-ready skills (SIP/RTP, scaling, APIs, DevOps) and a showcase project.  
* **Hands-On** – every step includes commands, code snippets, and tests.  
* **Progress Tracking** – this README is updated with *What to Do* and *What Was Done*.  
* **GitHub Integrated** – commit each milestone for transparent learning history.

### Key Technologies

* Core: **FreeSWITCH**, **FusionPBX**, SIP/RTP/RTCP
* Advanced: WebRTC, Python ESL, Lua dialplans, load testing
* DevOps: Docker, Kubernetes, Terraform, Prometheus/Grafana
* Cloud: Azure VPS, WireGuard VPN, Cloudflare Tunnels
* Tooling: Wireshark, SIPp, Git

### Minimum System Requirements (met)

* RAM ≥ 512 MB (**7.7 GiB**)  
* Storage ≥ 50 MB (**914 GB**)  
* CPU: 64-bit, 2+ cores (Intel i3-5005U, 2 cores/4 threads)  
* OS: Ubuntu 24.04.3 LTS 64-bit  
* Network: Stable internet (ping verified)

---

## 📋 Phases: Zero → Hero Roadmap

| Phase | Topics & Milestones | Status |
|-------|--------------------|--------|
| **0 — System Verification & Prep** | Hardware checks, LVM resize, swap boost, updates, firewall | **✅ Completed (12 Sep 2025)** |
| **1 — FreeSWITCH & FusionPBX Install** | Package repos, install scripts, first test call | ⏳ |
| **2 — Core VoIP Skills** | SIP/RTP theory, dialplans, conferences, 100-call load test | ⏳ |
| **3 — Advanced Development** | WebRTC, Python ESL, RTP proxy, 1 500-call scaling | ⏳ |
| **4 — Containerization & K8s** | Docker images, minikube, CI/CD pipelines | ⏳ |
| **5 — Cloud Deployment & Security** | Azure VPS, WireGuard, Cloudflare Tunnel, monitoring | ⏳ |
| **6 — Portfolio & Job Readiness** | Full platform demo, docs, resume integration | ⏳ |

### Phase 0 — *What Was Done*

* Verified RAM with `free -h`
* Verified initial 98 GB root LV; extended to **928 GB** 
 
  **via**:
- sudo lvextend -l +100%FREE /dev/ubuntu-vg/ubuntu-lv
- sudo resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv
* Swap increased from 4 GB ➜ **8 GB** using a `/swapfile`
* System updated & autoremove; kernel 6.14 confirmed
* Firewall (UFW) enabled for SSH
* Outcome: **System ready for lab setup**

---

## 🚀 Getting Started

### 1. Clone the repo
- git clone https://github.com/S-V-J/Mastering-FreeSWITCH.git
- ~/Mastering-FreeSWITCH
- cd ~/Mastering-FreeSWITCH

### 2. After each step
- git add .
- git commit -m "Describe progress"
- git push

**Note**: Use VirtualBox or Docker for isolated experiments before touching production configs.

---

## 📈 Progress Summary

* **Current Phase**: 0 (completed)
* **Next**: Phase 1 – FreeSWITCH & FusionPBX installation
* **Completion**: 10 %
* **Key Win**: Storage extended 100 GB ➜ 914 GB; swap now 8 GB

---

## 🤝 Collaboration & Support

| Contact | Link |
|---------|------|
| Email | [stjl093@gmail.com](mailto:stjl093@gmail.com) |
| Phone | +91 809 587 5948 |
| LinkedIn | [linkedin.com/in/sid-093](https://linkedin.com/in/sid-093) |
| Donate | [PayPal](https://www.paypal.com/ncp/payment/2J5NTJBYW2HL8) |

Issues and pull requests are welcome—let’s build this together!

---

*Last updated: **12 Sep 2025***  
*License: **MIT** – free to use but no modify.*
