# Architecture

## Current Status

Reference Architecture Version 1.0

---

## Purpose

This document describes the logical architecture of the AI Cybersecurity Homelab.

The initial implementation follows the AIRIA reference tutorial while allowing future architectural expansion.

---

## Current Components

### Kali Linux

Role

Attacker workstation

Responsibilities

- Generate attack activity
- Execute security tools
- Produce logs

---

### Ubuntu Server

Role

Central processing server

Responsibilities

- Collect logs
- Execute Python automation
- Preprocess data
- Interface with AIRIA

---

### AIRIA Create

Role

AI workflow design

Responsibilities

- Configure AI processing
- Build workflows
- Prepare deployment

---

### Published AIRIA Agent

Role

AI analysis engine

Responsibilities

- Analyze events
- Detect anomalies
- Generate recommendations

---

# Current Data Flow

Kali Linux

↓

Ubuntu Server

↓

AIRIA Create

↓

Published AIRIA Agent

---

# Architecture Status

Version 1.0

Reference tutorial implementation.

Future versions will evolve beyond this baseline as additional services and infrastructure are introduced.
