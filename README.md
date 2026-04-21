# 🖥️ Self-Hosted Homelab Infrastructure

## Overview

Built and managed a two-node self-hosted homelab to run containerized services for AI experimentation, automation, monitoring, and system management.

The setup consists of a high-performance Debian-based main server for workloads and a Raspberry Pi acting as an always-on control node for monitoring and remote power management.

---

## 🧠 System Architecture

### 🔹 Main Server (Compute Node)

* OS: Debian
* Role: Primary compute and service host
* Containerization: Docker + Docker Compose
* Responsibilities:

  * Running core services (AI, dashboards, automation, monitoring)
  * Managing containerized workloads

### 🔹 Raspberry Pi (Control Node)

* Model: Raspberry Pi 4 (4GB RAM)
* Role: Always-on control and monitoring node
* Responsibilities:

  * Uptime monitoring (Uptime Kuma)
  * Remote log access (Dozzle agent)
  * Wake-on-LAN for remote power control and recovery workflows

---

## ⚙️ Hardware Configuration

### 🖥️ Main Server

* CPU: AMD Ryzen 7 3700X (8-core, 16-thread)
* RAM: 32GB DDR4 (3200 MHz)
* Storage:

  * 500GB NVMe (boot drive)
  * 1TB NVMe (high-speed storage)
  * 2 × 1TB SATA SSD (data / containers)
* GPU: NVIDIA RTX 2070 Super (used for AI workloads via Ollama)
* OS: Debian

### 🍓 Raspberry Pi

* Model: Raspberry Pi 4 (4GB RAM)
* Role: Always-on auxiliary node for control and monitoring

---

## 🐳 Services Deployed

### 🖥️ Main Server

* **Open WebUI** – Self-hosted interface for local AI (Ollama integration)
* **n8n** – Workflow automation engine
* **Portainer** – Container management UI
* **Netdata** – Real-time system and performance monitoring
* **Homepage** – Centralized service dashboard
* **Dozzle** – Real-time Docker log viewer
* **Watchtower** – Automated container updates

### 🍓 Raspberry Pi

* **Uptime Kuma** – Service uptime monitoring and alerting
* **Dozzle Agent** – Remote log streaming for containers

---

## 🚀 Key Features

* Two-node architecture separating compute and control responsibilities
* Fully containerized infrastructure using Docker Compose
* Real-time monitoring and observability (Netdata, Uptime Kuma)
* Remote power management using Raspberry Pi + Wake-on-LAN
* Secure remote access for administration
* Centralized dashboards for service visibility
* Automated container updates using Watchtower
* Terminal multiplexing workflows using tmux

---

## 🛠️ Technical Highlights

* Managed multiple containerized services across distributed nodes
* Configured health checks for critical services
* Integrated Docker socket for container visibility and management
* Designed for reliability with restart policies and monitoring
* Organized services into logical stacks (AI, automation, monitoring, dashboards)

---

## 🔌 Architecture Diagram
```text
Client (Laptop / Phone)
        │
 Secure Remote Access
        │
 Raspberry Pi (Control Node)
 ├── Uptime Kuma
 ├── Dozzle Agent
 └── Wake-on-LAN
        │
        ▼
 Debian Main Server
 ├── Open WebUI (AI)
 ├── n8n (Automation)
 ├── Portainer (Management)
 ├── Netdata (Monitoring)
 ├── Homepage (Dashboard)
 ├── Dozzle (Logs)
 └── Watchtower (Updates)
```

---

## 📸 Screenshots

* Portainer dashboard
* Netdata monitoring
* Homepage dashboard
* Uptime Kuma status page
* Dozzle logs
* tmux session

---

## 📁 Repository Structure

```text
.
├── docker/
│   ├── main-server/
│   └── raspberry-pi/
├── docs/
│   └── architecture.png
├── screenshots/
└── README.md
```

---

## 🎯 Why I Built This

This project started as a self-initiated effort to explore self-hosting and real-world infrastructure management. It evolved into a practical environment for running production-like services, experimenting with automation, and managing distributed systems.

---

## 🔮 Future Improvements

* Reverse proxy with domain-based routing (NGINX / Traefik)
* Automated backups for persistent volumes
* Centralized metrics stack (Prometheus + Grafana)
* Network segmentation and service isolation
* Secrets management for environment variables

