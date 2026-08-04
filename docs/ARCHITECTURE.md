# Architecture

> **Current Architecture:** Version 2.0
>
> **Status:** IN DEVELOPMENT
>
> **Current Milestone:** v0.2.0 – Local AI SOC Analysis Operational

---

# Overview

This document describes the logical architecture of the AI Cybersecurity HomeLab and the relationships between its major components.

The HomeLab is designed as a modular cybersecurity environment that combines offensive security, defensive monitoring, Python automation, and self-hosted artificial intelligence. Each component has a clearly defined responsibility, allowing the platform to expand incrementally as additional capabilities are implemented and verified.

---

# Architecture Principles

The HomeLab follows several core engineering principles:

- Modular architecture
- Self-hosted where practical
- Incremental implementation
- Evidence-based documentation
- Separation of verified and planned capabilities
- Professional engineering documentation

Each milestone is implemented, tested, verified, documented, and committed before additional functionality is introduced.

---

# Current Architecture

The current verified implementation consists of five primary components.

## 1. Kali Linux Virtual Machine

### Role

Authorized attack simulation workstation.

### Responsibilities

- Generate controlled attack activity
- Perform network reconnaissance
- Simulate adversary techniques
- Produce security events for testing

---

## 2. Ubuntu Server Virtual Machine

### Role

Central processing and automation server.

### Responsibilities

- Execute Python automation
- Host the Ollama service
- Process security events
- Coordinate AI-assisted analysis
- Support future telemetry processing

---

## 3. Python Automation Layer

### Role

Integration layer between security data and artificial intelligence.

### Responsibilities

- Process security events
- Communicate with the Ollama API
- Submit requests for AI analysis
- Receive and present AI-generated results

---

## 4. Ollama

### Role

Local large language model (LLM) inference runtime.

### Responsibilities

- Host local language models
- Process requests from Python
- Return AI-generated SOC analysis

---

## 5. Llama 3 8B Instruct

### Role

Local language model responsible for cybersecurity analysis.

### Responsibilities

- Analyze supplied security events
- Assess severity
- Generate findings
- Recommend response actions

---

# Current Verified Workflow

The following processing path has been successfully tested and verified.

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

This workflow represents the current v0.2.0 milestone.

---

# Component Relationships

```text
Kali Linux VM
        │
        │ (Generates Security Activity)
        ▼
Ubuntu Server
        │
        ├── Python Automation
        │
        ▼
Ollama
        │
        ▼
Llama 3 8B Instruct
        │
        ▼
AI SOC Analysis
```

At the current stage of development, the AI workflow begins with a supplied security event. Integration with live HomeLab telemetry is the next planned milestone.

---

# Current Limitations

The following capabilities are not yet part of the verified implementation:

- Real security telemetry ingestion
- Detection and alert pipeline
- Centralized logging
- Threat intelligence enrichment
- Automated reporting
- AI-assisted threat hunting

These capabilities remain **IN DEVELOPMENT** or **PLANNED** and are intentionally documented separately from the verified architecture.

---

# Target Architecture

The long-term objective is an end-to-end AI-assisted SOC workflow.

```text
Kali Linux
      │
      ▼
Authorized Attack Simulation
      │
      ▼
Security Telemetry
      │
      ▼
Detection / Alert
      │
      ▼
Python Automation
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

The transition from manually supplied security events to real telemetry integration is the current architectural focus.

---

# Architectural Decisions

Key engineering decisions include:

- Self-hosted AI instead of cloud-hosted AI services
- Python as the primary automation language
- Ubuntu Server as the central processing platform
- Modular documentation structure
- Incremental, evidence-based development
- Preservation of verified milestones and historical engineering decisions

---

# Future Expansion

The architecture is designed to support future integration of additional defensive and analytical capabilities, including:

- Centralized logging
- Detection engineering
- Threat intelligence enrichment
- Retrieval-Augmented Generation (RAG)
- Additional defensive monitoring
- Automated reporting
- AI-assisted incident investigation

Future components will be documented only after implementation and verification.
