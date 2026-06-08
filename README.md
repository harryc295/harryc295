# Harry Corcoran
### Cybersecurity Student — First-Class Predicted | England, UK

> BSc (Hons) Cybersecurity | Active Directory · Penetration Testing · Malware Analysis · DevSecOps  
> Seeking SOC Analyst or Red Team roles — open to graduate positions, placements, and collaborations.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/harrycorcoran-cybersecurity)
[![GitHub](https://img.shields.io/badge/GitHub-harryc295-181717?style=flat-square&logo=github)](https://github.com/harryc295)

---

## Contents

- [About](#about)
- [Projects](#projects)
- [Skills](#skills)
- [What I'm Looking For](#what-im-looking-for)

---

## About

I'm a final-year cybersecurity student who builds things rather than just studies them. My lab work covers enterprise Active Directory engineering, offensive Python tooling, low-level binary analysis, and DevSecOps automation. Most of what's here started as coursework and grew into something I actually care about finishing properly.

Currently working toward landing a cybersecurity role after graduation. I'm equally comfortable on the red and blue side — I find the overlap between the two (understanding attacks to build better defences) is where the most interesting problems live.

---

## Projects

### BarmBuzz — Enterprise Active Directory Lab
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)

A two-domain Active Directory forest built from scratch to simulate a real enterprise environment, including cross-domain trust boundaries, delegated administration, and policy enforcement.

**What was built:**
- Root domain `bolton.local` with child domain `derby.bolton.local` and a Nottingham OU nested inside Derby
- Windows Server 2022 domain controllers, Windows 11 Pro client, and Ubuntu Desktop joined via `realmd`/`SSSD`
- Role-based access control via security groups with a confidential SMB share proving cross-domain access boundaries
- Group policies on the Nottingham OU restricting Control Panel and disabling Command Prompt — each with a documented risk rationale
- 12 Pester tests for automated validation, plus full dcdiag health checks and screenshot evidence

The project is built with PowerShell DSC so the environment is repeatable from configuration files rather than manual steps. A complete runbook, GPO backups, and evidence folder are included.

**Repo:** [github.com/harryc295/BarmBuzz](https://github.com/harryc295/BarmBuzz)

---

### COM5413 Security Portfolio — The Benji Protocol
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

A four-tool offensive security toolkit built incrementally across a five-week assessed module, culminating in a live-environment mission. Everything runs from the command line — no manual input, fully automatable.

| Tool | Script | What it does |
|---|---|---|
| Evidence Collector | `log_parser.py` | Parses `auth.log` for failed SSH/login attempts, outputs CSV |
| Network Cartographer | `scan.py` | Multi-threaded TCP port scanner with banner grabbing |
| Access Validator | `brute.py` | Targeted SSH/FTP credential tester with mandatory delay |
| Web Enumerator | `web_enum.py` | HTTP recon, header analysis, path enumeration, comment scraping |

Each week's work is tagged in the repo (`w1`–`w4`, then `hunt-final`). Exploit and remediation scripts are included for five vulnerability classes: command injection, LFI, FTP brute force, SSH remote execution, and sensitive file exposure. An AI usage log is maintained throughout per university academic integrity policy.

**Repo:** [github.com/harryc295/COM5413_Security_Portfolio](https://github.com/harryc295/COM5413_Security_Portfolio)

---

### Binary Slammer — Binary Analysis Tool
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Language](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

A low-level binary analysis and manipulation tool written in C++ with a C component. Built with CMake, dependency-managed via vcpkg, and wired up with GitHub Actions for CI. Currently in active development.

**Repo:** [github.com/harryc295/Binary-slammer](https://github.com/harryc295/Binary-slammer)

---

### DevSecOps n8n Workflow Platform
![Status](https://img.shields.io/badge/status-planning-blue?style=flat-square)

An automation platform built around n8n to integrate DevSecOps pipelines — covering automated security alerting, CI/CD pipeline hooks, and vulnerability triage workflows. Repository initialised, architecture in progress.

**Repo:** [github.com/harryc295/devsecops-n8n-workflow-platform](https://github.com/harryc295/devsecops-n8n-workflow-platform)

---

## Skills

**Languages:** Python · PowerShell · C · C++ · Bash · C# · Assembly

**Security:** Active Directory · Penetration Testing · Malware Analysis · Threat Intelligence · OSINT · Splunk · Kali Linux

**Infrastructure:** Windows Server 2022 · Ubuntu · VMware · Cisco · DNS · DHCP · SMB · SSH · FTP

**Tooling:** Git · GitHub Actions · CMake · vcpkg · SQLite · .NET · Figma · Blender · GIMP · After Effects

---

## GitHub Stats

![Harry's GitHub Stats](https://github-readme-stats.shion.dev/api?username=harryc295&theme=bear&hide_border=false&include_all_commits=false&count_private=true)
![Top Languages](https://github-readme-stats.shion.dev/api/top-langs/?username=harryc295&theme=bear&hide_border=false&include_all_commits=false&count_private=true&layout=compact)

---

## What I'm Looking For

I'm finishing my degree and actively looking for my first professional cybersecurity role — SOC Analyst, Junior Penetration Tester, or anything on the offensive/defensive boundary. I bring real lab experience rather than just theoretical knowledge, and I'm the kind of person who builds the thing to understand it.

If you're hiring, mentoring, or working on something interesting in this space — reach out on [LinkedIn](https://linkedin.com/in/harrycorcoran-cybersecurity).
