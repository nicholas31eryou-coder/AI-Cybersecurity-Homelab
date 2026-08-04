# Virtualization

> **Platform:** Oracle VirtualBox
>
> **Status:** IN DEVELOPMENT

---

# Overview

This document describes the virtual infrastructure that supports the AI Cybersecurity HomeLab.

Virtualization provides isolated systems for authorized attack simulation, Python automation, self-hosted artificial intelligence, and future defensive monitoring.

The environment is intentionally modular so that additional systems and security tooling can be introduced without redesigning the existing infrastructure.

---

# Virtualization Platform

## Oracle VirtualBox

**Status:** VERIFIED

Oracle VirtualBox is the hypervisor used to host the virtual machines that make up the HomeLab.

Using virtual machines allows offensive security activities, defensive monitoring, and AI-assisted analysis to be performed within an isolated environment while protecting the host operating system.

---

# Current Virtual Machines

## Kali Linux Virtual Machine

**Status:** VERIFIED

### Purpose

Authorized attack simulation workstation.

### Responsibilities

- Generate controlled attack activity
- Perform network reconnaissance
- Simulate adversary techniques
- Produce security events for testing
- Support future detection validation

---

## Ubuntu Server Virtual Machine

**Status:** VERIFIED

### Purpose

Central processing, automation, and AI server.

### Responsibilities

- Execute Python automation
- Host the Ollama service
- Process security events
- Generate AI-assisted SOC analysis
- Support future telemetry integration

---

### Verified Resources

| Resource | Value | Status |
|----------|-------|--------|
| vCPUs | 8 | VERIFIED |
| RAM | Pending Verification | UNVERIFIED |

---

### Administration

- SSH remote administration
- Python virtual environment
- Git version control

---

# Current Virtual Topology

```text
┌─────────────────────┐
│   Kali Linux VM     │
│                     │
│ Attack Simulation   │
└──────────┬──────────┘
           │
           │ Security Activity
           ▼
┌─────────────────────┐
│ Ubuntu Server VM    │
│                     │
│ Python Automation   │
│ Ollama              │
│ AI Processing       │
└─────────────────────┘
```

---

# Current Operational Workflow

The current verified implementation begins with a supplied security event.

```text
Security Event
      │
      ▼
Python
      │
      ▼
Ollama API
      │
      ▼
Llama 3 8B Instruct
      │
      ▼
AI SOC Analysis
```

This processing path has been successfully tested and verified.

---

# Networking

The virtual machines operate within an isolated HomeLab environment.

Current network design supports:

- Authorized attack simulation
- AI-assisted analysis
- Future telemetry collection

IP addresses observed during testing are treated as test-event data and are not considered verified infrastructure mappings.

---

# Current Limitations

The following capabilities are not yet part of the verified virtual infrastructure:

- Real telemetry ingestion
- Detection and alert pipeline
- Centralized logging
- Additional defensive monitoring

These remain **IN DEVELOPMENT** or **PLANNED**.

---

# Future Expansion

The virtual infrastructure is designed to support future components, including:

- Centralized logging
- Detection engineering
- Additional defensive virtual machines
- SIEM technologies
- Network monitoring sensors
- Threat intelligence enrichment

Future infrastructure components will be documented after implementation and verification.
