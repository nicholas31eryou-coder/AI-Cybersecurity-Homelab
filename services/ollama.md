# Ollama Service

## Overview

Ollama provides local large language model (LLM) inference for the AI Cybersecurity HomeLab.

It enables Python applications to communicate with locally hosted AI models without relying on cloud-based services.

---

## Purpose

The Ollama service is responsible for:

- Hosting local language models
- Receiving requests from Python
- Returning AI-generated SOC analysis
- Supporting AI-assisted cybersecurity workflows

---

## Current Status

VERIFIED

---

## Current Capabilities

- Local model inference
- Python API communication
- AI SOC analysis generation

---

## Current Workflow

Security Event
↓
Python
↓
Ollama
↓
Llama 3 8B Instruct
↓
AI SOC Analysis

---

## Dependencies

- Ubuntu Server
- Python
- Llama 3 8B Instruct

---

## Future Development

Planned improvements include:

- Structured JSON responses
- Multiple model support
- Prompt optimization
- Performance evaluation
