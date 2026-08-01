# AI Cybersecurity Homelab

> **Status:** 🚧 Initial Implementation

---

# Project Overview

The AI Cybersecurity Homelab is an enterprise-inspired learning environment designed to develop practical experience in offensive security, defensive security, artificial intelligence, and security automation.

The project combines virtual machines, attack simulation, security telemetry, Python automation, and AI-assisted analysis into a continuously evolving cybersecurity laboratory.

Rather than focusing on a single technology, the objective is to understand how modern security operations integrate infrastructure, detection, automation, and artificial intelligence.

---

# Project Objectives

The primary objectives are:

- Develop hands-on cybersecurity skills
- Learn Linux and virtual infrastructure administration
- Build an AI-assisted security analysis workflow
- Perform controlled attack simulations
- Generate and analyze security telemetry
- Implement defensive monitoring
- Explore detection engineering
- Develop security automation using Python
- Gain experience operating a locally hosted LLM
- Produce professional engineering documentation
- Build a portfolio-quality GitHub repository

---

# Current Project Status

## Phase

**Initial Implementation**

## Completed

- GitHub repository created
- Centralized documentation framework established
- Reference architecture documented
- Kali Linux attacker VM deployed
- Project transitioned from the AIRIA reference workflow toward a self-hosted AI architecture

## In Progress

- Ubuntu Server configuration
- Ollama deployment
- Local LLM deployment and testing
- Python security automation preparation
- Adaptation of the reference AI workflow for local inference

## Planned

- Network traffic collection
- Security telemetry processing
- Alert JSON generation
- Ollama API integration
- Llama-based SOC analysis
- AI-assisted anomaly detection
- Attack simulation and validation
- Detection engineering
- Additional defensive security tooling

---

# Project Scope

The current homelab focuses on:

- Offensive Security
- Defensive Security
- AI-Assisted Analysis
- Linux Infrastructure
- Virtualization
- Security Telemetry
- Python Automation
- Detection Engineering
- Technical Documentation

The project is intentionally developed incrementally. Additional technologies and services will be introduced only as the core architecture is implemented and validated.

---

# Current Implementation Direction

The current implementation follows a four-stage architecture:

1. **Threat Actor — Kali Linux VM**
2. **Ubuntu Server — Log Collection and Python Automation**
3. **Self-Hosted AI — Ollama and Llama**
4. **Detection and Analysis**

The Ubuntu Server acts as the central processing system between generated security activity and the local AI layer.

Python automation will be used to process collected telemetry, generate structured alerts, and submit relevant security information to the locally hosted AI model for analysis.

---

# Reference Implementation

The project originally began from an AIRIA AI cybersecurity tutorial.

The tutorial architecture is preserved as:

**Reference Architecture Version 1.0**

It established the original workflow and serves as a learning reference rather than the final architecture of the homelab.

The project has since diverged from the vendor-hosted AI portion of the reference implementation.

---

# Self-Hosted AI Direction

The current architecture replaces the vendor-hosted AI component of the reference implementation with a locally hosted AI environment.

The planned AI stack consists of:

- **Ollama** — Local LLM runtime
- **Llama** — Language model for security analysis
- **Python** — Integration and automation layer

This approach allows security telemetry to remain within the homelab while providing hands-on experience with local AI infrastructure and API integration.

---

# Engineering Philosophy

The project follows an incremental engineering approach.

Each implementation milestone is:

1. Planned
2. Implemented
3. Validated
4. Documented
5. Committed to GitHub

Documentation is maintained alongside implementation to preserve architectural decisions, troubleshooting history, research, and lessons learned throughout the project lifecycle.
