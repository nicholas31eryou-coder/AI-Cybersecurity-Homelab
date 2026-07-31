# Architecture

## Status

**Current Architecture:** Version 2.0 (In Development)

**Reference Architecture:** Version 1.0 (Archived Reference)

---

# Purpose

This document describes the logical architecture of the AI Cybersecurity Homelab and how it has evolved throughout the project.

The homelab began by following the AIRIA cybersecurity tutorial as an initial reference implementation. As the project matured, the architecture shifted toward a modular, self-hosted AI platform to provide greater flexibility, privacy, and educational value.

---

# Architecture Philosophy

The homelab follows several engineering principles:

- Modular design
- Self-hosted where practical
- Vendor-independent architecture
- Incremental implementation
- AI-assisted security operations
- Continuous documentation

Each component has a clearly defined responsibility and can be replaced or expanded without redesigning the entire platform.

---

# Current Planned Architecture

## 1. Threat Actor (Kali Linux VM)

### Role

Attacker workstation

### Responsibilities

- Generate attack activity
- Execute offensive security tools
- Produce realistic security telemetry
- Simulate adversary techniques

---

## 2. Ubuntu Server

### Role

Central processing and automation server

### Responsibilities

- Collect system and security logs
- Execute Python automation
- Normalize and preprocess data
- Interface with the local AI layer
- Coordinate supporting services

---

## 3. Self-Hosted AI Layer

### Role

Artificial intelligence analysis platform

### Planned Model

**Llama 3 8B Instruct**

### Responsibilities

- Analyze collected telemetry
- Detect anomalous behaviour
- Assist threat hunting
- Generate recommendations
- Support future Retrieval-Augmented Generation (RAG)

---

## 4. Detection & Analysis

### Role

Security analytics

### Responsibilities

- Threat correlation
- Detection engineering
- AI-assisted investigations
- Security reporting
- Future automation

---

# Current Data Flow

```text
Threat Actor (Kali Linux VM)
            │
            ▼
Ubuntu Server
(Log Collection & Python Automation)
            │
            ▼
Self-Hosted AI Layer
(Llama 3)
            │
            ▼
Detection & Analysis
```

---

# Reference Architecture (Version 1.0)

The original implementation followed the AIRIA cybersecurity tutorial.

Reference data flow:

```text
Kali Linux
        │
        ▼
Ubuntu Server
        │
        ▼
AIRIA Create
        │
        ▼
Published AIRIA Agent
```

This architecture served as the initial learning platform and established the baseline for the homelab. The project has since transitioned toward a self-hosted AI architecture while retaining the reference implementation for historical documentation.

---

# Architecture Evolution

The project transitioned away from the AIRIA workflow to a self-hosted LLM architecture in order to:

- Increase architectural flexibility
- Maintain complete ownership of security data
- Experiment with multiple language models
- Reduce vendor dependency
- Better understand AI infrastructure
- Support future AI research and experimentation

---

# Future Expansion

The architecture has been intentionally designed to accommodate additional services as the homelab evolves.

Planned future integrations include:

- Centralized logging platform
- SIEM capabilities
- Threat intelligence feeds
- Detection engineering tools
- Knowledge base / RAG
- Security automation
- Additional AI models
- Enterprise monitoring

---

# Document Status

**Current Architecture:** Active

**Reference Architecture:** Preserved for historical reference

This document will be updated as major architectural milestones are completed.
