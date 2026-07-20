# Standardized Community Health & Infrastructure Suite

**Target Profile:** [`pingsaketchoudhary`](https://github.com/pingsaketchoudhary)  
**Operator:** Saket Kumar Choudhary  

This document contains production-grade, copy-pasteable `.github/` templates to establish enterprise community health standards across all repositories in Saket Kumar Choudhary's ecosystem.

---

## 1. `.github/SECURITY.md`

```markdown
# Security Policy & Vulnerability Disclosure

## Supported Versions

We publish security patches for active major versions of our software:

| Project / Version | Supported          | Security Maintenance Level |
| ----------------- | ------------------ | -------------------------- |
| `VulnSightAI` v2  | :white_check_mark: | Active Security Updates    |
| `Atlas` v0.1+     | :white_check_mark: | Active Security Updates    |
| Legacy (< 1.0)    | :x:                | End of Life                |

## Reporting a Vulnerability

We take the security and integrity of our open-source tools seriously. If you discover a vulnerability, please do NOT open a public issue.

### Preferred Disclosure Channel
Please report security concerns directly via encrypted email:
- **Primary Email:** [`icybersaket@gmail.com`](mailto:icybersaket@gmail.com)
- **Publisher:** Saket Kumar Choudhary (Founder @ Cyberfact Security)
- **Official Site:** [https://saketchoudhary.in](https://saketchoudhary.in)

### Report Structure
Please include:
1. Affected repository and component version.
2. Step-by-step proof of concept (PoC) or reproduction steps.
3. Potential impact assessment (e.g., local privilege escalation, unauthorized network egress).

### Response SLA
- **Acknowledgement:** Within 24–48 hours.
- **Triage & Impact Assessment:** Within 3–5 business days.
- **Patch & Advisory Release:** Coordinated disclosure timeline (typically 30–60 days).
```

---

## 2. `.github/CONTRIBUTING.md`

```markdown
# Contributing Guidelines

Thank you for your interest in contributing! We welcome contributions to help improve security, performance, and code quality.

## Code Standards

### Go Repositories (`VulnSightAI`)
- Format code using `gofmt` or `goimports`.
- Ensure all tests pass: `go test -v ./...`.
- Pass linter checks: `golangci-lint run`.

### Rust Repositories (`Atlas`)
- Format code using `cargo fmt`.
- Ensure no warnings on workspace targets: `cargo check --all-targets --workspace`.
- Run workspace tests: `cargo test --workspace`.

## Workflow Process

1. **Fork the Repository:** Create a feature branch off `main`.
2. **Commit Changes:** Use conventional commit syntax (`feat: ...`, `fix: ...`, `docs: ...`).
3. **Open a Pull Request:** Fill out the `.github/PULL_REQUEST_TEMPLATE.md` checklist.
```

---

## 3. `.github/PULL_REQUEST_TEMPLATE.md`

```markdown
## Description
A clear and concise summary of the changes introduced in this PR.

## Type of Change
- [ ] Bug fix (non-breaking change fixing an issue)
- [ ] New feature (non-breaking change adding functionality)
- [ ] Refactoring / Optimization (no code functionality change)
- [ ] Documentation update

## Verification & Testing
Describe the verification steps conducted:
1. `cargo test --workspace` / `go test ./...`
2. Verified on Operating Systems: [ ] Linux [ ] macOS [ ] Windows

## Checklist
- [ ] My code follows the style guidelines of this project.
- [ ] I have performed a self-review of my code.
- [ ] I have updated documentation accordingly.
```

---

## 4. `.github/ISSUE_TEMPLATE/bug_report.yml`

```yaml
name: Bug Report
description: Create a report to help us improve software stability.
labels: ["kind/bug", "status/triage"]
body:
  - type: markdown
    attributes:
      value: |
        Thank you for taking the time to report a bug!
  - type: input
    id: environment
    attributes:
      label: Environment & Version
      description: OS (e.g. Ubuntu 22.04, Arch Linux), Go/Rust version, CLI tool version.
      placeholder: e.g. Linux 6.5 x86_64, Go 1.22.1, VulnSightAI v2.0.1
    validations:
      required: true
  - type: textarea
    id: expected
    attributes:
      label: Expected Behavior
      description: What did you expect to happen?
    validations:
      required: true
  - type: textarea
    id: actual
    attributes:
      label: Actual Behavior & Logs
      description: What actually happened? Provide terminal log output if available.
    validations:
      required: true
```

---

## 5. Standardized Label Taxonomy (`LABEL_SCHEMA.json`)

```json
[
  { "name": "kind/bug", "color": "d93f0b", "description": "Something isn't working as expected" },
  { "name": "kind/feature", "color": "a2eeef", "description": "New feature request or enhancement" },
  { "name": "kind/docs", "color": "0075ca", "description": "Improvements or additions to documentation" },
  { "name": "kind/security", "color": "7057ff", "description": "Security-related fix or vulnerability hardening" },
  { "name": "area/go", "color": "00add8", "description": "Go codebase component" },
  { "name": "area/rust", "color": "000000", "description": "Rust codebase component" },
  { "name": "status/triage", "color": "fef2c0", "description": "Awaiting triage by maintainers" },
  { "name": "status/accepted", "color": "0e8a16", "description": "Issue accepted for implementation" }
]
```
