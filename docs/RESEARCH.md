# Research Notes

## Current References

### AIRIA AI Cybersecurity Tutorial

Purpose

Reference implementation for the initial architecture.

Status

# AI Model Selection Research

## Objective

Identify an AI solution suitable for a self-hosted cybersecurity homelab.

---

## Initial Approach

The project initially evaluated a vendor-hosted AI workflow as part of the reference architecture.

While this provided a useful introduction to AI-assisted security operations, it introduced long-term considerations related to recurring costs, vendor dependency, and reduced control over the AI environment.

---

## Research Findings

The project shifted toward a self-hosted open-weight large language model to achieve:

- Zero recurring licensing costs for local inference
- Greater control over the AI infrastructure
- Improved data privacy by processing telemetry locally
- Flexibility to evaluate multiple AI models
- Better understanding of deploying and operating LLMs

---

## Selected Direction

The planned AI platform is based on:

- **Llama 3 8B Instruct**

This model was selected as the initial target because it provides a strong balance between capability and the hardware resources available for the homelab.

Future model evaluations may include additional open-weight LLMs as the project evolves.

---

## Engineering Decision

The objective is not simply to use a free AI model.

The objective is to build a sustainable, vendor-independent AI platform that supports long-term experimentation, cybersecurity research, and continuous learning without recurring operational costs.

Reference Architecture Version 1.0

---

Future research topics will be documented as the project expands.
