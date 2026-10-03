# Stride Threat Model Juice Shop

[![GRC](https://img.shields.io/badge/Domain-GRC-243B53)](https://en.wikipedia.org/wiki/Governance,_risk_management,_and_compliance)
[![STRIDE](https://img.shields.io/badge/Framework-STRIDE-CC0000)](https://en.wikipedia.org/wiki/STRIDE_(security))
[![OWASP](https://img.shields.io/badge/Target-OWASP%20Juice%20Shop-F7941E)](https://owasp.org/www-project-juice-shop/)
[![MITRE ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK-Enterprise-005A9C)](https://attack.mitre.org/)
[![Docker](https://img.shields.io/badge/Platform-Docker-2496ED)](https://www.docker.com/)

A structured threat modeling and live validation exercise conducted against **OWASP Juice Shop v17.x**, deployed as a Docker container on an Ubuntu 22.04 VM. The engagement applies **STRIDE** threat classification, **DREAD** risk scoring, **OWASP Top 10** alignment, and **MITRE ATT&CK** mapping to produce a full prioritised remediation backlog.

> **Core principle:** a threat was only counted as confirmed when live exploitation produced reproducible, photographic evidence.

## Final Report

📄 **[Read the complete STRIDE Threat Modeling Report](ZRD_Week4_GRC_Report.pdf)**

- **Task ID:** ZDR-W4-GRC-24GB
- **Assessment type:** Threats to Backlog — STRIDE Threat Modeling, Live Validation & Structured Remediation Planning
- **Report date:** 14 September 2026
- **Prepared by:** Abdullah Zubair

## Project Objectives

1. Deploy OWASP Juice Shop v17.x in a controlled Docker environment.
2. Build a Data Flow Diagram (DFD) using OWASP Threat Dragon.
3. Apply STRIDE to produce a complete threat register across all six categories.
4. Score every threat using DREAD for quantitative prioritisation.
5. Validate six selected threats live and capture photographic evidence.
6. Map all threats to OWASP Top 10 categories and MITRE ATT&CK tactics.
7. Produce a sprint-based remediation backlog with ownership and effort estimates.

## Scope and Environment

| Component | Detail |
|---|---|
| Target application | OWASP Juice Shop v17.x |
| Deployment | Docker container |
| Host VM | BUN — Ubuntu 22.04 |
| Endpoint | `http://127.0.0.1:3000` — IP: `192.168.136.131` |
| Threat modeling tool | OWASP Threat Dragon |

### Standards and Guidance

- **STRIDE** — Threat classification
- **DREAD** — Risk scoring
- **OWASP Top 10**
- **MITRE ATT&CK for Enterprise**
- **CWE** — Common Weakness Enumeration

## Key Results

| Metric | Value |
|---|---:|
| Total STRIDE threats identified | 12 |
| Critical (DREAD ≥ 8.0) | 4 |
| High (DREAD 6.0–7.9) | 7 |
| Medium (DREAD 4.0–5.9) | 1 |
| Threats validated live | 6 of 6 (100%) |
| Remediation backlog items | 12 (REM-01 to REM-12) |
| Total estimated remediation effort | 35 developer-days |
| OWASP Top 10 categories covered | 6 |
| MITRE ATT&CK tactics mapped | 5 |
| CWE identifiers assigned | 12 |

## Validated Threats

| ID | Title | DREAD | OWASP Category |
|---|---|---|---|
| THR-01 | SQL Injection — Authentication Bypass | 9.0 | A03: Injection |
| THR-02 | Detailed Error Disclosure | — | A05: Security Misconfiguration |
| THR-03 | Missing Content Security Policy (CSP) | — | A05: Security Misconfiguration |
| THR-04 | IDOR — Basket Access | — | A01: Broken Access Control |
| THR-06 | DOM-based XSS | — | A03: Injection |
| THR-08 | No Rate Limiting | — | A07: Auth Failures |

All six threats were confirmed through live exploitation. Evidence screenshots EV-14 through EV-19 are included in the repository.

## Sprint Plan

| Sprint | Focus | Items | Timeline |
|---|---|---|---|
| Sprint 1 | Critical risks | 4 | Weeks 1–4 |
| Sprint 2 | High risks | 4 | Weeks 5–8 |
| Sprint 3 | Defence in depth | 4 | Weeks 9–12 |

## Repository Structure

```text
.
├── README.md
├── ZRD_Week4_GRC_Report.pdf
├── Diagram.png
└── Screenshots/
```

## Limitations

- The exercise was conducted in an isolated lab environment against an intentionally vulnerable application.
- DREAD scores reflect analyst judgment at the time of assessment and are not independently verified.
- Six of twelve threats were selected for live validation; the remaining six were assessed analytically only.
- Remediation effort estimates are indicative and were not derived from a formal sizing exercise.
- Results should not be generalised to production environments or other applications.

## Lessons Learned

- A threat model without live validation produces assumptions, not findings.
- DREAD scoring is most useful when applied consistently across all threats before prioritisation.
- Docker-based targets reduce environment variability and make evidence collection repeatable.
- SQL injection remains trivially exploitable when parameterised queries are absent.
- Documenting a threat is not the same as understanding its exploitability — execution reveals the difference.

## Author

**Abdullah Zubair**  
Cybersecurity | GRC | Security Automation
- GitHub: [@AvatarParzival](https://github.com/AvatarParzival)
- LinkedIn: [Abdullah Zubair](https://www.linkedin.com/in/abdullahzubairr)
- Email: [abdullah69zubair@gmail.com](mailto:abdullah69zubair@gmail.com)

## Responsible Use

This repository is intended for educational, defensive-security and professional portfolio purposes. The target application is intentionally vulnerable and was deployed in an isolated lab. Do not use the techniques or findings demonstrated here against systems without explicit authorisation.