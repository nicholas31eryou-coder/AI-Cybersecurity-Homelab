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
- Process captured data
- Generate structured security alerts
- Interface with the local AI layer

---

## 3. Self-Hosted AI Layer

### Role

Artificial intelligence analysis platform

### Runtime

**Ollama**

### Model

**Llama 3 8B Instruct**

### Responsibilities

- Provide local LLM inference
- Analyze structured security alerts
- Assist with threat classification
- Generate security recomendations
- Support AI-assisted security analysis
- Detect anomalous behaviour
- Assist threat hunting

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
(Ollama + Llama)
            │
            ▼
Detection & Analysis
```

---

# Processing Workflow



The current implementation adapts the processing workflow from the original reference tutorial while replacing the vendor-hosted AI component with local inference.

```text
Kali Linux
     │
     ▼
Network Activity
     │
     ▼
Ubuntu Server
     │
     ▼
Traffic Capture
     │
     ▼
Python Processing
     │
     ▼
Structured Alert JSON
     │
     ▼
Ollama + Llama
     │
     ▼
SOC Analysis
```

Python automation acts as the integration layer between collected security telemetry and the self-hosted AI environment.

The processing workflow is responsible for converting captured activity into structured alert data that can be submitted to the local language model for analysis.
---

# Reference Architecture (Version 1.0)

The current implementation adapts the processing workflow from my original concept while replacing the vendor-hosted AI component with local inference.
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
- Maintain local control of security data
- Reduce recurring operational costs
- Reduce vendor dependency
- Experiment with different language models
- Better understand AI infrastructure

The core security workflow remains closely based on the reference implementation while the AI processing component has been redesigned for local inference.

---

# Future Expansion

The architecture is intentionally designed to support additional capabilities as the homelab develops.

Future expansion may include:

- Centralized logging
- Detection engineering
- Threat intelligence
- Knowledge base / RAG
- Security automation
- Additional defensive monitoring
