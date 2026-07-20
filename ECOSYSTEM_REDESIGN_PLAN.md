# Master GitHub Ecosystem Redesign & Engineering Plan

**Target Profile:** [`pingsaketchoudhary`](https://github.com/pingsaketchoudhary)  
**Operator:** Saket Kumar Choudhary  
**Primary Track:** AI Security Engineer • Offensive Security Researcher • Founder (`Cyberfact Security`)  

---

## 1. Repository Ecosystem Restructuring

```
┌────────────────────────────────────────────────────────────────────────┐
│                   RESTRUCTURED REPOSITORY ECOSYSTEM                    │
├───────────────────────────────────┬────────────────────────────────────┤
│ 1. VulnSightAI (Flagship)        │ 2. Atlas (Rust Systems Platform)   │
│    • Domain: AI Recon & SAST      │    • Domain: Zero-Telemetry TUI    │
├───────────────────────────────────┼────────────────────────────────────┤
│ 3. IRA-Security-Guardian-Releases │ 4. Tactical-Voice-Recon (Rebranded)│
│    • Domain: Enterprise Releases  │    • Domain: IoT Security Control  │
├───────────────────────────────────┼────────────────────────────────────┤
│ [ARCHIVED] Password-generator     │ [PRIVATE] anniversary-celebration  │
└───────────────────────────────────┴────────────────────────────────────┘
```

### Action Blueprint Per Repository

| Repository | Current Name | Recommended Name | Target Topics | Action Blueprint |
| :--- | :--- | :--- | :--- | :--- |
| **`VulnSightAI`** | `VulnSightAI` | `VulnSightAI` | `ai-security`, `reconnaissance-framework`, `vulnerability-assessment`, `go-security`, `red-teaming`, `sast`, `security-automation` | Overhaul README. Remove skull ASCII graphics. Highlight Go concurrent scanner and AST vulnerability parser. |
| **`Atlas`** | `Atlas` | `Atlas` | `rust`, `system-monitor`, `telemetry`, `cross-platform`, `tui`, `diagnostics`, `zero-telemetry`, `ratatui`, `performance-monitoring` | Add ASCII TUI terminal mockup in README. Document multi-crate Cargo architecture. |
| **`IRA-Security-Guardian-Releases`** | `IRA-Security-Guardian-Releases` | `IRA-Security-Guardian-Releases` | `cyberfact-security`, `security-software`, `endpoint-protection`, `installer-hub`, `release-binaries`, `sha256-verification` | Rewrite README as Cyberfact Security Enterprise Product Portal. Remove legacy handle references. Add SHA-256 integrity guide. |
| **`HackerMode`** | `HackerMode` | `Tactical-Voice-Recon` | `alexa-skill`, `iot-security`, `voice-interface`, `security-automation`, `recon-controller` | Rename repository or update documentation. Add MIT license and structured IoT voice recon specs. |
| **`Password-generator`** | `Password-generator` | `sec-passgen` *(or Archive)* | `python`, `cryptography`, `cli-tool` | Archive repository as read-only, or refactor into CLI tool with `secrets` module and `argparse`. |
| **`anniversary-celebration`** | `anniversary-celebration` | N/A *(Set Private)* | N/A | Set visibility to Private. |

---

## 2. Visual Design System & Dark Cyber Palette

The entire profile ecosystem follows a strict **Tactical Obsidian & Cyber Cyan** color system:

```gfm
Primary Background:     #0B0F19  (Obsidian Midnight)
Card / Container:       #1E293B  (Tactical Slate)
Primary Accent:         #00F3FF  (Electric Cyber Cyan)
Secondary Accent:       #3B82F6  (Deep Cobalt Blue)
Text / Headings:        #F8FAFC  (High-Contrast Pure Silver)
Text / Muted:           #94A3B8  (Steel Gray)
Alert / Warning:        #F59E0B  (Security Amber)
```

### Visual Palette Representation

- `████████` **Obsidian Midnight** (`#0B0F19` - Base background)
- `████████` **Tactical Slate** (`#1E293B` - Card container background)
- `████████` **Electric Cyber Cyan** (`#00F3FF` - Highlight accent & primary badges)
- `████████` **Deep Cobalt Blue** (`#3B82F6` - Secondary accent & repository links)

---

## 3. GitHub Pages & Custom Domain Architecture

- **Primary Portfolio URL:** `https://saketchoudhary.in`
- **DNS / CNAME Setup:** CNAME record pointing `saketchoudhary.in` to `pingsaketchoudhary.github.io`.
- **HTTPS Enforcement:** Enforce HTTPS via GitHub Pages settings.
- **Enterprise Portal:** Establish `cyberfact-security` organization on GitHub with clean product links to `saketchoudhary.in`.

---

## 4. GitHub Actions CI/CD Workflows

### A. Go CI & Binary Compilation (`VulnSightAI/.github/workflows/ci.yml`)
```yaml
name: Go CI Build & Test

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set up Go
        uses: actions/setup-go@v5
        with:
          go-version: '1.22'
      - name: Verify Dependencies
        run: go mod verify
      - name: Run Tests
        run: go test -v ./...
      - name: Build Binary
        run: go build -o bin/vulnsight ./src/...
```

### B. Cargo Build & Check (`Atlas/.github/workflows/ci.yml`)
```yaml
name: Rust CI Pipeline

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set up Rust
        uses: dtolnay/rust-toolchain@stable
      - name: Run Cargo Check
        run: cargo check --all-targets --workspace
      - name: Run Tests
        run: cargo test --workspace
```

---

## 5. Social Preview Assets & SVG Banner Specifications

- **Dimensions:** 1200 x 630 px (OpenGraph Standard)
- **Background:** Dark Obsidian (`#0B0F19`) with fine grid overlay.
- **Text Elements:** "SAKET KUMAR CHOUDHARY" in bold high-contrast silver (`#F8FAFC`), subtitle "AI Security Engineer • Offensive Security Researcher" in Electric Cyan (`#00F3FF`).
- **Logo Elements:** Cyberfact Security Shield SVG and Rust/Go official vector marks.
