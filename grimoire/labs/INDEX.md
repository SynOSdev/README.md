# 📚 GRIMOIRE Lab Index

> Complete catalog of all 42 GRIMOIRE labs organized by track.

## Core Foundation (All Factions)

| Lab | Title | Difficulty | XP | Prerequisites |
|-----|-------|-----------|-----|---------------|
| [LAB-001](core/LAB-001.md) | Terminal Basics and Shell Navigation | ⭐ | 100 | None |
| [LAB-002](core/LAB-002.md) | Network Fundamentals and Packet Analysis | ⭐⭐ | 150 | LAB-001 |
| [LAB-003](core/LAB-003.md) | Linux System Administration Essentials | ⭐⭐ | 150 | LAB-001 |
| [LAB-004](core/LAB-004.md) | Cryptography Foundations | ⭐⭐ | 150 | LAB-001 |
| [LAB-005](core/LAB-005.md) | Web Technologies and HTTP | ⭐⭐ | 150 | LAB-001, LAB-002 |
| [LAB-006](core/LAB-006.md) | Scripting Fundamentals | ⭐⭐ | 200 | LAB-001 |
| [LAB-007](core/LAB-007.md) | Log Analysis and SIEM Basics | ⭐⭐ | 150 | LAB-001, LAB-006 |
| [LAB-008](core/LAB-008.md) | Introduction to Vulnerability Assessment | ⭐⭐⭐ | 200 | LAB-001, LAB-002, LAB-003 |

## 🔴 Crimson Circuit — Red Team

| Lab | Title | Difficulty | XP | Prerequisites |
|-----|-------|-----------|-----|---------------|
| [LAB-009](red-team/LAB-009.md) | Reconnaissance and OSINT Techniques | ⭐⭐ | 150 | LAB-001, LAB-002, LAB-005 |
| [LAB-010](red-team/LAB-010.md) | Network Scanning and Enumeration | ⭐⭐ | 200 | LAB-002, LAB-008, LAB-009 |
| [LAB-011](red-team/LAB-011.md) | Exploitation Fundamentals | ⭐⭐⭐ | 250 | LAB-008, LAB-010 |
| [LAB-012](red-team/LAB-012.md) | Web Application Attacks | ⭐⭐⭐ | 250 | LAB-005, LAB-011 |
| [LAB-013](red-team/LAB-013.md) | Privilege Escalation Techniques | ⭐⭐⭐ | 250 | LAB-003, LAB-011 |
| [LAB-014](red-team/LAB-014.md) | Password Attacks and Credential Harvesting | ⭐⭐⭐ | 200 | LAB-004, LAB-011 |
| [LAB-015](red-team/LAB-015.md) | Lateral Movement and Pivoting | ⭐⭐⭐⭐ | 300 | LAB-011, LAB-013 |
| [LAB-016](red-team/LAB-016.md) | Post-Exploitation and Data Exfiltration | ⭐⭐⭐⭐ | 300 | LAB-013, LAB-015 |

## 🔵 Azure Shield — Blue Team

| Lab | Title | Difficulty | XP | Prerequisites |
|-----|-------|-----------|-----|---------------|
| [LAB-017](blue-team/LAB-017.md) | Firewall Configuration and Network Hardening | ⭐⭐ | 150 | LAB-002, LAB-003 |
| [LAB-018](blue-team/LAB-018.md) | Intrusion Detection and Prevention Systems | ⭐⭐⭐ | 200 | LAB-002, LAB-007, LAB-017 |
| [LAB-019](blue-team/LAB-019.md) | Incident Response Procedures | ⭐⭐⭐ | 250 | LAB-007, LAB-008 |
| [LAB-020](blue-team/LAB-020.md) | Malware Analysis Fundamentals | ⭐⭐⭐ | 250 | LAB-003, LAB-006 |
| [LAB-021](blue-team/LAB-021.md) | Digital Forensics and Evidence Collection | ⭐⭐⭐ | 250 | LAB-003, LAB-007 |
| [LAB-022](blue-team/LAB-022.md) | Endpoint Detection and Response | ⭐⭐⭐ | 200 | LAB-003, LAB-007, LAB-020 |
| [LAB-023](blue-team/LAB-023.md) | Security Information and Event Management | ⭐⭐⭐⭐ | 300 | LAB-007, LAB-018, LAB-022 |
| [LAB-024](blue-team/LAB-024.md) | Threat Intelligence and IOC Management | ⭐⭐⭐ | 250 | LAB-007, LAB-008, LAB-019 |

## 🟣 Violet Nexus — Purple Team

| Lab | Title | Difficulty | XP | Prerequisites |
|-----|-------|-----------|-----|---------------|
| [LAB-025](purple-team/LAB-025.md) | Attack Simulation and Detection Mapping | ⭐⭐⭐ | 250 | LAB-008, LAB-011, LAB-018 |
| [LAB-026](purple-team/LAB-026.md) | MITRE ATT&CK Framework Operations | ⭐⭐⭐ | 250 | LAB-025 |
| [LAB-027](purple-team/LAB-027.md) | Red vs Blue War Games | ⭐⭐⭐⭐ | 300 | LAB-016, LAB-019, LAB-025 |
| [LAB-028](purple-team/LAB-028.md) | Security Control Validation | ⭐⭐⭐ | 250 | LAB-017, LAB-025 |
| [LAB-029](purple-team/LAB-029.md) | Adversary Emulation Plans | ⭐⭐⭐⭐ | 300 | LAB-026, LAB-027 |
| [LAB-030](purple-team/LAB-030.md) | Detection Engineering and Rule Writing | ⭐⭐⭐⭐ | 300 | LAB-018, LAB-025, LAB-026 |

## 👻 Shadow Protocol — Ghost Team

| Lab | Title | Difficulty | XP | Prerequisites |
|-----|-------|-----------|-----|---------------|
| [LAB-031](ghost-team/LAB-031.md) | Advanced OSINT and Social Engineering Awareness | ⭐⭐⭐ | 250 | LAB-005, LAB-009 |
| [LAB-032](ghost-team/LAB-032.md) | Dark Web Navigation and Monitoring | ⭐⭐⭐ | 200 | LAB-002, LAB-031 |
| [LAB-033](ghost-team/LAB-033.md) | Steganography and Covert Channels | ⭐⭐⭐ | 250 | LAB-004, LAB-006 |
| [LAB-034](ghost-team/LAB-034.md) | Anonymous Operations and OpSec | ⭐⭐⭐ | 250 | LAB-002, LAB-004, LAB-032 |
| [LAB-035](ghost-team/LAB-035.md) | Counter-Intelligence Techniques | ⭐⭐⭐⭐ | 300 | LAB-031, LAB-034 |
| [LAB-036](ghost-team/LAB-036.md) | Threat Actor Profiling and Attribution | ⭐⭐⭐⭐ | 300 | LAB-031, LAB-035 |

## 🛠️ Build Your Own — Capstone

| Lab | Title | Difficulty | XP | Prerequisites |
|-----|-------|-----------|-----|---------------|
| [LAB-037](build-your-own/LAB-037.md) | Build Your Own Security Dashboard | ⭐⭐⭐⭐ | 400 | LAB-007, LAB-022, LAB-023 |
| [LAB-038](build-your-own/LAB-038.md) | Build Your Own Threat Detection Pipeline | ⭐⭐⭐⭐ | 400 | LAB-007, LAB-018, LAB-030 |
| [LAB-039](build-your-own/LAB-039.md) | Build Your Own Vulnerability Scanner | ⭐⭐⭐⭐ | 400 | LAB-008, LAB-010, LAB-028 |
| [LAB-040](build-your-own/LAB-040.md) | Build Your Own Incident Response Toolkit | ⭐⭐⭐⭐ | 400 | LAB-019, LAB-021, LAB-022 |
| [LAB-041](build-your-own/LAB-041.md) | Build Your Own Secure Communication System | ⭐⭐⭐⭐ | 400 | LAB-004, LAB-034 |
| [LAB-042](build-your-own/LAB-042.md) | Build Your Own Integrated Security Suite | ⭐⭐⭐⭐⭐ | 500 | LAB-037–LAB-041 |

---

## Totals

- **42 Labs** across 6 tracks
- **Total XP Available:** 10,250 XP (main quests only)
- **Difficulty Range:** ⭐ to ⭐⭐⭐⭐⭐
