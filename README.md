# Harry Corcoran
### Security Engineer & Full-Stack Developer | Bolton, UK

> BSc (Hons) Cybersecurity — First-Class Predicted | Accelerated entry via APL
> Targeting Cloud Security Engineering and long-term Security Architecture / CISO track roles.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/harrycorcoran-cybersecurity)
[![GitHub](https://img.shields.io/badge/GitHub-harryc295-181717?style=flat-square&logo=github)](https://github.com/harryc295)
[![Portfolio](https://img.shields.io/badge/Portfolio-Coming%20Soon-00ff88?style=flat-square&logo=vercel&logoColor=black)](https://github.com/harryc295)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Cybersecurity%20101-red?style=flat-square&logo=tryhackme&logoColor=white)](https://tryhackme.com)
[![HackTheBox](https://img.shields.io/badge/HackTheBox-Labs-9FEF00?style=flat-square&logo=hackthebox&logoColor=black)](https://hackthebox.com)
[![Status](https://img.shields.io/badge/Status-Open%20to%20opportunities-brightgreen?style=flat-square&logo=checkmarx&logoColor=white)](mailto:corcoranharry2@gmail.com)
[![Email](https://img.shields.io/badge/Email-corcoranharry2%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:corcoranharry2@gmail.com)
[![Daily AWS Price Tracker](https://github.com/harryc295/Aws-price-tracker-Live-api/actions/workflows/daily-price.yml/badge.svg)](https://github.com/harryc295/Aws-price-tracker-Live-api/actions/workflows/daily-price.yml)
[![CVE](https://img.shields.io/badge/CVE--2025--49132-CRITICAL%20CVSS%209.8-red?style=flat-square)](https://github.com/harryc295)
[![Degree](https://img.shields.io/badge/BSc%20Cybersecurity-Predicted%201st%20Class-blue?style=flat-square)](https://github.com/harryc295)

---

## Contents

- [About](#about)
- [Highlights](#highlights)
- [Projects](#projects)
- [Lab Environment](#lab-environment)
- [Skills & Stack](#skills--stack)
- [Experience](#experience)
- [Education & Certifications](#education--certifications)
- [GitHub Stats](#github-stats)
- [What I'm Building Toward](#what-im-building-toward)

---

## About

Security engineer and full-stack developer finishing a first-class cybersecurity degree, admitted directly into second year via Accredited Prior Learning. I find critical vulnerabilities, build regulated financial platforms, automate cloud infrastructure, and document everything properly.

My work deliberately spans offensive security and cloud/infrastructure engineering — I think the strongest security engineers understand how systems break and build accordingly. Long-term I'm aiming for Cloud Security Engineering, then Security Architecture and CISO level.

---

## Highlights

| | |
|---|---|
| 🔴 **CVE-2025-49132** | Critical unauthenticated RCE in Pterodactyl Panel — CVSS 9.8 — discovered and responsibly disclosed |
| 🔍 **269** | Previously undocumented API endpoints enumerated in a single authorised engagement |
| 🏦 **FCA DISP Platform** | Production internship at Ideal4Finance — NestJS 11 + Next.js 16 regulated complaints platform |
| ☁️ **Cloud Native** | Kubernetes, Terraform, OpenFaaS, Prometheus/Grafana — deployed on Minikube + K3s edge |
| 🟡 **AWS FinOps Pipeline** | Live boto3 integration with AWS Pricing API — daily cron via GitHub Actions, credentials via Secrets |
| 📦 **13+ Projects** | Across offensive security, cloud, full-stack, infrastructure automation, and malware analysis |

---

## Projects

### 001 — Full-Scope Penetration Test *(Authorised Engagement)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-offensive%20security-red?style=flat-square) ![CVE](https://img.shields.io/badge/CVE--2025--49132-CVSS%209.8-critical?style=flat-square)

Black-box engagement covering a web application, subdomains, and four cloud-hosted targets. Discovered and responsibly disclosed a critical unauthenticated RCE vulnerability now recorded as a CVE.

- Identified **CVE-2025-49132** — unauthenticated RCE in Pterodactyl Panel, CVSS 9.8, now patched
- Enumerated **269 undocumented API endpoints** on port 8080 using ffuf
- Full OAuth2 security review: redirect_uri bypass, missing state parameter, absent PKCE
- Delivered 18-page executive and technical report with full remediation roadmap

`Burp Suite Community` `Metasploit` `ffuf` `Nmap` `OAuth2`

---

### 002 — Ideal4Finance — FCA DISP Complaints Platform *(Internship, Present)*
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Type](https://img.shields.io/badge/type-full--stack-blue?style=flat-square) ![FCA](https://img.shields.io/badge/FCA-DISP%20Regulated-blueviolet?style=flat-square)

Core developer on an FCA-regulated financial complaints management platform built from scratch. Full architecture responsibility alongside security implementation and delivery pipeline.

- Monorepo NestJS 11 + Next.js 16 with PostgreSQL and Drizzle ORM
- 16 workflow stages, 32 state transitions across 6 RBAC roles
- SHA-256 evidence integrity hashing and immutable audit log
- Magic-link authentication, BullMQ cron scheduling, Docker Compose deployment
- CI pipeline with npm audit gate and security dependency scanning

`NestJS 11` `Next.js 16` `PostgreSQL` `BullMQ` `Docker` `Drizzle ORM` `TypeScript`

---

### 003 — AWS EC2 Price Tracker — Live API Pipeline
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![AWS](https://img.shields.io/badge/AWS-boto3-FF9900?style=flat-square&logo=amazonaws&logoColor=white) ![Actions](https://img.shields.io/badge/GitHub%20Actions-daily%20cron-2088FF?style=flat-square&logo=githubactions&logoColor=white)

A two-phase FinOps automation project that evolved from a static proof of concept into a fully live AWS API integration — demonstrating iterative, production-minded cloud engineering.

Phase 1 — Static Foundation (Aws-price-tracker-static): GitOps pipeline architecture built first — scheduled GitHub Actions cron, YAML-driven instance/region configuration, CSV ETL output with timestamps, logging to file and console. Proved the automation layer before touching real APIs.

Phase 2 — Live API Integration (Aws-price-tracker-Live-api): Replaced the static price table with live boto3 calls against the AWS Pricing API. IAM policy scoped to least-privilege (pricing:GetProducts, pricing:DescribeServices). AWS credentials stored as GitHub Secrets. Runs daily at 09:00 UTC, logs real-time EC2 on-demand prices across regions and instance types to timestamped CSV.

Planned extensions: Cost Explorer integration, Slack/email price-change alerts, matplotlib trend charts committed to GitHub Pages.

**Repos:** [Live API](https://github.com/harryc295/Aws-price-tracker-Live-api) · [Static v1](https://github.com/harryc295/Aws-price-tracker-static)

`Python` `boto3` `AWS Pricing API` `GitHub Actions` `IAM` `GitHub Secrets` `FinOps` `ETL`

---

### 004 — ACME Streamly — Cloud Native Platform *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-cloud%20engineering-blueviolet?style=flat-square) ![K8s](https://img.shields.io/badge/Kubernetes-Minikube%20%2B%20K3s-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

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
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white) ![AD](https://img.shields.io/badge/Active%20Directory-Two--Domain%20Forest-0078D4?style=flat-square&logo=windows&logoColor=white)

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
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-automation-yellow?style=flat-square) ![AI](https://img.shields.io/badge/Local%20LLM-Llama%203.2-ff6b35?style=flat-square)

Self-hosted Docker Compose stack combining n8n workflow automation with a local Llama 3.2 model via Ollama. Runs a daily security news digest pipeline — RSS feeds to formatted HTML to Gmail — entirely locally with no data leaving the machine. Local LLM used for workflow generation and summarisation.

`Docker Compose` `n8n` `Ollama` `Llama 3.2` `Redis` `PostgreSQL` `Self-Hosted AI`

---

### 007 — Nessus Vulnerability Pipeline
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![Type](https://img.shields.io/badge/type-devsecops-00b4d8?style=flat-square)

Python wrapper for the Nessus REST API automating scan launches, result parsing, and critical vulnerability extraction. Slack webhook integration for real-time alerts and CSV report generation for compliance tracking.

`Python` `Nessus API` `REST` `Slack API` `CSV` `DevSecOps`

---

### 008 — OSINT Threat Intelligence Dashboard
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![Type](https://img.shields.io/badge/type-threat%20intelligence-8B0000?style=flat-square)

Threat intelligence aggregator pulling from VirusTotal, Shodan, and AbuseIPDB APIs. Enriches IOCs — IPs, domains, file hashes — with reputation scores, geolocation, and WHOIS data. Outputs structured JSON reports and a live HTML dashboard for rapid triage during incident response.

`Python` `VirusTotal API` `Shodan` `AbuseIPDB` `OSINT` `IOC Enrichment` `Incident Response`

---

### 009 — Binary Hammer — Malware Analysis Tool
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Language](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Type](https://img.shields.io/badge/type-malware%20analysis-darkred?style=flat-square)

Open-source C++ tool for automating repetitive tasks in malware analysis workflows — built to remove manual overhead from binary inspection so analysis time is spent on decisions, not mechanics. Inspired by IDA Pro 9.0 patterns. Full development lifecycle: design, implementation, testing, documentation. Public release pending.

`C++` `CMake` `vcpkg` `GitHub Actions` `Reverse Engineering` `Static Analysis` `Malware Analysis`

**Repo:** [github.com/harryc295/Binary-slammer](https://github.com/harryc295/Binary-slammer)

---

### 010 — Secure Vault — Zero-Knowledge Password Manager
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![Crypto](https://img.shields.io/badge/AES--256-Zero%20Knowledge-green?style=flat-square)

Python password manager with AES-256 encryption and a zero-knowledge architecture — the application never holds plaintext credentials at rest. Automated credential auditing detects weak or reused passwords across the vault. Published open source.

`Python` `AES-256` `Cryptography` `SQLite` `Zero-Knowledge`

---

### 011 — Benji Protocol — Offensive Security Toolkit *(Academic)*
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Language](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![Type](https://img.shields.io/badge/type-pentest%20toolkit-red?style=flat-square)

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
![Status](https://img.shields.io/badge/status-complete-brightgreen?style=flat-square) ![Type](https://img.shields.io/badge/type-architecture%20%26%20strategy-blueviolet?style=flat-square) ![ZT](https://img.shields.io/badge/Zero--Trust-SD--WAN%20%2F%20SASE-0066cc?style=flat-square)

Designed and evaluated competing WAN architectures (MPLS vs SD-WAN/SASE) for a global multi-site organisation. Implemented Zero-Trust design principles with identity-based access control throughout. Strategic thinking directly relevant to both Cloud Engineer and CISO-track roles.

`SD-WAN` `SASE` `MPLS` `Zero-Trust` `RBAC` `Network Architecture` `Identity-Based Access Control`

---

### 013 — DevSecOps n8n Workflow Platform
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=flat-square) ![Type](https://img.shields.io/badge/type-devsecops-00b4d8?style=flat-square)

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

### Languages
[![My Skills](https://skillicons.dev/icons?i=python,typescript,javascript,cpp,cs,c,bash,powershell&theme=dark)](https://github.com/harryc295)

![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Assembly](https://img.shields.io/badge/MIPS%20Assembly-grey?style=flat-square&logo=assemblyscript&logoColor=white)

### Cloud & DevSecOps
[![Cloud Skills](https://skillicons.dev/icons?i=aws,kubernetes,docker,terraform,grafana,prometheus,nginx,redis,github&theme=dark)](https://github.com/harryc295)

![AWS](https://img.shields.io/badge/AWS-boto3%20%7C%20IAM%20%7C%20EC2%20%7C%20Pricing%20API-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![OpenFaaS](https://img.shields.io/badge/OpenFaaS-serverless-345DA7?style=flat-square)
![K3s](https://img.shields.io/badge/K3s-edge-FFC61A?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-automation-EA4B71?style=flat-square)
![Ollama](https://img.shields.io/badge/Ollama-Llama%203.2-black?style=flat-square)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-008FBA?style=flat-square&logo=cmake&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05033?style=flat-square&logo=git&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-181717?style=flat-square&logo=gitlab&logoColor=white)

### Full-Stack
[![Full Stack Skills](https://skillicons.dev/icons?i=nestjs,nextjs,react,nodejs,postgres&theme=dark)](https://github.com/harryc295)

![NestJS](https://img.shields.io/badge/NestJS%2011-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js%2016-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=flat-square&logo=sqlite&logoColor=white)
![Drizzle ORM](https://img.shields.io/badge/Drizzle%20ORM-C5F74F?style=flat-square)
![BullMQ](https://img.shields.io/badge/BullMQ-queue%20%26%20jobs-red?style=flat-square)
![.NET](https://img.shields.io/badge/.NET-5C2D91?style=flat-square&logo=.net&logoColor=white)
![OAuth2](https://img.shields.io/badge/OAuth2-magic%20link%20auth-orange?style=flat-square)

### Offensive Security Tools
![Burp Suite Community](https://img.shields.io/badge/Burp%20Suite%20Community-FF6633?style=flat-square&logo=burpsuite&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-2596CD?style=flat-square)
![Nmap](https://img.shields.io/badge/Nmap-0E83CD?style=flat-square)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![Nessus](https://img.shields.io/badge/Nessus-00C176?style=flat-square)
![ffuf](https://img.shields.io/badge/ffuf-web%20fuzzer-red?style=flat-square)
![BloodHound](https://img.shields.io/badge/BloodHound-AD%20attack%20paths-red?style=flat-square)
![Cobalt Strike](https://img.shields.io/badge/Cobalt%20Strike-C2%20framework-darkred?style=flat-square)
![Impacket](https://img.shields.io/badge/Impacket-network%20protocols-blue?style=flat-square)
![CrackMapExec](https://img.shields.io/badge/CrackMapExec-AD%20enum-blue?style=flat-square)
![Responder](https://img.shields.io/badge/Responder-LLMNR%20poisoning-orange?style=flat-square)
![Ligolo-ng](https://img.shields.io/badge/Ligolo--ng-tunneling-purple?style=flat-square)
![IDA Pro](https://img.shields.io/badge/IDA%20Pro-reverse%20engineering-grey?style=flat-square)
![Maltego](https://img.shields.io/badge/Maltego-OSINT-blue?style=flat-square)
![ZAProxy](https://img.shields.io/badge/ZAProxy-web%20scanner-00549E?style=flat-square)
![OpenVAS](https://img.shields.io/badge/OpenVAS-vuln%20scanning-green?style=flat-square)
![Nuclei](https://img.shields.io/badge/Nuclei-templated%20scanning-9933FF?style=flat-square)
![Wfuzz](https://img.shields.io/badge/Wfuzz-web%20fuzzer-red?style=flat-square)
![Snort](https://img.shields.io/badge/Snort-IDS%2FIPS-CC0000?style=flat-square)
![Fail2ban](https://img.shields.io/badge/Fail2ban-brute%20force%20protection-yellow?style=flat-square)
![Splunk](https://img.shields.io/badge/Splunk-SIEM-000000?style=flat-square&logo=splunk&logoColor=white)
![TOR](https://img.shields.io/badge/TOR-anonymity-7E4798?style=flat-square&logo=torproject&logoColor=white)
![Tampermonkey](https://img.shields.io/badge/Tampermonkey-browser%20scripts-00485B?style=flat-square&logo=tampermonkey&logoColor=white)

### Infrastructure & Identity
![Active Directory](https://img.shields.io/badge/Active%20Directory-0078D4?style=flat-square&logo=windows&logoColor=white)
![PowerShell DSC](https://img.shields.io/badge/PowerShell%20DSC-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Kerberos](https://img.shields.io/badge/Kerberos-authentication-CC0000?style=flat-square)
![Group Policy](https://img.shields.io/badge/Group%20Policy-GPO-0078D4?style=flat-square)
![RBAC](https://img.shields.io/badge/RBAC-access%20control-green?style=flat-square)
![SSSD](https://img.shields.io/badge/SSSD-linux%20domain%20join-orange?style=flat-square)
![Zero-Trust](https://img.shields.io/badge/Zero--Trust-architecture-blueviolet?style=flat-square)
![SD-WAN](https://img.shields.io/badge/SD--WAN%20%2F%20SASE-network-blue?style=flat-square)
![MPLS](https://img.shields.io/badge/MPLS-legacy%20WAN-grey?style=flat-square)
![Cisco](https://img.shields.io/badge/Cisco-networking-049fd9?style=flat-square&logo=cisco&logoColor=black)
![DNS](https://img.shields.io/badge/DNS-networking-lightgrey?style=flat-square)
![VPN](https://img.shields.io/badge/VPN%20%2F%20VLAN-segmentation-00b4d8?style=flat-square)

### Operating Systems & Platforms
[![OS Skills](https://skillicons.dev/icons?i=linux,ubuntu,kali,fedora,windows&theme=dark)](https://github.com/harryc295)

![Kali Linux](https://img.shields.io/badge/Kali%20Linux-268BEE?style=flat-square&logo=kalilinux&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Fedora](https://img.shields.io/badge/Fedora-294172?style=flat-square&logo=fedora&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows%20Server%202022-0078D4?style=flat-square&logo=windows&logoColor=white)
![Windows 11](https://img.shields.io/badge/Windows%2011-0078D4?style=flat-square&logo=windows11&logoColor=white)
![Arch Linux](https://img.shields.io/badge/Arch%20Linux-1793D1?style=flat-square&logo=archlinux&logoColor=white)
![XFCE](https://img.shields.io/badge/XFCE-desktop-2284F2?style=flat-square&logo=xfce&logoColor=white)
![Windows Terminal](https://img.shields.io/badge/Windows%20Terminal-4D4D4D?style=flat-square&logo=windowsterminal&logoColor=white)

### Design & Creative
[![Design Skills](https://skillicons.dev/icons?i=figma,blender,ae&theme=dark)](https://github.com/harryc295)

![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white)
![Blender](https://img.shields.io/badge/Blender-F5792A?style=flat-square&logo=blender&logoColor=white)
![GIMP](https://img.shields.io/badge/GIMP-657D8B?style=flat-square&logo=gimp&logoColor=FFFFFF)
![Adobe After Effects](https://img.shields.io/badge/After%20Effects-9999FF?style=flat-square&logo=adobeaftereffects&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-00C4CC?style=flat-square&logo=canva&logoColor=white)

### Security Frameworks & Standards
![OWASP](https://img.shields.io/badge/OWASP%20Top%2010-000000?style=flat-square&logo=owasp&logoColor=white)
![OWASP API](https://img.shields.io/badge/OWASP%20API%20Security%20Top%2010-000000?style=flat-square&logo=owasp&logoColor=white)
![FCA DISP](https://img.shields.io/badge/FCA%20DISP-regulated-blueviolet?style=flat-square)
![Zero-Trust](https://img.shields.io/badge/Zero--Trust%20Architecture-framework-blue?style=flat-square)
![FinOps](https://img.shields.io/badge/FinOps-cloud%20cost%20engineering-FF9900?style=flat-square)
![CVE Research](https://img.shields.io/badge/CVE%20Research-responsible%20disclosure-red?style=flat-square)

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

![THM](https://img.shields.io/badge/TryHackMe-Cybersecurity%20101-red?style=flat-square&logo=tryhackme&logoColor=white)
![HTB](https://img.shields.io/badge/Hack%20The%20Box-Security%20Labs-9FEF00?style=flat-square&logo=hackthebox&logoColor=black)
![PortSwigger](https://img.shields.io/badge/PortSwigger-Burp%20Suite%20Academy-FF6633?style=flat-square&logo=burpsuite&logoColor=white)
![OWASP](https://img.shields.io/badge/OWASP-Top%2010%20%26%20API%20Security-000000?style=flat-square&logo=owasp&logoColor=white)
![AZ900](https://img.shields.io/badge/AZ--900-In%20Progress-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![SC900](https://img.shields.io/badge/SC--900-In%20Progress-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=harryc295&show_icons=true&theme=dark&hide_border=true&include_all_commits=true&count_private=true&bg_color=0d1117&title_color=00ff88&icon_color=00ff88&text_color=d8dde8" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=harryc295&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=00ff88&text_color=d8dde8&langs_count=8" height="165"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=harryc295&theme=dark&hide_border=true&background=0d1117&stroke=00ff88&ring=00ff88&fire=ff4040&currStreakLabel=00ff88&sideLabels=d8dde8&dates=5a6080" height="165"/>
</p>

---

## What I'm Building Toward

Near-term I'm targeting Cloud Security Engineering roles — the technical depth is there across AWS, Kubernetes, Terraform, and DevSecOps automation. Long-term the goal is Security Architecture and CISO level, so I'm building strategic thinking and governance understanding alongside the hands-on work.

Currently working on: finishing the degree (first-class), publishing Secure Vault and WAN architecture write-up to GitHub, extending the AWS price tracker toward Cost Explorer and Slack alerting, and working toward AZ-900 / SC-900 as the next credential milestones.

Open to graduate roles, placements, and mentorship — [linkedin.com/in/harrycorcoran-cybersecurity](https://linkedin.com/in/harrycorcoran-cybersecurity) or corcoranharry2@gmail.com.
