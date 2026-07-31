# Services

## Status

**Current Services:** In Development

This document describes the services that make up the AI Cybersecurity Homelab and their responsibilities.

---

# Offensive Security

## Kali Linux VM

**Status:** ✅ Confirmed

### Role

Primary attacker workstation.

### Responsibilities

- Penetration testing
- Vulnerability assessment
- Attack simulation
- Security tool execution
- Traffic generation
- Adversary emulation

---

# Infrastructure Services

## Ubuntu Server

**Status:** 🚧 In Progress

### Role

Central infrastructure and automation server.

### Responsibilities

- Central log collection
- Python automation
- Data preprocessing
- Security monitoring
- AI integration
- Future service orchestration

---

# Artificial Intelligence

## Self-Hosted LLM

**Status:** 🚧 Planned

### Planned Model

**Llama 3 8B Instruct**

### Role

Local AI analysis platform.

### Responsibilities

- Log analysis
- Threat analysis
- AI-assisted investigations
- Security recommendations
- Natural language querying
- Future Retrieval-Augmented Generation (RAG)

---

# Detection & Analytics

**Status:** 📋 Planned

Future responsibilities include:

- Detection engineering
- Threat correlation
- Anomaly detection
- Security reporting
- AI-assisted investigations

---

# Planned Services

The following services are planned for future implementation as the homelab evolves:

## Logging

- Filebeat
- Logstash

## Search & Analytics

- Elasticsearch
- Kibana

## Network Security

- Suricata
- Zeek

## Detection Engineering

- Sigma Rules
- YARA Rules

---

# Service Roadmap

| Service | Status |
|----------|--------|
| Kali Linux VM | ✅ Confirmed |
| Ubuntu Server | 🚧 In Progress |
| Self-Hosted LLM (Llama 3 8B Instruct) | 📋 Planned |
| Detection & Analytics | 📋 Planned |
| Kibana | 📋 Planned |
| Zeek | 📋 Planned |

---

# Notes

Services will be documented in greater detail as they are deployed and validated.

The architecture is intentionally modular, allowing individual services to be added, replaced, or removed without affecting the overall design.
