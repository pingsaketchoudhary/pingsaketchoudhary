# Community Health & Governance Architecture

**Target Profile:** [`pingsaketchoudhary`](https://github.com/pingsaketchoudhary)  
**Operator:** Saket Kumar Choudhary  

This document provides production-ready, copy-pasteable `.github/` community health templates to establish enterprise governance across all public repositories.

---

## 1. Structured Community Governance Proposal

### Proposal 1: Unified Security Disclosure Policy (`SECURITY.md`)
- **Proposal:** Deploy `.github/SECURITY.md` across all primary repositories (`VulnSightAI`, `Atlas`, `IRA-Security-Guardian-Releases`).
- **Why it should change:** Establishes formal vulnerability reporting procedures and encrypted contact lines (`icybersaket@gmail.com`).
- **Expected Impact:** Demonstrates security maturity to external researchers and enterprise auditing teams.
- **Priority:** High | **Difficulty:** Low | **Risk:** Zero | **Estimated Improvement:** +50% security posture.

---

## 2. Production Templates Suite

### A. `.github/SECURITY.md`
```markdown
# Security Policy & Responsible Disclosure

## Supported Versions

| Project / Version | Supported          | Maintenance Level |
| ----------------- | ------------------ | ----------------- |
| `VulnSightAI` v2  | :white_check_mark: | Active Security Updates |
| `Atlas` v0.1+     | :white_check_mark: | Active Security Updates |
| Legacy (< 1.0)    | :x:                | End of Life       |

## Reporting a Vulnerability

Please report security concerns directly via encrypted email:
- **Email:** [`icybersaket@gmail.com`](mailto:icybersaket@gmail.com)
- **Publisher:** Saket Kumar Choudhary (Founder @ Cyberfact Security)
- **Official Site:** [https://saketchoudhary.in](https://saketchoudhary.in)

### Response SLA
- **Acknowledgement:** Within 24–48 hours.
- **Triage Assessment:** Within 3–5 business days.
```

---

### B. `.github/CONTRIBUTING.md`
```markdown
# Contributing Guidelines

Thank you for contributing! Please follow these standards to ensure code quality:

## Code Formatting
- **Go (`VulnSightAI`):** Format with `gofmt`. Run `go test ./...`.
- **Rust (`Atlas`):** Format with `cargo fmt`. Run `cargo test --workspace`.

## Pull Request Submission
1. Fork repository and branch from `main`.
2. Write conventional commit messages (`feat: ...`, `fix: ...`).
3. Complete `.github/PULL_REQUEST_TEMPLATE.md`.
```

---

### C. `.github/PULL_REQUEST_TEMPLATE.md`
```markdown
## Description
Summary of changes introduced in this PR.

## Type of Change
- [ ] Bug fix (non-breaking change)
- [ ] New feature (non-breaking change)
- [ ] Documentation update

## Verification & Testing
- [ ] `cargo test --workspace` / `go test ./...`
- Tested OS: [ ] Linux [ ] macOS [ ] Windows
```

---

### D. `.github/ISSUE_TEMPLATE/bug_report.yml`
```yaml
name: Bug Report
description: Report a bug or regression.
labels: ["kind/bug", "status/triage"]
body:
  - type: input
    id: env
    attributes:
      label: Environment & OS Version
      placeholder: e.g. Linux 6.5 x86_64, Go 1.22, VulnSightAI v2.0.1
    validations:
      required: true
  - type: textarea
    id: actual
    attributes:
      label: Description of Issue & Terminal Logs
    validations:
      required: true
```

---

### E. Standardized Label Taxonomy (`LABEL_SCHEMA.json`)
```json
[
  { "name": "kind/bug", "color": "d93f0b", "description": "Something isn't working as expected" },
  { "name": "kind/feature", "color": "a2eeef", "description": "New feature request or enhancement" },
  { "name": "kind/security", "color": "7057ff", "description": "Security hardening or vulnerability fix" },
  { "name": "area/go", "color": "00add8", "description": "Go codebase component" },
  { "name": "area/rust", "color": "000000", "description": "Rust codebase component" }
]
```
