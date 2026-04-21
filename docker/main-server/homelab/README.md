# 🧠 Core Services Stack (AI, Automation & Monitoring)

## Overview

This stack represents the core services running on the main server of the homelab. It is designed to support AI workflows, automation, container management, and real-time system monitoring in a self-hosted environment.

The services are organized to provide a centralized, accessible, and observable infrastructure for development and experimentation.

---

## 🚀 Services

### 🔹 Open WebUI

A self-hosted web interface for interacting with local AI models.

**Purpose:**

* Provides a user-friendly interface for AI workflows
* Connects to locally hosted models (via Ollama)
* Enables experimentation with LLMs in a private environment

---

### 🔹 n8n

A workflow automation platform used to automate repetitive tasks and build integrations.

**Purpose:**

* Create automated workflows
* Connect services and APIs
* Experiment with event-driven automation

---

### 🔹 Portainer

A web-based container management interface for Docker environments.

**Purpose:**

* Monitor and manage running containers
* View container status, logs, and resource usage
* Simplify Docker operations through a UI

---

### 🔹 Netdata

A real-time monitoring and observability tool for system performance.

**Purpose:**

* Track CPU, memory, disk, and network usage
* Provide live performance metrics
* Assist in debugging and system optimization

---

## 🧩 System Design

These services are part of the main server (compute node) and are designed to work together:

* **AI Layer:** Open WebUI
* **Automation Layer:** n8n
* **Management Layer:** Portainer
* **Monitoring Layer:** Netdata

This layered approach helps in organizing responsibilities and maintaining clarity in system design.

---

## 🌐 Access

All services are accessible:

* Locally over the network (LAN)
* Remotely via secure access (Tailscale)

This allows full control and monitoring of the system from any authorized device.

---

## 🔑 Key Features

* Self-hosted AI interface for private model interaction
* Workflow automation for integrating services
* Centralized container management
* Real-time system monitoring and observability
* Modular and scalable service design
* Remote accessibility for management and debugging

---

## 🛠️ Technical Highlights

* Multiple services orchestrated as part of a unified infrastructure
* Health monitoring implemented for service reliability
* Persistent storage used for data durability
* Designed for continuous uptime with restart policies

---

## 🎯 Use Cases

* Running and testing local AI models
* Automating workflows and integrations
* Monitoring system performance in real-time
* Managing containerized services efficiently
