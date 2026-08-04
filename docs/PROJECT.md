# AI Cybersecurity HomeLab

> **Status:** 🚧 In Development
>
> **Current Version:** v0.2.0
>
> **Current Phase:** Real Telemetry Integration

---

# Project Overview

The AI Cybersecurity HomeLab is an enterprise-inspired learning environment designed to develop practical experience in offensive security, defensive monitoring, Linux administration, Python automation, self-hosted artificial intelligence, and security engineering.

The project combines virtualized infrastructure, authorized attack simulation, security telemetry, automation, and AI-assisted analysis into a continuously evolving cybersecurity laboratory.

Rather than focusing on a single technology, the objective is to understand how modern Security Operations Centers (SOCs) integrate infrastructure, detection engineering, automation, and artificial intelligence to improve security operations.

The project is developed incrementally, with each milestone being planned, implemented, tested, documented, and committed before moving to the next phase.

---

# Project Objectives

The primary objectives of this HomeLab are to:

- Develop practical cybersecurity skills through hands-on implementation
- Build and administer Linux-based infrastructure
- Design and operate a self-hosted AI-assisted SOC analysis workflow
- Perform authorized attack simulations
- Generate and analyze security telemetry
- Develop Python-based security automation
- Explore detection engineering concepts
- Evaluate locally hosted LLMs for cybersecurity use cases
- Produce professional engineering documentation
- Build a portfolio-quality GitHub repository that demonstrates real implementation work

---

# Current Project Status

## Current Phase

**Real Telemetry Integration**

The local AI analysis pipeline has been successfully implemented and verified.

The next milestone is connecting real HomeLab-generated security telemetry to the existing AI workflow.

---

## Verified

- GitHub repository established
- Modular documentation framework
- Kali Linux attacker virtual machine
- Ubuntu Server virtual machine
- SSH remote administration
- Python virtual environment
- Self-hosted Ollama inference service
- Llama 3 8B Instruct deployment
- Python to Ollama API communication
- AI-assisted SOC analysis generation
- Ubuntu Server optimized for local LLM inference (8 vCPUs)

---

## In Development

- Real security telemetry integration
- Detection and alert processing pipeline
- Python telemetry processing
- End-to-end AI-assisted SOC workflow

---

## Planned

- Centralized logging
- Detection engineering
- Threat hunting
- Structured AI JSON output
- Threat intelligence enrichment
- Additional defensive monitoring
- Automated reporting
- Security knowledge base (RAG)
- Evaluation of AI SOC analysis accuracy

---

# Project Scope

The HomeLab currently focuses on the following technical domains:

- Offensive Security
- Defensive Monitoring
- Self-Hosted Artificial Intelligence
- Linux Administration
- Virtualization
- Python Automation
- Detection Engineering
- Security Telemetry
- Technical Documentation

Future technologies will be introduced only after they have been implemented, tested, and documented.

---

# Current Architecture

The current verified implementation consists of:

1. Kali Linux virtual machine for authorized attack simulation
2. Ubuntu Server virtual machine for Python automation and AI processing
3. Ollama local inference runtime
4. Llama 3 8B Instruct
5. AI-assisted SOC analysis

### Current Verified Workflow

Security Event

↓

Python

↓

Ollama API

↓

Llama 3 8B Instruct

↓

AI SOC Analysis

---

# Current Development Direction

The current implementation begins with a supplied security event.

The next milestone is expanding the workflow into a complete AI-assisted SOC pipeline:

Kali Linux

↓

Authorized Attack Simulation

↓

Security Telemetry

↓

Detection / Alert

↓

Python Automation

↓

Ollama API

↓

AI SOC Analysis

---

# Artificial Intelligence

Unlike the original reference implementation, this project uses a fully self-hosted AI environment.

Current verified AI components include:

- Ollama
- Llama 3 8B Instruct
- Python integration

Future AI development will focus on:

- Structured responses
- Threat intelligence enrichment
- Retrieval-Augmented Generation (RAG)
- AI-assisted investigation
- Model evaluation and prompt optimization

---

# Engineering Philosophy

This project follows an incremental engineering methodology.

Every milestone follows the same process:

1. Plan
2. Implement
3. Test
4. Verify
5. Document
6. Commit
7. Begin the next milestone

Documentation is maintained alongside implementation to preserve architectural decisions, troubleshooting history, research, lessons learned, and evidence for every verified milestone.

Project documentation distinguishes between:

- VERIFIED
- CONFIRMED
- IN DEVELOPMENT
- PLANNED
- ASSUMED
- DEPRECATED

This ensures that future goals are clearly separated from completed engineering work while preserving the historical evolution of the HomeLab.
