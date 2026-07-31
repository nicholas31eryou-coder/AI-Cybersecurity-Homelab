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
