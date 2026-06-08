# Harry Corcoran
### Security Engineer & Full-Stack Developer | Bolton, UK

> BSc (Hons) Cybersecurity — First-Class Predicted | Accelerated entry via APL
> Targeting Cloud Security Engineering and long-term Security Architecture / CISO track roles.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/harrycorcoran-cybersecurity)
[![GitHub](https://img.shields.io/badge/GitHub-harryc295-181717?style=flat-square&logo=github)](https://github.com/harryc295)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Cybersecurity%20101-red?style=flat-square&logo=tryhackme&logoColor=white)](https://tryhackme.com)
[![Status](https://img.shields.io/badge/Status-Available%20for%20opportunities-brightgreen?style=flat-square)](mailto:corcoranharry2@gmail.com)
[![Daily AWS Price Tracker](https://github.com/harryc295/Aws-price-tracker-Live-api/actions/workflows/daily-price.yml/badge.svg)](https://github.com/harryc295/Aws-price-tracker-Live-api/actions/workflows/daily-price.yml)

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

Security engineer and full-stack developer finishing a first-class cybersecurity degree, admitted directly into second year via Accredited Prior Learning. I find critical vulnerabilities, build regulated financial platforms, automate cloud infrastructure, and document everything properly.

My work deliberately spans offensive security and cloud/infrastructure engineering — I think the strongest security engineers understand how systems break and build accordingly. Long-term I'm aiming for Cloud Security Engineering, then Security Architecture and CISO level.

---

## Highlights

| | |
|---|---|
| **CVE-2025-49132** | Critical unauthenticated RCE in Pterodactyl Panel — CVSS 9.8 — discovered and responsibly disclosed |
| **269** | Previously undocumented API endpoints enumerated in a single authorised engagement |
| **FCA DISP Platform** | Production internship at Ideal4Finance — NestJS 11 + Next.js 16 regulated complaints platform |
| **Cloud Native** | Kubernetes, Terraform, OpenFaaS, Prometheus/Grafana — deployed on Minikube + K3s edge |
| **AWS FinOps Pipeline** | Live boto3 integration with AWS Pricing API — daily cron via GitHub Actions, credentials via Secrets |
| **13+ Projects** | Across offensive security, cloud, full-stack, infrastructure automation, and malware analysis |

---

## Projects

### 001 — Full-Scope Penetration Test *(Authorised Engagement)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-offensive%20security-red?style=flat-square)

Black-box engagement covering a web application, subdomains, and four cloud-hosted targets. Discovered and responsibly disclosed a critical unauthenticated RCE vulnerability now recorded as a CVE.

- Identified **CVE-2025-49132** — unauthenticated RCE in Pterodactyl Panel, CVSS 9.8, now patched
- Enumerated **269 undocumented API endpoints** on port 8080 using ffuf
- Full OAuth2 security review: redirect_uri bypass, missing state parameter, absent PKCE
- Delivered 18-page executive and technical report with full remediation roadmap

`Burp Suite Pro` `Metasploit` `ffuf` `Nmap` `OAuth2`

---

### 002 — Ideal4Finance — FCA DISP Complaints Platform *(Internship, Present)*
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Type](https://img.shields.io/badge/type-full--stack-blue?style=flat-square)

Core developer on an FCA-regulated financial complaints management platform built from scratch. Full architecture responsibility alongside security implementation and delivery pipeline.

- Monorepo NestJS 11 + Next.js 16 with PostgreSQL and Drizzle ORM
- 16 workflow stages, 32 state transitions across 6 RBAC roles
- SHA-256 evidence integrity hashing and immutable audit log
- Magic-link authentication, BullMQ cron scheduling, Docker Compose deployment
- CI pipeline with npm audit gate and security dependency scanning

`NestJS 11` `Next.js 16` `PostgreSQL` `BullMQ` `Docker` `Drizzle ORM` `TypeScript`

---

### 003 — AWS EC2 Price Tracker — Live API Pipeline
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![AWS](https://img.shields.io/badge/AWS-boto3-FF9900?style=flat-square&logo=amazonaws&logoColor=white)

A two-phase FinOps automation project that evolved from a static proof of concept into a fully live AWS API integration — demonstrating iterative, production-minded cloud engineering.

Phase 1 — Static Foundation (Aws-price-tracker-static): GitOps pipeline architecture built first — scheduled GitHub Actions cron, YAML-driven instance/region configuration, CSV ETL output with timestamps, logging to file and console. Proved the automation layer before touching real APIs.

Phase 2 — Live API Integration (Aws-price-tracker-Live-api): Replaced the static price table with live boto3 calls against the AWS Pricing API. IAM policy scoped to least-privilege (pricing:GetProducts, pricing:DescribeServices). AWS credentials stored as GitHub Secrets. Runs daily at 09:00 UTC, logs real-time EC2 on-demand prices across regions and instance types to timestamped CSV.

Planned extensions: Cost Explorer integration, Slack/email price-change alerts, matplotlib trend charts committed to GitHub Pages.

**Repos:** [Live API](https://github.com/harryc295/Aws-price-tracker-Live-api) · [Static v1](https://github.com/harryc295/Aws-price-tracker-static)

`Python` `boto3` `AWS Pricing API` `GitHub Actions` `IAM` `GitHub Secrets` `FinOps` `ETL`

---

### 004 — ACME Streamly — Cloud Native Platform *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-cloud%20engineering-blueviolet?style=flat-square)

Three-tier application deployed on Kubernetes with full observability, serverless compute, edge simulation, and zero-trust RBAC architecture throughout.

- Multi-stage Dockerfile, Docker Compose with PostgreSQL, health checks, volume and resource limits
- Kubernetes (Minikube) with Deployments, PersistentVolumeClaims, Services, and Network Policies
- Zero-trust security: RBAC + Network Policies enforcing least-privilege access between pods
- Prometheus + Grafana observability stack deployed via Helm with live CPU/memory dashboards
- OpenFaaS serverless functions for compute workloads
- K3s edge simulation — lightweight cluster running in Docker for edge deployment testing
- Full k8s/ manifest directory including default-deny-all and explicit allow rules

`Kubernetes` `Docker` `Terraform` `Prometheus` `Grafana` `OpenFaaS` `K3s` `Helm` `RBAC` `Network Policies`

**Repo:** [github.com/harryc295/COM5408-cloud-project](https://github.com/harryc295/COM5408-cloud-project)

---

### 005 — BarmBuzz — Enterprise Active Directory Lab
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)

Two-domain Active Directory forest simulating an enterprise network with RBAC, cross-platform authentication, automated deployment, and validated security controls.

- Root domain bolton.local / child domain derby.bolton.local / Nottingham OU — demonstrating that domains are security boundaries, OUs are not
- Windows Server 2022 DCs + Ubuntu Desktop joined via realmd/SSSD with full Kerberos authentication
- Fine-Grained Password Policies, RBAC security groups, confidential SMB share proving cross-domain access control
- Group Policy controls with documented risk rationale per control
- PowerShell DSC for fully repeatable automated deployment from config files
- 12 Pester tests for infrastructure validation + dcdiag health checks + full screenshot evidence

`Active Directory` `PowerShell DSC` `Kerberos` `SSSD` `Group Policy` `RBAC` `Fine-Grained Password Policies` `Pester`

**Repo:** [github.com/harryc295/BarmBuzz](https://github.com/harryc295/BarmBuzz)

---

### 006 — AI Security Workflow — n8n + Ollama + Llama 3.2
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-automation-yellow?style=flat-square)

Self-hosted Docker Compose stack combining n8n workflow automation with a local Llama 3.2 model via Ollama. Runs a daily security news digest pipeline — RSS feeds to formatted HTML to Gmail — entirely locally with no data leaving the machine. Local LLM used for workflow generation and summarisation.

`Docker Compose` `n8n` `Ollama` `Llama 3.2` `Redis` `PostgreSQL` `Self-Hosted AI`

---

### 007 — Nessus Vulnerability Pipeline
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Python wrapper for the Nessus REST API automating scan launches, result parsing, and critical vulnerability extraction. Slack webhook integration for real-time alerts and CSV report generation for compliance tracking.

`Python` `Nessus API` `REST` `Slack API` `CSV` `DevSecOps`

---

### 008 — OSINT Threat Intelligence Dashboard
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Threat intelligence aggregator pulling from VirusTotal, Shodan, and AbuseIPDB APIs. Enriches IOCs — IPs, domains, file hashes — with reputation scores, geolocation, and WHOIS data. Outputs structured JSON reports and a live HTML dashboard for rapid triage during incident response.

`Python` `VirusTotal API` `Shodan` `AbuseIPDB` `OSINT` `IOC Enrichment` `Incident Response`

---

### 009 — Binary Hammer — Malware Analysis Tool
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Language](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

Open-source C++ tool for automating repetitive tasks in malware analysis workflows — built to remove manual overhead from binary inspection so analysis time is spent on decisions, not mechanics. Inspired by IDA Pro 9.0 patterns. Full development lifecycle: design, implementation, testing, documentation. Public release pending.

`C++` `CMake` `vcpkg` `GitHub Actions` `Reverse Engineering` `Static Analysis` `Malware Analysis`

**Repo:** [github.com/harryc295/Binary-slammer](https://github.com/harryc295/Binary-slammer)

---

### 010 — Secure Vault — Zero-Knowledge Password Manager
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Python password manager with AES-256 encryption and a zero-knowledge architecture — the application never holds plaintext credentials at rest. Automated credential auditing detects weak or reused passwords across the vault. Published open source.

`Python` `AES-256` `Cryptography` `SQLite` `Zero-Knowledge`

---

### 011 — Benji Protocol — Offensive Security Toolkit *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)

Four-tool CLI security toolkit built across a five-week assessed penetration testing module. Fully headless and automatable via argparse. Week-tagged releases and an AI usage log maintained throughout.

| Tool | Script | What it does |
|---|---|---|
| Evidence Collector | log_parser.py | Parses auth.log for failed SSH/login attempts, outputs CSV |
| Network Cartographer | scan.py | Multi-threaded TCP port scanner with banner grabbing |
| Access Validator | brute.py | Targeted SSH/FTP credential tester with mandatory delay |
| Web Enumerator | web_enum.py | HTTP recon, header analysis, path enumeration, comment scraping |

Exploit and remediation scripts included for five vulnerability classes: command injection, LFI, FTP brute force, SSH remote execution, and sensitive file exposure.

**Repo:** [github.com/harryc295/COM5413_Security_Portfolio](https://github.com/harryc295/COM5413_Security_Portfolio)

---

### 012 — Enterprise WAN Architecture & Zero-Trust Design *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-architecture%20%26%20strategy-blueviolet?style=flat-square)

Designed and evaluated competing WAN architectures (MPLS vs SD-WAN/SASE) for a global multi-site organisation. Implemented Zero-Trust design principles with identity-based access control throughout. Strategic thinking directly relevant to both Cloud Engineer and CISO-track roles.

`SD-WAN` `SASE` `MPLS` `Zero-Trust` `RBAC` `Network Architecture` `Identity-Based Access Control`

---

### 013 — DevSecOps n8n Workflow Platform
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square)

Automation platform built around n8n for integrating DevSecOps pipelines — automated security alerting, CI/CD pipeline hooks, and vulnerability triage workflows. Architecture in progress.

**Repo:** [github.com/harryc295/devsecops-n8n-workflow-platform](https://github.com/harryc295/devsecops-n8n-workflow-platform)

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
Metasploit · Burp Suite Pro · Nmap · Wireshark · Nessus · ffuf · Snort · IDA Pro · BloodHound · Cobalt Strike · Impacket · CrackMapExec · Responder · Ligolo-ng · Maltego · ZAProxy · OpenVAS · Nuclei · Wfuzz · Fail2ban

**Cloud & DevSecOps**
AWS (boto3 · Pricing API · IAM · EC2) · Kubernetes · Terraform · Docker · Prometheus · Grafana · OpenFaaS · K3s · Helm · GitHub Actions · BullMQ · Redis · n8n · Ollama · Nginx

**Infrastructure & Identity**
Active Directory · PowerShell DSC · Group Policy · RBAC · Kerberos · SSSD · Fine-Grained Password Policies · DNS · SMB · Zero-Trust Architecture · MPLS · SD-WAN · SASE · VLANs · VPNs

**Languages**
Python · TypeScript · JavaScript · PowerShell · Bash · C++ · C# · C · MIPS Assembly · SQL

**Full-Stack**
NestJS 11 · Next.js 16 · PostgreSQL · Drizzle ORM · React · REST APIs · OAuth2 · Magic-link Auth · BullMQ

**Security Frameworks & Standards**
OWASP Top 10 · OWASP API Security Top 10 · FCA DISP · Zero-Trust · CVE Research · FinOps

---

## Experience

**Full-Stack Developer — Ideal4Finance** *(2026 — Present · Internship)*
Building an FCA DISP-aligned financial complaints platform from the ground up. Core contributor responsible for architecture, security implementation, and CI pipeline. NestJS 11 + Next.js 16 + PostgreSQL + Docker.

**Penetration Tester — Authorised Client Engagement** *(June 2026)*
Full-scope black-box test across web, subdomains, and four cloud-hosted targets. Discovered CVE-2025-49132 (Critical CVSS 9.8), enumerated 269 undocumented endpoints, full OAuth2 audit. Delivered 18-page executive and technical report with remediation roadmap.

**Kitchen Porter / Bar Back — Lytham House** *(2021 — 2024)*
Three years in a high-pressure hospitality environment. Teamwork, reliability, and communication under pressure.

---

## Education & Certifications

**BSc (Hons) Cybersecurity — First-Class Predicted**
University of Greater Manchester · 2025–Present · Accelerated entry via Accreditation of Prior Learning

**Foundation Degree in Cybersecurity**
University of Greater Manchester · 2024–2025

**A Levels** — Law, Geography, Sociology · Cardinal Newman College · 2022–2024

**GCSEs** — AKS Lytham (Independent)

**Certifications & Training**
- TryHackMe — Cybersecurity 101
- Hack The Box — Security Labs
- PortSwigger Burp Suite Academy — Web Security Training
- OWASP Top 10 & API Security Top 10

---

## GitHub Stats

![Harry's GitHub Stats](https://github-readme-stats.shion.dev/api?username=harryc295&theme=bear&hide_border=false&include_all_commits=false&count_private=true)
![Top Languages](https://github-readme-stats.shion.dev/api/top-langs/?username=harryc295&theme=bear&hide_border=false&include_all_commits=false&count_private=true&layout=compact)

---

## What I'm Building Toward

Near-term I'm targeting Cloud Security Engineering roles — the technical depth is there across AWS, Kubernetes, Terraform, and DevSecOps automation. Long-term the goal is Security Architecture and CISO level, so I'm building strategic thinking and governance understanding alongside the hands-on work.

Currently working on: finishing the degree (first-class), publishing Secure Vault and WAN architecture write-up to GitHub, extending the AWS price tracker toward Cost Explorer and Slack alerting, and working toward AZ-900 / SC-900 as the next credential milestones.

Open to graduate roles, placements, and mentorship — [linkedin.com/in/harrycorcoran-cybersecurity](https://linkedin.com/in/harrycorcoran-cybersecurity) or corcoranharry2@gmail.com.
