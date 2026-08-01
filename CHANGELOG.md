# Change Log

## Version 0.1.0 - 2026-07-31

- Repository initialized.

## Version 0.1.1 - 2026-07-31

### Changed

- Centralized project documentation into the `docs/` directory.

### Removed

- `MASTER_DOCUMENTATION.md` in favor of a modular documentation structure.

## Version 0.2.0 - 2026-08-01

### Added

- Configured SSH remote administration for the Ubuntu Server VM.
- Established remote Ubuntu Server access from the host laptop terminal.
- Installed and configured the local Ollama inference service.
- Integrated the Llama 3 8B Instruct model for local AI-assisted security analysis.
- Created and validated the Python-to-Ollama SOC analysis workflow.
- Established `src/ollama_client.py` as the working integration between Python and the local Ollama API.
- Added AI-generated SOC analysis containing event summaries, severity assessments, findings, and recommended actions.

### Changed

- Increased Ubuntu Server virtual machine resources to improve local LLM inference performance.
- Increased Ubuntu Server CPU allocation to 8 vCPUs.
- Increased VM memory allocation during local LLM performance tuning.
- Updated the project architecture from a primarily planned AI workflow to a partially verified operational AI analysis pipeline.
- Updated Ollama service status from In Development to Operational.
- Updated Llama service status from In Development to Operational.
- Updated Python automation status from Planned to In Development.

### Fixed

- Resolved excessively slow local LLM response generation during AI SOC analysis testing.
- Improved Ollama inference performance through virtual machine resource tuning.
- Verified that apparent delays at the `AI SOC ANALYSIS` stage were related to inference performance rather than an Ollama service failure.

### Verified

- Ollama system service is active and operational.
- Python virtual environment is functional.
- `src/ollama_client.py` successfully communicates with the Ollama API.
- Local Llama model successfully returns complete SOC analysis.
- Test TCP port-scan activity was correctly interpreted by the AI analysis workflow.
- The test identified `192.168.50.20` as the scanning host and `192.168.50.10` as the target.
- The working processing path is currently:

  `Security Event → Python → Ollama API → Local LLM → AI SOC Analysis`

### Documentation

- Updated service documentation to reflect operational Ollama and Llama components.
- Added Ubuntu Server resource allocation and performance-tuning information.
- Expanded troubleshooting documentation with SSH administration, Ollama performance, Python integration, and AI recommendation-quality findings.
- Updated architecture documentation to distinguish verified components from planned telemetry integration.

### Next Phase

- Integrate real HomeLab-generated security telemetry with the verified AI analysis pipeline.
- Establish the processing path:

  `Kali Linux → Monitored Target → Security Telemetry → Detection / Alert → Python → Ollama → AI SOC Analysis`
