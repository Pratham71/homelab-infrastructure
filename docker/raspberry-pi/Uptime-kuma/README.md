# 📊 Uptime Kuma – Service Monitoring & Availability

## Overview

Uptime Kuma is deployed on the Raspberry Pi control node to monitor the availability and health of services running across the homelab.

It provides a centralized interface for tracking uptime, detecting failures, and ensuring that critical services remain operational.

---

## 🎯 Purpose

* Monitor uptime of services running on the main server
* Detect service failures and downtime
* Provide a centralized status dashboard
* Improve reliability and observability of the homelab

---

## 🧩 Role in System

Uptime Kuma runs on the **Raspberry Pi (control node)** as part of the monitoring layer.

It continuously checks the availability of:

* Services hosted on the main server
* Internal endpoints and dashboards
* Critical infrastructure components

This separation ensures monitoring remains active even if the main server goes offline.

---

## 🚀 Features

* Real-time uptime monitoring
* Service health checks (HTTP, TCP, etc.)
* Centralized status dashboard
* Lightweight and efficient (ideal for Raspberry Pi)
* Historical uptime tracking

---

## 🌐 Access

* Available on the local network (LAN)
* Accessible remotely via secure access (Tailscale)

---

## 🛠️ Technical Highlights

* Runs independently from the main server for higher reliability
* Uses periodic health checks to track service status
* Maintains persistent data for uptime history
* Designed for always-on monitoring with minimal resource usage

---

🎯 Use Cases

* Monitoring availability of all homelab services
* Detecting downtime or service crashes
* Ensuring critical services remain operational
* Providing a quick overview of system health
