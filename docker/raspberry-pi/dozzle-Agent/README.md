# 📡 Dozzle Agent – Remote Log Streaming Node

## Overview

Dozzle Agent is deployed on the Raspberry Pi control node to expose Docker container logs from the device to a central Dozzle instance running on the main server.

It enables real-time log streaming across nodes, allowing centralized visibility into containers running on multiple machines.

---

## 🎯 Purpose

* Enable remote log access from the Raspberry Pi
* Integrate with the main Dozzle instance for centralized logging
* Provide lightweight log streaming without full monitoring overhead

---

## 🧩 Role in System

The Dozzle Agent runs on the **Raspberry Pi (control node)** and acts as a bridge between:

* Local Docker containers on the Pi
* The main Dozzle UI running on the primary server

This allows logs from multiple nodes to be viewed in a single interface.

---

## 🚀 Features

* Real-time Docker log streaming
* Lightweight agent-based architecture
* Centralized log access across multiple nodes
* Minimal resource usage (suitable for Raspberry Pi)

---

## 🌐 Connectivity

* Exposes a log streaming endpoint on the Raspberry Pi
* Accessible from the main server via secure networking (Tailscale)
* Integrated into the main Dozzle UI for unified log viewing

---

## 🛠️ Technical Highlights

* Uses Docker socket (read-only) for log access
* Designed for distributed log visibility across nodes
* Works alongside a central Dozzle instance
* Enables cross-node observability without heavy logging stacks

---

## 📸 Screenshots

* Raspberry Pi container

  ![1776796039009](image/README/1776796039009.png)

---

## 🎯 Use Cases

* Viewing logs from multiple machines in one place
* Debugging distributed services
* Monitoring auxiliary nodes (Raspberry Pi)
* Simplifying log access without SSH
