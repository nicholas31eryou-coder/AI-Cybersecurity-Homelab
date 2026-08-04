# Research

> This document records technical research performed during the development of the AI Cybersecurity HomeLab.

The purpose of this document is to document research topics, engineering evaluations, and technical decisions that influence the direction of the project.

Research supports implementation but does not replace testing or verification. Features are documented as operational only after successful implementation and validation.

---

# Artificial Intelligence Research

## Objective

Evaluate locally hosted AI technologies suitable for AI-assisted cybersecurity analysis.

---

## AI Platform Evaluation

### Research Question

Should the HomeLab use a cloud-hosted AI platform or a self-hosted large language model?

### Evaluation

Both approaches were considered during the early design of the project.

Cloud-hosted AI platforms provide rapid deployment but introduce considerations such as recurring costs, vendor dependency, and reduced control over infrastructure.

Self-hosted AI environments require additional setup and infrastructure management but provide greater flexibility and complete local control over processing.

### Engineering Decision

The project adopted a self-hosted AI architecture using:

- Ollama
- Llama 3 8B Instruct

This approach provides:

- Local AI inference
- Greater privacy
- Vendor independence
- Practical experience managing AI infrastructure

---

## Future AI Research

Areas planned for future evaluation include:

- Prompt engineering
- Structured JSON output
- Model comparison
- AI response consistency
- Security-specific prompt optimization
- AI performance benchmarking

---

# Detection Engineering Research

## Current Research Topics

Current areas of investigation include:

- Alert normalization
- MITRE ATT&CK mapping
- Detection engineering workflows
- Sigma rule development
- Security event classification

**Status:** IN DEVELOPMENT

---

# Python Automation Research

## Current Research Topics

Research currently focuses on:

- Security event processing
- API integration
- Automation workflows
- Data parsing
- Structured alert generation

**Status:** IN DEVELOPMENT

---

# Infrastructure Research

## Current Research Topics

Infrastructure research includes:

- Virtual machine resource optimization
- Local AI performance
- Virtual network design
- System scalability

**Status:** ONGOING

---

# Future Research

The following research areas are planned for future milestones:

- Centralized logging
- Threat intelligence enrichment
- Retrieval-Augmented Generation (RAG)
- Threat hunting methodologies
- SIEM technologies
- Security orchestration
- Automated reporting
- AI evaluation methodologies

---

# Research Methodology

Research within this project follows an evidence-based engineering process:

1. Research
2. Evaluate
3. Implement
4. Test
5. Verify
6. Document

Only verified implementation results are incorporated into the operational project documentation.
