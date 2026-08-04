# Python Dependencies

## Purpose

This document records the Python dependencies used by the AI Cybersecurity HomeLab and explains their role within the project.

Dependencies are documented as they become part of the verified implementation. Planned or experimental libraries are not listed until they have been integrated and tested.

---

# Current Dependencies

| Dependency | Purpose | Status |
|------------|---------|--------|
| Python Standard Library (`json`) | Process security event data | VERIFIED |
| Python Standard Library (`urllib`) | HTTP communication with the Ollama API* | VERIFIED |
| Python Virtual Environment (`venv`) | Isolated Python environment | VERIFIED |

> *Update this entry if your implementation uses a different HTTP library (for example, `requests`). Only document what is actually used by the project.

---

# Runtime Environment

The Python application executes on the Ubuntu Server virtual machine within a dedicated Python virtual environment.

Current responsibilities include:

- Processing security event data
- Sending requests to the local Ollama API
- Receiving AI-generated SOC analysis
- Displaying analysis results

---

# Future Dependencies

The following libraries may be introduced as the project expands. They are **not currently part of the verified implementation**.

| Dependency | Planned Purpose | Status |
|------------|-----------------|--------|
| requests | Simplified HTTP communication | PLANNED |
| pandas | Data parsing and analysis | PLANNED |
| pydantic | Structured data validation | PLANNED |
| PyYAML | Configuration management | PLANNED |

---

# Dependency Management

Python dependencies will be managed through a virtual environment.

As additional verified dependencies are introduced, a `requirements.txt` file will be maintained alongside this documentation to support reproducible project setup.
