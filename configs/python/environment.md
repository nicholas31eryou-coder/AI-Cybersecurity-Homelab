# Python Environment

## Purpose

The Python environment provides the automation layer for the AI Cybersecurity HomeLab. It is responsible for processing security events, communicating with the local Ollama API, and orchestrating AI-assisted SOC analysis.

---

## Environment

- Python 3
- Python virtual environment (venv)

**Status:** VERIFIED

---

## Current Capabilities

The current Python environment supports:

- Python virtual environment
- Communication with the local Ollama API
- AI-assisted SOC analysis generation
- Local execution on the Ubuntu Server VM

---

## Current Workflow

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

## Verified Components

- Python virtual environment
- Python → Ollama API communication
- AI SOC analysis generation
- `src/ollama_client.py` established as the known-good integration baseline

---

## Current Development Phase

**IN DEVELOPMENT**

The current implementation begins with a supplied security event. The next milestone is integrating real HomeLab-generated security telemetry into the existing Python processing workflow.

Target pipeline:

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

## Notes

- The Python environment executes on the Ubuntu Server VM.
- `src/ollama_client.py` is treated as the current known-good baseline and should not be modified unnecessarily while future integrations are developed.
- Future enhancements will be documented as additional capabilities are implemented and verified.
