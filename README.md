# Aspiritech Academy - Cybersecurity Training Projects

**Author:** Tyler Arend  
**Program:** Aspiritech Cybersecurity Training  
**Date:** September 2026

## Overview

This repository contains four hands-on cybersecurity projects completed as part of my training program with Aspiritech. Each project simulates real-world tasks that security analysts perform in professional environments, including threat intelligence gathering, vulnerability assessment, incident response planning, and risk management.

These documents demonstrate practical application of Security+ concepts, industry-standard frameworks (NIST 800-61, MITRE ATT&CK), and quantitative risk analysis methodologies.

---

## Technologies & Frameworks Used

| Category | Tools/Frameworks |
|----------|------------------|
| Threat Intelligence | MITRE ATT&CK, Wikipedia, CrowdStrike |
| Vulnerability Scanning | TryHackMe, Nmap |
| Incident Response | NIST 800-61 Framework |
| Risk Management | SLE/ARO/ALE Calculations |
| Documentation | Microsoft Word, Markdown |

---

## Certifications Alignment

These projects align with CompTIA Security+ exam objectives, specifically:

- **Threats, Attacks, and Vulnerabilities** — Understanding threat actors, attack vectors, and vulnerability identification
- **Architecture and Design** — Secure architecture, network segmentation, defense in depth
- **Implementation** — Identity management, cryptography, secure protocols
- **Operations and Incident Response** — NIST framework, forensic procedures, recovery strategies
- **Governance, Risk, and Compliance** — Risk assessment, treatment strategies, compliance requirements

---

## Notes on Formatting

In each document, **my original written analysis appears in red text**, while the project template structure is in black. This formatting allows readers to distinguish between provided instructions and my independent contributions.

---

## License

All projects created for Aspiritech cybersecurity training program. Intended for portfolio and educational purposes only.

---

## Projects

### 1. Threat Intelligence Brief — Anonymous Hacker Group

**Objective:** Research a real-world threat actor and document findings in a professional analyst format.

**Scope:**
- Identified Anonymous as an international hacktivist collective active since ~2003-2008
- Documented motivations (political activism, disruption, ideological beliefs)
- Mapped attack methods using MITRE ATT&CK framework (DDoS, SQL injection, botnets)
- Analyzed notable incident: Project Chanology (2008) against Church of Scientology
- Assessed sophistication level as **Moderate (3/5)** due to decentralized structure and varying skill levels

**Key Learnings:**
- Understanding the difference between hacktivism and financially-motivated cybercrime
- Applying MITRE ATT&CK to categorize threat actor techniques
- Evaluating threat actor sophistication beyond technical capabilities
- Recognizing social engineering as a primary attack vector for decentralized groups

**Sources:**
- <a href="https://en.wikipedia.org/wiki/Anonymous_(hacker_group)">Anonymous (Hacker Group)</a>
- <a href="https://www.crowdstrike.com/en-au/cybersecurity-101/threat-intelligence/hacktivism/">What is Hacktivism? | CrowdStrike</a>
- <a href="https://content.time.com/time/specials/packages/article/0,28804,2111975_2111976_2112122,00.html">Anonymous - 2012 TIME 100: The Most Influential People in the World - TIME</a>

---

### 2. Vulnerability Assessment Report — TryHackMe Lab

**Objective:** Use TryHackMe's browser-based platform to scan a target system and document vulnerabilities.

**Lab Details:**
- Platform: TryHackMe (Room: Vulnversity)
- Target IP: 10.67.150.195
- Scanning Tool: Nmap (`nmap -sV`)

**Findings Documented:**
| Finding | Port/Service | Severity | Vulnerability Description | Recommended Fix |
|---------|--------------|----------|---------------------------|-----------------|
| #1 | 22 (SSH) | Medium | Remote access server vulnerable to weak credentials | Strong passwords, monitor access, change default port |
| #2 | 3128 (HTTP-Proxy) | High | Squid proxy caching unencrypted data | Enable encryption, keep systems patched |
| #3 | 3333 (HTTP) | High | Network Caller ID service transmits unencrypted data | Patching, enable SSH/VPN encryption |

**Executive Summary:** Created leadership-friendly summary explaining risks in plain language, prioritizing encryption, port configuration changes, and employee training.

**Key Learnings:**
- Hands-on experience with network reconnaissance and port scanning
- Differentiating between low, medium, high, and critical severity findings
- Translating technical findings for non-technical stakeholders
- Practical application of vulnerability management lifecycle

---

### 3. Incident Response Plan — Ransomware at Riverdale Community Hospital

**Objective:** Work through a ransomware attack scenario using the NIST 800-61 Incident Response framework (6 steps).

**Scenario:** Hospital ransomware attack affecting patient files, radiology imaging systems, and billing systems with a $500,000 Bitcoin demand.

**Framework Applied:**
| NIST Phase | Key Actions Taken |
|------------|------------------|
| Preparation | Assessed existing IR policy, backup policy, disaster recovery plan, SIEM, IDS/IPS deployment |
| Detection & Analysis | Identified IoCs (ransom messages, locked files, SIEM alerts), determined Critical severity |
| Containment | Short-term: Isolate infected machines. Long-term: Network segmentation, credential resets |
| Eradication | Malware removal, registry cleanup, reimaging, password resets for all accounts |
| Recovery | Cloud backup restoration prioritization (patient care → front desk → billing) |
| Lessons Learned | Identified gaps in backups, SIEM-only detection, staff training |

**Ethical Decision:** Analyzed the complex question of whether to pay ransom in healthcare context, weighing patient safety against the uncertainty of attacker cooperation.

**Key Learnings:**
- Applying NIST 800-61 systematically to a high-stakes scenario
- Balancing containment actions with patient safety requirements
- Identifying stakeholders for breach notification (law enforcement, patients, insurers, attorneys)
- Understanding the distinction between containment and eradication phases

---

### 4. Risk Assessment & Register — PixelShop E-Commerce Company

**Objective:** Calculate quantitative risk metrics (SLE, ARO, ALE) and recommend treatment strategies for 5 security risks.

**Company Profile:** Mid-sized e-commerce retailer, $5M annual revenue, 45 employees, customer database with 200,000 records.

**Risk Register Summary:**
| Risk | Asset Value | Exposure Factor | SLE | ARO | ALE | Treatment |
|------|-------------|-----------------|-----|-----|-----|-----------|
| Phishing → Ransomware | $90,000 | 0.50 | $45,000 | 3.0 | $135,000 | Mitigate/Transfer |
| SQL Injection Data Breach | $400,000 | 0.30 | $120,000 | 0.5 | $60,000 | Avoid/Mitigate |
| Web Server DDoS Outage | $80,000 | 1.0 | $80,000 | 0.5 | $40,000 | Mitigate/Accept |
| Insider Threat Leak | $150,000 | 0.20 | $30,000 | 0.1 | $3,000 | Mitigate/Transfer |
| Payment API Breach | $200,000 | 0.75 | $150,000 | 0.5 | $75,000 | Avoid/Mitigate |

**Total Combined ALE:** $313,000 annually

**Analysis:**
- Highest ALE risk: Phishing attacks ($135,000/year) — indicates need for employee security awareness training
- Developed business case for risk treatment decisions based on cost-benefit analysis
- Evaluated residual risks that remain after implementing controls

**Key Learnings:**
- Quantitative risk calculation using industry-standard formulas
- Connecting financial impact to security investment decisions
- Understanding when to avoid, transfer, mitigate, or accept risks
- Creating executive summaries for leadership decision-making
