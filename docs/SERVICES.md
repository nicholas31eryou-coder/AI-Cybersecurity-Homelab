# Services

## Purpose

This document describes the primary services and components currently used or being implemented within the AI Cybersecurity Homelab.

---

# Offensive Security

## Kali Linux VM

**Status:** ✅ Deployed

### Role

Primary threat actor workstation.

### Responsibilities

- Execute offensive security tools
- Generate controlled attack activity
- Perform attack simulations
- Generate network traffic and security telemetry
- Support detection testing

---

# Infrastructure

## Ubuntu Server

**Status:** 🚧 In Development

### Role

Central processing and automation server.

### Responsibilities

- Collect security telemetry
- Run Python automation
- Process captured data
- Generate structured security alerts
- Interface with the local AI environment

---

# Artificial Intelligence

## Ollama

**Status:** 🚧 In Development

### Role

Local LLM runtime.

### Responsibilities

- Host and run the selected language model
- Provide local model inference
- Provide an interface for Python automation
- Keep AI processing within the homelab environment

---

## Llama

**Status:** 🚧 In Development

### Role

Language model used for AI-assisted security analysis.

### Responsibilities

- Analyze structured security alerts
- Assist with threat classification
- Assess security events
- Generate security recommendations
- Produce structured SOC analysis

---

# Security Processing

## Python Automation

**Status:** 📋 Planned

### Role

Processing and integration layer between collected security telemetry and the local AI environment.

### Responsibilities

- Process collected security data
- Analyze captured traffic
- Generate structured alert data
- Submit alerts to Ollama
- Receive and store AI-generated analysis

---

# Current Service Flow

```text
Kali Linux VM
      │
      ▼
Ubuntu Server
      │
      ▼
Python Automation
      │
      ▼
Ollama
      │
      ▼
Llama
      │
      ▼
Security Analysis
