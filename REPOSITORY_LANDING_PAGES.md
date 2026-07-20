# Production Repository Landing Pages Suite

**Target Profile:** [`pingsaketchoudhary`](https://github.com/pingsaketchoudhary)  
**Operator:** Saket Kumar Choudhary  

This document contains complete, production-ready `README.md` source files for each primary repository in Saket Kumar Choudhary's GitHub ecosystem.

---

## 1. `VulnSightAI` — Production README

```markdown
# VulnSightAI

> **Next-Generation Autonomous Reconnaissance & AI-Driven Vulnerability Assessment Engine**

[![Go Version](https://img.shields.io/badge/Go-1.22%2B-00ADD8?style=flat-square&logo=go&logoColor=white)](https://golang.org)
[![Build Status](https://img.shields.io/badge/CI-Passing-brightgreen?style=flat-square)](https://github.com/pingsaketchoudhary/VulnSightAI/actions)
[![License](https://img.shields.io/badge/License-MIT-blue.style=flat-square)](LICENSE)
[![Release](https://img.shields.io/badge/Release-v2.0.1-00F3FF?style=flat-square)](https://github.com/pingsaketchoudhary/VulnSightAI/releases)

---

### Overview

**VulnSightAI** is an open-source security framework designed for security researchers, red teams, and DevSecOps engineers. It combines a concurrent **Go scanning pipeline** with artificial intelligence model integration to automate target reconnaissance, endpoint discovery, and contextual risk scoring.

```gfm
Target Domain ──► Concurrent Port/Subdomain Audit ──► AST Vulnerability Engine ──► AI Threat Analysis ──► Report
```

---

### Core Architecture & Features

- **Concurrent Network Reconnaissance:** Multi-threaded Go routines for high-throughput port auditing and HTTP banner grabbing.
- **AST & Payload Analysis:** Automated static inspection of web application endpoints and vulnerability fingerprinting.
- **AI Model Risk Scoring:** Integrates local LLM inference engines (Ollama/PyTorch) to contextualize vulnerability severity and generate actionable mitigation paths.
- **Unified Interface:** CLI mode (`vulnsight`) for pipeline integration and interactive Web UI for visualization.

---

### Quick Start

#### Single Binary Installation
Download pre-compiled release binaries directly from [Releases](https://github.com/pingsaketchoudhary/VulnSightAI/releases):

```bash
# Download and install binary
curl -sSL https://raw.githubusercontent.com/pingsaketchoudhary/VulnSightAI/main/start.sh | bash

# Run CLI Scan
vulnsight scan --target example.com --ai-analysis
```

#### Build from Source
```bash
git clone https://github.com/pingsaketchoudhary/VulnSightAI.git
cd VulnSightAI
go build -o vulnsight ./src/...
./vulnsight --help
```

---

### Security & Compliance

Please refer to [.github/SECURITY.md](.github/SECURITY.md) for vulnerability reporting procedures.

**License:** Distributed under the [MIT License](LICENSE).
```

---

## 2. `Atlas` — Production README

```markdown
# Atlas

> **Offline-First, Zero-Telemetry System Intelligence & Diagnostic Console**

[![Rust](https://img.shields.io/badge/Rust-2021%20Edition-000000?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org)
[![Interface](https://img.shields.io/badge/Interface-TUI%20%2F%20GUI-3B82F6?style=flat-square)](https://github.com/pingsaketchoudhary/Atlas)
[![Zero Telemetry](https://img.shields.io/badge/Telemetry-ZERO%20EGRESS-00F3FF?style=flat-square)](https://github.com/pingsaketchoudhary/Atlas)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

---

### Overview

**Atlas** is a high-performance system diagnostics console written in **Rust**. Built with a strict **zero-telemetry design principle**, Atlas guarantees 100% data sovereignty for security professionals, sysadmins, and privacy-sensitive environments.

```gfm
┌────────────────────────────────────────────────────────────────────────┐
│                        ATLAS TUI SYSTEM DASHBOARD                      │
├────────────────────────────────────────────────────────────────────────┤
│ CPU Usage:  [████████████░░░░░░░░] 60%  │ Memory:  [████████░░░░] 4.2GB│
│ Processes:  142 Active / 0 Anomalies   │ Network: 0 External Egress │
└────────────────────────────────────────────────────────────────────────┘
```

---

### Workspace Architecture

Atlas is structured as a multi-crate Cargo workspace to maximize modularity and performance:

- `atlas-core` — Hardware telemetry sampling and process tracing engine.
- `atlas-tui` — Terminal user interface powered by `ratatui` with zero-allocation rendering paths.
- `atlas-cli` — Command-line query interface for script automation.
- `atlas-gui` — Desktop graphical interface.
- `atlas-api` — Local IPC interface for system telemetry integration.

---

### Installation

#### Automated Script (Linux / macOS)
```bash
curl -sSL https://raw.githubusercontent.com/pingsaketchoudhary/Atlas/main/install.sh | bash
```

#### Cargo Build from Source
```bash
git clone https://github.com/pingsaketchoudhary/Atlas.git
cd Atlas
cargo build --release --workspace
./target/release/atlas-tui
```

---

### License

Distributed under the [MIT License](LICENSE).
```

---

## 3. `IRA-Security-Guardian-Releases` — Production README

```markdown
# IRA Security Guardian Releases

> **Official Release & Installer Hub for Cyberfact Security's Enterprise Endpoint Defense Suite**

[![Publisher](https://img.shields.io/badge/Publisher-Cyberfact%20Security-00F3FF?style=flat-square&logo=shield&logoColor=00F3FF)](https://saketchoudhary.in)
[![Status](https://img.shields.io/badge/Status-Stable%20Release-3B82F6?style=flat-square)](https://github.com/pingsaketchoudhary/IRA-Security-Guardian-Releases/releases)
[![Verification](https://img.shields.io/badge/Verification-SHA256%20Checksums-brightgreen?style=flat-square)](SHA256SUMS)

---

### Product Overview

**IRA Security Guardian** is an enterprise-grade endpoint defense system developed by **Cyberfact Security**. This repository serves as the official distribution portal for verified installation binaries, release checksums, and update distributions across Linux, Windows, and macOS endpoints.

---

### Latest Production Release (`v1.0.2-Stable`)

| Platform | Installer Binary | SHA-256 Checksum Verification |
| :--- | :--- | :--- |
| **Linux (64-bit)** | [`ira-guardian-v1.0.2-linux-x64.tar.gz`](downloads/ira-guardian-v1.0.2-linux-x64.tar.gz) | Consult `SHA256SUMS` |
| **Windows (64-bit)** | [`ira-guardian-v1.0.2-windows-x64.msi`](downloads/ira-guardian-v1.0.2-windows-x64.msi) | Consult `SHA256SUMS` |
| **macOS (Apple Silicon)** | [`ira-guardian-v1.0.2-darwin-arm64.pkg`](downloads/ira-guardian-v1.0.2-darwin-arm64.pkg) | Consult `SHA256SUMS` |

---

### Checksum Verification Procedure

To verify installer integrity before deployment:

```bash
# Download binary and SHA256SUMS
curl -O https://github.com/pingsaketchoudhary/IRA-Security-Guardian-Releases/releases/download/v1.0.2/ira-guardian-v1.0.2-linux-x64.tar.gz
curl -O https://github.com/pingsaketchoudhary/IRA-Security-Guardian-Releases/releases/download/v1.0.2/SHA256SUMS

# Verify SHA-256 signature
sha256sum --check --ignore-missing SHA256SUMS
```

---

### Technical Support & Enterprise Inquiries

- **Official Web Portal:** [saketchoudhary.in](https://saketchoudhary.in)
- **Security & Support Line:** [`icybersaket@gmail.com`](mailto:icybersaket@gmail.com)
```

---

## 4. `Tactical-Voice-Recon` (Rebranded `HackerMode`) — Production README

```markdown
# Tactical Voice Recon

> **Tactical IoT Voice Interface & Automated Reconnaissance Controller**

[![Platform](https://img.shields.io/badge/Platform-Amazon%20Alexa%20Skill-FF9900?style=flat-square&logo=alexa&logoColor=white)](https://github.com/pingsaketchoudhary/HackerMode)
[![Domain](https://img.shields.io/badge/Domain-IoT%20Security-00F3FF?style=flat-square)](https://github.com/pingsaketchoudhary/HackerMode)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

---

### Overview

**Tactical Voice Recon** (formerly *HackerMode*) is an IoT security skill framework designed to interface voice control endpoints with security reconnaissance pipelines. It enables voice-assisted query triggers, status checks, and threat alerts for automated security environments.

---

### Architecture

```gfm
Voice Input ──► Alexa Skill Lambda Handler ──► Security API Endpoint ──► Status Response
```

---

### License

Distributed under the [MIT License](LICENSE).
```
