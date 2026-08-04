# Services

> **Status:** IN DEVELOPMENT

---

# Overview

This document describes the primary services currently implemented within the AI Cybersecurity HomeLab and the role each service performs within the overall architecture.

The HomeLab follows a modular design where each service has a clearly defined responsibility. New services are introduced only after they have been implemented, tested, and verified.

---

# Current Services

## Kali Linux

**Status:** VERIFIED

### Purpose

Authorized attack simulation platform.

### Responsibilities

- Perform network reconnaissance
- Generate controlled attack activity
- Produce security events for testing
- Support detection validation

### Dependencies

- Oracle VirtualBox

---

## Ubuntu Server

**Status:** VERIFIED

### Purpose

Central processing and automation server.

### Responsibilities

- Execute Python automation
- Host the Ollama service
- Process security events
- Coordinate AI-assisted SOC analysis
- Support future telemetry processing

### Dependencies

- Oracle VirtualBox
- OpenSSH Server
- Python
- Ollama

---

## OpenSSH

**Status:** VERIFIED

### Purpose

Provides secure remote administration of the Ubuntu Server.

### Responsibilities

- Remote server administration
- Command-line access
- System maintenance

### Dependencies

- Ubuntu Server

---

## Python Automation

**Status:** VERIFIED

### Purpose

Acts as the automation and integration layer between security events and the local AI environment.

### Responsibilities

- Process supplied security events
- Communicate with the Ollama API
- Receive AI-generated analysis
- Present AI SOC analysis

### Dependencies

- Ubuntu Server
- Ollama
- Python Virtual Environment

---

## Ollama

**Status:** VERIFIED

### Purpose

Provides local large language model (LLM) inference.

### Responsibilities

- Host local language models
- Receive requests from Python
- Return AI-generated SOC analysis

### Dependencies

- Ubuntu Server
- Llama 3 8B Instruct

---

## Llama 3 8B Instruct

**Status:** VERIFIED

### Purpose

Provides AI-assisted cybersecurity analysis.

### Responsibilities

- Analyze supplied security events
- Assess event severity
- Generate security findings
- Recommend response actions

### Dependencies

- Ollama

---

# Current Verified Service Flow

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

---

# Services In Development

The following services are currently being developed and are **not yet part of the verified implementation**.

- Real security telemetry ingestion
- Detection and alert pipeline
- Centralized logging
- Threat intelligence enrichment
- AI-assisted threat hunting
- Automated reporting

These services will be documented after implementation and verification.

---

# Next Milestone

The next service integration milestone is connecting real HomeLab-generated security telemetry to the existing verified AI analysis pipeline.

Target processing flow:

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
AI SOC Analysis
```
