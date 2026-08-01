# Virtualization

## Purpose

This document describes the virtualization environment used to host the AI Cybersecurity Homelab.

The virtual infrastructure provides isolated systems for offensive security testing, security telemetry generation, centralized processing, automation, and AI-assisted analysis.

---

# Virtualization Platform

## Oracle VirtualBox

**Status:** ✅ Active

Oracle VirtualBox is the current hypervisor used to host the virtual machines that make up the homelab.

VirtualBox provides an isolated environment where attack activity and defensive monitoring can be performed without directly affecting the host system or external networks.

---

# Current Virtual Machines

## 1. Kali Linux VM

**Status:** ✅ Deployed

### Role

Threat actor / attacker workstation.

### Purpose

The Kali Linux virtual machine is used to generate controlled attack activity against systems within the homelab.

### Responsibilities

- Execute offensive security tools
- Generate network activity
- Perform controlled attack simulations
- Produce security telemetry for analysis
- Support future detection testing

---

## 2. Ubuntu Server VM

**Status:** 🚧 In Development

### Role

Central processing and automation server.

### Purpose

The Ubuntu Server acts as the primary defensive infrastructure system within the current architecture.

### Responsibilities

- Collect security telemetry
- Run Python automation
- Process captured data
- Generate structured security alerts
- Host or interface with local AI services
- Support AI-assisted analysis

---

# Current Virtual Topology

```text
┌─────────────────────┐
│   Kali Linux VM     │
│                     │
│   Threat Actor      │
└──────────┬──────────┘
           │
           │ Security / Network Activity
           ▼
┌─────────────────────┐
│   Ubuntu Server VM  │
│                     │
│ Collection          │
│ Processing          │
│ Automation          │
└─────────────────────┘
