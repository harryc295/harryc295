# Harry Corcoran
### Security Engineer & Full-Stack Developer | Bolton, UK

> BSc (Hons) Cybersecurity — First-Class Predicted | Accelerated entry via APL  
> Targeting Cloud Security Engineering and long-term Security Architecture / CISO track roles.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/harrycorcoran-cybersecurity)
[![GitHub](https://img.shields.io/badge/GitHub-harryc295-181717?style=flat-square&logo=github)](https://github.com/harryc295)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Cybersecurity%20101-red?style=flat-square&logo=tryhackme&logoColor=white)](https://tryhackme.com)
[![Status](https://img.shields.io/badge/Status-Available%20for%20opportunities-brightgreen?style=flat-square)](mailto:corcoranharry2@gmail.com)

---

## Contents

- [About](#about)
- [Highlights](#highlights)
- [Projects](#projects)
- [Lab Environment](#lab-environment)
- [Skills & Stack](#skills--stack)
- [Experience](#experience)
- [Education & Certifications](#education--certifications)
- [What I'm Building Toward](#what-im-building-toward)

---

## About

Security engineer and full-stack developer finishing a first-class cybersecurity degree, admitted directly into second year via Accredited Prior Learning. I find critical vulnerabilities, build regulated financial platforms, and automate security workflows end-to-end.

My work sits deliberately across both offensive and engineering tracks — I think the best security engineers understand how things break and build accordingly. Long-term I'm aiming for Cloud Security Engineering, then Security Architecture and CISO level.

---

## Highlights

| | |
|---|---|
| **CVE-2025-49132** | Critical unauthenticated RCE in Pterodactyl Panel — CVSS 9.8 — discovered and responsibly disclosed |
| **269** | Previously undocumented API endpoints enumerated in a single authorised engagement |
| **FCA DISP Platform** | Production internship at Ideal4Finance — NestJS 11 + Next.js 16 regulated complaints platform |
| **Cloud Native** | Kubernetes, Terraform, OpenFaaS, Prometheus/Grafana — deployed on Minikube + K3s edge |
| **11+ Projects** | Shipped across offensive security, infrastructure, full-stack, and malware analysis |

---

## Projects

### 001 — Full-Scope Penetration Test *(Authorised Engagement)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-offensive%20security-red?style=flat-square)

Black-box engagement across a web application, subdomains, and four cloud-hosted targets. Discovered and responsibly disclosed a critical unauthenticated remote code execution vulnerability that was accepted as a CVE.

- Identified **CVE-2025-49132** — unauthenticated RCE in Pterodactyl Panel, CVSS 9.8, now patched
- Enumerated **269 undocumented API endpoints** on port 8080 using ffuf
- Full OAuth2 security review: redirect_uri bypass, missing state parameter, absent PKCE
- Delivered an 18-page executive and technical report with full remediation roadmap

`Burp Suite Pro` `Metasploit` `ffuf` `Nmap` `OAuth2`

---

### 002 — Ideal4Finance — FCA DISP Complaints Platform *(Internship, Present)*
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Type](https://img.shields.io/badge/type-full--stack-blue?style=flat-square)

Core developer on an FCA-regulated financial complaints management platform built from scratch. Full architecture responsibility alongside security implementation and delivery pipeline.

- Monorepo NestJS 11 + Next.js 16 with PostgreSQL and Drizzle ORM
- 16 workflow stages, 32 state transitions, 6 RBAC roles
- SHA-256 evidence integrity hashing and immutable audit log
- Magic-link auth, BullMQ cron scheduling, Docker Compose deployment
- CI pipeline with npm audit gate and security dependency scanning

`NestJS 11` `Next.js 16` `PostgreSQL` `BullMQ` `Docker` `Drizzle ORM` `TypeScript`

---

### 003 — ACME Streamly — Cloud Native Platform *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-cloud%20engineering-blueviolet?style=flat-square)

Three-tier application deployed on Kubernetes with full observability, serverless functions, edge compute, and zero-trust architecture. Exactly the kind of cloud-native work that maps to Cloud Engineer roles.

- Kubernetes (Minikube) with Prometheus/Grafana observability stack
- OpenFaaS serverless functions for compute workloads
- K3s edge deployment for lightweight remote nodes
- Zero-trust RBAC architecture throughout
- Infrastructure provisioned with Terraform

`Kubernetes` `Terraform` `Prometheus` `Grafana` `OpenFaaS` `K3s` `Docker`

**Repo:** [github.com/harryc295/COM5408-cloud-project](https://github.com/harryc295/COM5408-cloud-project)

---

### 004 — BarmBuzz — Enterprise Active Directory Lab
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)

Two-domain Active Directory forest simulating an enterprise network with RBAC, cross-platform authentication, and automated deployment.

- Root domain `bolton.local` / child domain `derby.bolton.local` with Nottingham OU
- Windows Server 2022 DCs + Ubuntu via `realmd`/`SSSD` + Kerberos federation
- Fine-Grained Password Policies, RBAC security groups, SMB share access control
- Group Policy controls with documented risk rationale per control
- PowerShell DSC for fully repeatable automated deployment
- 12 Pester tests for infrastructure validation + dcdiag health checks

`Active Directory` `PowerShell DSC` `Kerberos` `SSSD` `Pester` `Group Policy`

**Repo:** [github.com/harryc295/BarmBuzz](https://github.com/harryc295/BarmBuzz)

---

### 005 — AI Security Workflow — n8n + Ollama
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-automation-yellow?style=flat-square)

Self-hosted Docker Compose stack combining n8n workflow automation with a local Llama 3.2 model via Ollama. Built a daily security news digest pipeline — RSS feeds → processing → formatted HTML → Gmail delivery. Local LLM used for workflow generation and summarisation without sending data to external APIs.

`Docker Compose` `n8n` `Ollama` `Llama 3.2` `Redis` `PostgreSQL`

---

### 006 — Nessus Vulnerability Pipeline
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Python wrapper for the Nessus REST API that automates scan launches, result parsing, and critical vulnerability extraction. Slack webhook integration for real-time alerts and CSV report generation for compliance tracking.

`Python` `Nessus API` `Slack API` `REST` `DevSecOps`

---

### 007 — OSINT Threat Intelligence Dashboard
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Threat intelligence aggregator pulling from VirusTotal, Shodan, and AbuseIPDB APIs. Enriches IOCs — IPs, domains, file hashes — with reputation scores, geolocation, and WHOIS data. Outputs structured JSON reports and a live HTML dashboard for rapid triage during incident response.

`Python` `VirusTotal API` `Shodan` `AbuseIPDB` `OSINT` `IOC Enrichment`

---

### 008 — Binary Hammer — Malware Analysis Tool
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Language](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

Open-source C++ tool for automating repetitive tasks in malware analysis workflows — inspired by IDA Pro patterns. Covers the full development lifecycle: design, implementation, testing, documentation. Public release pending.

`C++` `CMake` `vcpkg` `GitHub Actions` `Reverse Engineering` `Static Analysis`

**Repo:** [github.com/harryc295/Binary-slammer](https://github.com/harryc295/Binary-slammer)

---

### 009 — Secure Vault — Zero-Knowledge Password Manager
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Python password manager with AES-256 encryption and a zero-knowledge architecture — the application never holds plaintext credentials at rest. Automated credential auditing detects weak or reused passwords across the vault.

`Python` `AES-256` `Cryptography` `SQLite`

---

### 010 — Benji Protocol — Offensive Security Toolkit *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Four-tool CLI toolkit built across a five-week assessed penetration testing module. Headless, fully automatable via argparse.

| Tool | What it does |
|---|---|
| Evidence Collector | Parses `auth.log` for failed SSH/login attempts, outputs CSV |
| Network Cartographer | Multi-threaded TCP port scanner with banner grabbing |
| Access Validator | Targeted SSH/FTP credential tester with mandatory delay |
| Web Enumerator | HTTP recon, header analysis, path enumeration, comment scraping |

**Repo:** [github.com/harryc295/COM5413_Security_Portfolio](https://github.com/harryc295/COM5413_Security_Portfolio)

---

### 011 — Enterprise WAN Architecture & Zero-Trust Design *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-architecture%20%26%20strategy-blueviolet?style=flat-square)

Evaluated MPLS vs SD-WAN/SASE architectures for a global organisation. Designed and implemented Zero-Trust principles with identity-based access control across a multi-site network. This project sits on the strategic side — the kind of thinking that feeds directly into Security Architecture and CISO-track roles.

`SD-WAN` `SASE` `MPLS` `Zero-Trust` `RBAC` `Network Architecture`

---

## Lab Environment

Personal cyber range running on VirtualBox — used daily for AD deployment, malware analysis, purple team exercises, and validating attack chains against real defensive controls.

| Machine | OS | Role |
|---|---|---|
| DC-Bolton | Windows Server 2022 | Root domain controller |
| DC-Derby | Windows Server 2022 | Child domain controller |
| WinClient | Windows 11 Pro | Domain-joined workstation |
| LinuxClient | Ubuntu Desktop | Cross-platform auth via SSSD/Kerberos |
| Attack Box | Kali Linux | Penetration testing / red team |
| Analysis VM | Fedora | Isolated malware analysis |

---

## Skills & Stack

**Offensive Security**
Metasploit · Burp Suite Pro · Nmap · Wireshark · Nessus · ffuf · Snort · IDA Pro · BloodHound · Cobalt Strike · Impacket · CrackMapExec · Responder · Ligolo-ng · Maltego · ZAProxy · OpenVAS · Nuclei · Wfuzz

**Infrastructure & Identity**
Active Directory · DSC · Group Policy · RBAC · Kerberos · Fine-Grained Password Policies · DNS · SMB · Zero-Trust Architecture · MPLS · SD-WAN · VLANs · VPNs

**Cloud & DevSecOps**
Kubernetes · Terraform · Docker · Prometheus · Grafana · OpenFaaS · K3s · GitHub Actions · BullMQ · Redis · n8n · Ollama · Nginx

**Languages**
TypeScript · Python · PowerShell · Bash · C++ · C# · C · MIPS Assembly · SQL

**Full-Stack**
NestJS 11 · Next.js 16 · PostgreSQL · Drizzle ORM · React · REST APIs · OAuth2 · Magic-link Auth

**Frameworks & Standards**
OWASP Top 10 · OWASP API Security Top 10 · FCA DISP · Zero-Trust · Pester · CMake · vcpkg

---

## Experience

**Full-Stack Developer — Ideal4Finance** *(2026 — Present, Internship)*
Building an FCA DISP-aligned financial complaints platform from the ground up. Core contributor responsible for architecture, security implementation, and CI pipeline. NestJS 11 + Next.js 16 + PostgreSQL.

**Penetration Tester — Authorised Client Engagement** *(June 2026)*
Full-scope black-box test. Discovered CVE-2025-49132 (Critical, CVSS 9.8), enumerated 269 undocumented endpoints, full OAuth2 audit. Delivered 18-page report with remediation roadmap.

---

## Education & Certifications

**BSc (Hons) Cybersecurity — First-Class Predicted**
University of Greater Manchester · 2025–Present · Accelerated entry via Accreditation of Prior Learning

**Foundation Degree in Cybersecurity**
University of Greater Manchester · 2024–2025

**A Levels** — Law, Geography, Sociology · Cardinal Newman College

**Certifications**
- TryHackMe — Cybersecurity 101
- Hack The Box — Security Labs
- PortSwigger Burp Suite Academy — Web Security
- OWASP Top 10 & API Security Top 10

---

## GitHub Stats

![Harry's GitHub Stats](https://github-readme-stats.shion.dev/api?username=harryc295&theme=bear&hide_border=false&include_all_commits=false&count_private=true)
![Top Languages](https://github-readme-stats.shion.dev/api/top-langs/?username=harryc295&theme=bear&hide_border=false&include_all_commits=false&count_private=true&layout=compact)

---

## What I'm Building Toward

Near-term I'm targeting Cloud Security Engineering — the technical depth is there and the salary ceiling is real. Long-term the goal is Security Architecture and eventually CISO, so I'm building strategic thinking and governance understanding alongside the hands-on work.

Currently working on: finishing the degree (first-class), publishing Secure Vault and the WAN architecture write-up to GitHub, expanding the ACME Streamly cloud project, and working toward AZ-900 / SC-900 as the next credential milestones.

Open to graduate roles, placements, and mentorship — [linkedin.com/in/harrycorcoran-cybersecurity](https://linkedin.com/in/harrycorcoran-cybersecurity) or corcoranharry2@gmail.com.
