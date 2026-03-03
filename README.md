<div align="center">

```
███████╗██╗   ██╗███╗   ██╗      ██████╗ ███████╗
██╔════╝╚██╗ ██╔╝████╗  ██║     ██╔═══██╗██╔════╝
███████╗ ╚████╔╝ ██╔██╗ ██║     ██║   ██║███████╗
╚════██║  ╚██╔╝  ██║╚██╗██║     ██║   ██║╚════██║
███████║   ██║   ██║ ╚████║     ╚██████╔╝███████║
╚══════╝   ╚═╝   ╚═╝  ╚═══╝      ╚═════╝ ╚══════╝
```

**AI-Enhanced Cybersecurity Operating System**

[![Status](https://img.shields.io/badge/Status-Active%20Development-brightgreen?style=flat-square)](https://github.com/SynOSdev)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=flat-square)](https://github.com/SynOSdev)
[![Security](https://img.shields.io/badge/Focus-Offensive%20%26%20Defensive%20Security-blueviolet?style=flat-square)](https://github.com/SynOSdev)
[![Version](https://img.shields.io/badge/Version-Post%20v20-blue?style=flat-square)](https://github.com/SynOSdev)
[![Codespaces](https://img.shields.io/badge/Codespaces-Ready-2088FF?style=flat-square&logo=github)](https://github.com/SynOSdev/README.md)

</div>

---

## Mission

Syn_OS is a security-focused operating system engineered for professionals operating at the intersection of offensive research, infrastructure hardening, and AI-driven threat analysis. Built from the ground up with a minimal-footprint, maximum-capability philosophy—every component is intentional, auditable, and replaceable.

> *"Minimal surface. Maximum signal. Zero noise."*

---

## Core Capabilities

| Domain | Capability |
|---|---|
| 🔴 Offensive Operations | Exploit development, red-team tooling, CTF automation |
| 🔵 Defensive Operations | Hardened baseline, anomaly detection, audit-ready configs |
| 🤖 AI Integration | Local LLM assistance for triage, recon, and report generation |
| 🌐 Network Ops | Mesh networking support, covert channel analysis |
| 🔬 Reverse Engineering | Binary analysis workflows, malware research environment |
| 📡 SIGINT / OSINT | Modular collection and correlation pipelines |
| 📱 Mobile Operations | Moto Z Play ADB bridge, mobile mesh networking, field deployment |

---

## Technology Stack

### Languages

[![Python](https://img.shields.io/badge/-Python%203.12-informational?logo=python&logoColor=white&style=flat-square)](https://python.org)
[![Rust](https://img.shields.io/badge/-Rust%201.80-orange?logo=rust&logoColor=white&style=flat-square)](https://rust-lang.org)
[![Go](https://img.shields.io/badge/-Go%201.23-blue?logo=go&logoColor=white&style=flat-square)](https://go.dev)
[![C](https://img.shields.io/badge/-C%20%2F%20C++-blue?logo=c&logoColor=white&style=flat-square)](https://gcc.gnu.org)
[![Assembly](https://img.shields.io/badge/-x86--64%20Assembly-lightgrey?logo=gnubash&logoColor=white&style=flat-square)](https://nasm.us)
[![Bash](https://img.shields.io/badge/-Bash%205-black?logo=gnubash&logoColor=white&style=flat-square)](https://gnu.org/software/bash)

### Infrastructure & Tooling

[![Linux](https://img.shields.io/badge/-Linux%20Kernel-black?logo=linux&logoColor=white&style=flat-square)](https://kernel.org)
[![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white&style=flat-square)](https://docker.com)
[![Nix](https://img.shields.io/badge/-Nix%2FNixOS-5277C3?logo=nixos&logoColor=white&style=flat-square)](https://nixos.org)
[![QEMU](https://img.shields.io/badge/-QEMU%2FKVM-FF6600?logo=qemu&logoColor=white&style=flat-square)](https://qemu.org)
[![Git](https://img.shields.io/badge/-Git-F05032?logo=git&logoColor=white&style=flat-square)](https://git-scm.com)
[![Codespaces](https://img.shields.io/badge/-Codespaces-2088FF?logo=github&logoColor=white&style=flat-square)](https://github.com/features/codespaces)

---

## Active Projects

| Project | Description | Status |
|---|---|---|
| **Syn_OS Core** | Base OS image — hardened kernel, custom init, toolchain | 🔧 Beta |
| **Host Config** | Merged host configuration — system defaults, shell, networking | ✅ Integrated |
| **Mobile Bridge** | Moto Z Play ADB integration and mobile mesh networking | 🔬 Research |
| **AI Triage Module** | Local LLM integration for alert correlation and recon automation | 🔬 Research |
| **Mesh C2 Framework** | Resilient mesh-networked command layer for distributed ops | 🔒 Private |
| **CTF Toolkit** | Modular challenge automation and solution scaffolding | 🔧 Active |

---

## Post-v20 Research: Mobile System Connection & Development

> Full research notes: [`docs/post-v20-mobile-research.md`](docs/post-v20-mobile-research.md)

The post-v20 milestone focuses on mobile-first field deployment using the **Moto Z Play** as the primary mobile development and operations platform. This research covers ADB connectivity, USB tethering for Codespace access, mobile mesh networking, and offline-capable development workflows for solo-dev field operations.

### Key Research Areas

| Area | Description |
|---|---|
| **ADB Bridge** | Android Debug Bridge configuration for Moto Z Play → Syn_OS host |
| **USB Tethering** | Mobile hotspot and USB tethering for Codespace connectivity in the field |
| **Termux Integration** | On-device terminal environment for emergency ops when laptop is unavailable |
| **Offline Sync** | Git bundle workflows for air-gapped development and later push |
| **Moto Mod Support** | Research into Moto Mod hardware extensions for field sensor integration |
| **Battery Management** | Power-optimized development workflow for extended field sessions |

---

## Host Configuration (Merged)

> Full config files: [`hostconfig/`](hostconfig/)
> Configuration audit: [`docs/config-audit-report.md`](docs/config-audit-report.md)

The `hostconfig/` directory contains the merged and deduplicated host configuration for Syn_OS systems. These are the default system configs previously maintained in a separate repository, now integrated into the master repo for single-source management.

```
hostconfig/
├── bashrc              # Shell configuration and aliases
├── profile             # Login shell environment
├── ssh_config          # SSH client hardened defaults
├── sshd_config         # SSH daemon hardened configuration
├── gitconfig           # Git configuration and aliases
├── tmux.conf           # Terminal multiplexer settings
├── nanorc              # Editor configuration
├── hosts               # Static host entries
├── resolv.conf         # DNS resolver configuration
├── sysctl.conf         # Kernel parameter tuning
├── ufw-rules           # Firewall rule set
└── network-interfaces  # Network interface configuration
```

---

## Codespace & Workspace Configuration

This repository is **Codespace-ready** with Syn_OS defaults pre-configured. Open in Codespaces for an instant development environment with all tools pre-installed.

[![Open in Codespaces](https://img.shields.io/badge/Open%20in-Codespaces-2088FF?style=for-the-badge&logo=github)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=SynOSdev/README.md)

- **Dev container**: Debian-based with security tooling pre-installed
- **VS Code settings**: Syn_OS workspace defaults applied automatically
- **Extensions**: Security-focused extension pack included
- **Shell**: Bash with Syn_OS aliases and prompt

---

## Research & Practice Platforms

[![TryHackMe](https://img.shields.io/badge/TryHackMe-DiabloRain%20%2F%20Syn__OS-12100E?logo=tryhackme&logoColor=white&style=flat-square)](https://tryhackme.com)
[![Hack The Box](https://img.shields.io/badge/Hack%20The%20Box-Active-2D2D2D?logo=hackthebox&logoColor=9FEF00&style=flat-square)](https://hackthebox.com)
[![BugCrowd](https://img.shields.io/badge/BugCrowd-DiabloRain-F26822?logo=bugcrowd&logoColor=white&style=flat-square)](https://bugcrowd.com)
[![HackerOne](https://img.shields.io/badge/HackerOne-Active-494649?logo=hackerone&logoColor=white&style=flat-square)](https://hackerone.com)
[![Intigriti](https://img.shields.io/badge/Intigriti-Active-1A1A2E?style=flat-square)](https://intigriti.com)

---

## Operational Principles

- **Least Privilege by Default** — Every process, user, and service runs with the minimum access required.
- **Air-Gap Awareness** — Core tooling is designed to function without internet connectivity.
- **Reproducibility** — Builds are deterministic; any deployment can be validated against a known-good state.
- **Separation of Concerns** — Red-team tooling is containerized and isolated from defensive instrumentation.
- **No Telemetry** — No data leaves the system without explicit operator action.
- **Mobile-Ready** — Field-deployable workflows that function over cellular/tethered connections.

---

## Repository Structure

```
.
├── README.md                          # This file — project overview
├── .devcontainer/
│   └── devcontainer.json              # Codespace / dev container configuration
├── .vscode/
│   └── settings.json                  # Syn_OS workspace defaults
├── docs/
│   ├── post-v20-mobile-research.md    # Moto Z Play & mobile dev research
│   └── config-audit-report.md         # 30-point configuration audit
└── hostconfig/
    ├── bashrc                         # Shell configuration
    ├── profile                        # Login environment
    ├── ssh_config                     # SSH client config
    ├── sshd_config                    # SSH daemon config
    ├── gitconfig                      # Git defaults
    ├── tmux.conf                      # Tmux configuration
    ├── nanorc                         # Editor config
    ├── hosts                          # Static hosts
    ├── resolv.conf                    # DNS resolver
    ├── sysctl.conf                    # Kernel tuning
    ├── ufw-rules                      # Firewall rules
    └── network-interfaces             # Network config
```

---

## Contributing & Engagement

This organization is **not accepting unsolicited pull requests** to private repositories at this time. Public repositories may accept contributions — see `CONTRIBUTING.md` in each repo.

If you have a **puzzle, challenge, or research idea** relevant to the project scope, open a Discussion in the appropriate public repository.

**Bug Bounty:** Responsible disclosure is welcomed. See the security policy in public repositories for scope and rules of engagement.

---

<div align="center">

*"Amateurs hack systems. Professionals build them."*

[![GitHub Org](https://img.shields.io/badge/GitHub-SynOSdev-181717?logo=github&logoColor=white&style=flat-square)](https://github.com/SynOSdev)

</div>