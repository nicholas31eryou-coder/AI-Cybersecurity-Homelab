# Troubleshooting

This document records issues encountered during the design, deployment, and operation of the AI Cybersecurity Homelab.

Each entry includes the symptoms, root cause, resolution, and any preventative actions.

---

# 2026-07-31

## Issue 1 — VirtualBox Guest Operating System Detection

### Status

✅ Resolved

### Component

VirtualBox

### Symptoms

VirtualBox did not automatically identify the Kali Linux ISO as a Kali Linux operating system and instead suggested Ubuntu.

### Root Cause

VirtualBox does not always correctly detect Kali Linux installation media.

### Resolution

Configured the virtual machine using the closest supported Linux profile and manually completed the remaining virtual machine configuration.

### Preventative Action

Always verify the guest operating system settings instead of relying solely on automatic detection.

---

## Issue 2 — GitHub Documentation Structure

### Status

✅ Resolved

### Component

Repository Documentation

### Symptoms

Project documentation was initially maintained within a single `MASTER_DOCUMENTATION.md` file.

As documentation expanded, the file became increasingly difficult to maintain and navigate.

### Root Cause

The original documentation structure was not designed to scale with the size of the project.

### Resolution

Reorganized documentation into a centralized `docs/` directory containing individual documents for each major engineering topic.

### Preventative Action

Separate documentation by subject area early in the project to improve maintainability.

---

## Issue 3 — AI Platform Selection

### Status

✅ Resolved

### Component

Architecture

### Symptoms

The original reference architecture relied on a vendor-hosted AI workflow.

### Root Cause

While suitable as a learning reference, the architecture introduced vendor dependency and recurring operational costs.

### Resolution

Transitioned the project toward a self-hosted Llama-based AI architecture.

### Preventative Action

Evaluate architectural trade-offs before committing to long-term platform dependencies.

---

## Issue 4 — GitHub Integration Write Access

### Status

⚠️ Open

### Component

GitHub Integration

### Symptoms

Repository contents could be read successfully, however automated write operations returned a GitHub integration authorization error.

### Root Cause

The GitHub integration available during development did not have functional write access to the repository.

### Current Workaround

Documentation changes are prepared locally and committed manually.

### Future Action

Re-evaluate repository integration if write access becomes available.

---

# 2026-08-01

## Issue 5 — Ubuntu Server Remote Administration

### Status

✅ Resolved

### Component

Ubuntu Server / SSH

### Symptoms

Direct interaction with the Ubuntu Server through the VirtualBox console was inconvenient for continued development, configuration, and troubleshooting.

A remote administration method was required so the server could be managed from the host laptop terminal.

### Resolution

SSH server functionality was installed and configured on the Ubuntu Server VM.

The SSH service was enabled and the Ubuntu Server became accessible remotely from the laptop terminal.

This provided a more efficient administrative workflow for:

- Linux configuration
- Python development
- Git operations
- Service management
- Troubleshooting
- HomeLab administration

### Result

Remote terminal access to the Ubuntu Server was successfully established and became the primary administration method for continued HomeLab development.

### Preventative Action

Maintain SSH as the primary remote administration method and verify SSH service availability after networking or system configuration changes.

---

## Issue 6 — Slow Local LLM Inference

### Status

✅ Resolved

### Component

Ubuntu Server VM / Ollama / VirtualBox

### Symptoms

During testing of the AI SOC analysis pipeline, execution successfully reached:

`=== AI SOC ANALYSIS ===`

However, the local model took an excessive amount of time to generate a response, initially creating the appearance that the process had stalled.

### Investigation

The Ollama system service was checked and confirmed to be active and running.

The service was also confirmed to be enabled.

`ollama ps` was used during troubleshooting to inspect model execution state.

Because the Ollama service itself was operational, attention shifted from service failure to virtual machine resource availability and local inference performance.

### Root Cause

The Ubuntu Server VM did not initially have sufficient compute resources allocated for acceptable local LLM inference performance.

The primary performance limitation observed during testing was CPU availability.

### Resolution

Virtual machine resources were increased during performance troubleshooting.

Memory allocation was increased during the tuning process.

CPU allocation was subsequently increased to:

- **8 vCPUs**

The AI SOC analysis test was then repeated.

### Result

Increasing the VM CPU allocation produced a significant improvement in local model response time.

The model successfully returned a complete SOC analysis, confirming that Ollama and the local LLM were functioning correctly.

### Preventative Action

Maintain the current 8-vCPU configuration as the known-good CPU baseline.

Avoid further VM resource changes unless inference performance becomes problematic during later phases of the project.

---

## Issue 7 — Ollama Python Integration Verification

### Status

✅ Resolved / Verified

### Component

Python / Ollama / Local LLM

### Symptoms

The project required confirmation that the Python SOC pipeline could successfully submit a security event to the local Ollama API and receive usable AI-generated security analysis.

### Investigation

The following components were verified during testing:

- Python virtual environment
- `src/ollama_client.py`
- Ollama service
- Local language model
- Model response generation
- SOC analysis output

### Resolution

The known-good Python environment was used to execute `src/ollama_client.py` against the local Ollama service.

A test security event representing TCP port-scanning activity was submitted for analysis.

### Verification

The model successfully:

- Recognized the activity as a TCP port scan
- Identified `192.168.50.20` as the scanning host
- Identified `192.168.50.10` as the target
- Assigned a Medium-High severity assessment
- Produced security findings
- Produced recommended response actions

The resulting processing path was successfully validated as:

`Security Event → Python → Ollama API → Local LLM → AI SOC Analysis`

### Result

The Ollama integration test was declared complete.

`src/ollama_client.py` is now considered a known-good implementation and should not be modified while the next integration phase is being established.

### Preventative Action

Preserve the current working implementation before integrating real security telemetry.

Future improvements should be introduced only after the real telemetry pipeline is operational and should be tested against the known-good baseline.

---

## Issue 8 — AI Analysis Recommendation Quality

### Status

⚠️ Improvement Identified

### Component

Local LLM / SOC Analysis

### Symptoms

Although the model successfully analyzed the test event, some remediation recommendations may be overly aggressive when evaluated without sufficient environmental context.

For example, automatically recommending that an internal host be blocked solely because scanning activity was detected may not always be appropriate in an authorized cyber range.

### Root Cause

The current AI analysis operates primarily on the supplied security event and does not yet have complete contextual awareness of authorized HomeLab activity, asset roles, or expected behavior.

### Future Action

Planned improvements include:

- Structured JSON output
- Normalized severity classifications
- MITRE ATT&CK mappings
- Additional environmental context
- Improved recommendation logic
- Differentiation between authorized simulation activity and potentially malicious activity

These improvements are not blockers for the current project phase.
