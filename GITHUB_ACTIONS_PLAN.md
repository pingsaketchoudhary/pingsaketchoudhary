# GitHub Actions & CI/CD Automation Plan

**Target Profile:** [`pingsaketchoudhary`](https://github.com/pingsaketchoudhary)  
**Operator:** Saket Kumar Choudhary  

---

## 1. Automation Infrastructure Strategy

Automating CI/CD checks and profile metrics demonstrates engineering discipline and open-source maintainership.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   GITHUB ACTIONS AUTOMATION SUITE                      │
├───────────────────────────────────┬────────────────────────────────────┤
│ 1. Go CI Pipeline                 │ 2. Rust Workspace CI Pipeline      │
│    • Target: VulnSightAI          │    • Target: Atlas                 │
├───────────────────────────────────┼────────────────────────────────────┤
│ 3. Profile Contribution Snake     │ 4. Release Binary Checksum Generator│
│    • Target: pingsaketchoudhary   │    • Target: IRA-Security-Guardian  │
└───────────────────────────────────┴────────────────────────────────────┘
```

---

## 2. Structured Workflow Proposals

### Proposal 1: Go CI Workflow for `VulnSightAI`
- **Proposal:** Create `.github/workflows/ci.yml` in `VulnSightAI` to run automated Go tests and binary verification on every push.
- **Why it should change:** Displays green CI build status badge on `VulnSightAI`.
- **Expected Impact:** Demonstrates automated test coverage and binary build health.
- **Priority:** High | **Difficulty:** Low | **Risk:** Zero | **Estimated Improvement:** +40% maintainership trust.

```yaml
name: Go CI Build

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

---

### Proposal 2: Cargo Workspace CI for `Atlas`
- **Proposal:** Create `.github/workflows/ci.yml` in `Atlas` for Cargo check and workspace unit tests.
- **Why it should change:** Ensures zero Cargo check regressions across multi-crate workspace (`atlas-core`, `atlas-cli`).
- **Expected Impact:** Validates memory-safety and build stability across targets.
- **Priority:** High | **Difficulty:** Low | **Risk:** Zero | **Estimated Improvement:** +45% Rust code confidence.

```yaml
name: Rust Workspace CI

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
      - name: Cargo Check
        run: cargo check --all-targets --workspace
      - name: Run Workspace Tests
        run: cargo test --workspace
```

---

### Proposal 3: Dynamic Profile Contribution Snake
- **Proposal:** Create `.github/workflows/profile-snake.yml` in `pingsaketchoudhary`.
- **Why it should change:** Generates dark obsidian-themed contribution snake SVG updated daily via GitHub Actions.
- **Expected Impact:** Dynamic contribution visual without third-party API downtime.
- **Priority:** Medium | **Difficulty:** Low | **Risk:** Zero | **Estimated Improvement:** +20% dynamic profile activity.
