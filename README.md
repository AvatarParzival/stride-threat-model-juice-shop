# stride-threat-model-juice-shop

> **ZeroDay Reapers | GRC Internship — Week 04**

A structured threat modeling and live validation exercise conducted against **OWASP Juice Shop** (v17.x), deployed as a Docker container on an Ubuntu 22.04 VM. The engagement applies STRIDE classification, DREAD risk scoring, OWASP Top 10 alignment, and MITRE ATT&CK mapping to produce a full remediation backlog.

---

## Overview

| Field | Detail |
|---|---|
| Task ID | ZDR-W4-GRC-24GB |
| Assessment Type | Threats to Backlog — STRIDE Threat Modeling, Live Validation & Structured Remediation Planning |
| Platform | Docker Container on BUN VM (Ubuntu 22.04) |
| Target Application | OWASP Juice Shop v17.x |
| Endpoint | `http://127.0.0.1:3000` — IP: `192.168.136.131` |
| Prepared By | Abdullah Zubair |
| Report Date | 14 September 2026 |

---

## Key Findings

| Metric | Value |
|---|---|
| Total STRIDE Threats Identified | 12 |
| Critical (DREAD ≥ 8.0) | 4 |
| High (DREAD 6.0–7.9) | 7 |
| Medium (DREAD 4.0–5.9) | 1 |
| Threats Validated Live | 6 of 6 (100%) |
| Remediation Backlog Items | 12 (REM-01 to REM-12) |
| Total Estimated Remediation Effort | 35 developer-days |
| OWASP Top 10 Categories Covered | 6 |
| MITRE ATT&CK Tactics Mapped | 5 |
| CWE Identifiers Assigned | 12 |

Most critical finding: **THR-01 — SQL Injection Authentication Bypass** (DREAD 9.0).

---

## Methodology

1. **Environment Setup** — Docker-based OWASP Juice Shop deployment on BUN VM
2. **Data Flow Diagram (DFD)** — Modeled with OWASP Threat Dragon
3. **STRIDE Threat Register** — 12 threats classified across all 6 STRIDE categories
4. **DREAD Risk Scoring** — Quantitative scoring for prioritization
5. **Live Threat Validation** — 6 of 6 threats confirmed with photographic evidence (EV-14–EV-19)
6. **Remediation Backlog** — 12 items organized into 3 sprints
7. **Risk Treatment Decisions** — Accept / Mitigate / Transfer per item

---

## Sprint Plan Summary

| Sprint | Focus | Items | Timeline |
|---|---|---|---|
| Sprint 1 | Critical Risks | 4 | Weeks 1–4 |
| Sprint 2 | High Risks | 4 | Weeks 5–8 |
| Sprint 3 | Defence in Depth | 4 | Weeks 9–12 |

---

## Validated Vulnerabilities

| ID | Title | DREAD |
|---|---|---|
| THR-01 | SQL Injection — Authentication Bypass | 9.0 |
| THR-02 | Detailed Error Disclosure | — |
| THR-03 | Missing Content Security Policy (CSP) | — |
| THR-04 | IDOR — Basket Access | — |
| THR-06 | DOM-based XSS | — |
| THR-08 | No Rate Limiting | — |

---

## Repository Contents

```
├── ZRD_Week4_GRC_Report.pdf        # Full GRC report
├── Diagram.png                     # Architecture / DFD diagram
└── Screenshots                     # Evidence screenshots

```

---

## Tools & Frameworks Used

- **OWASP Juice Shop** — Target application
- **OWASP Threat Dragon** — Threat model diagramming
- **Docker** — Container deployment
- **STRIDE** — Threat classification
- **DREAD** — Risk scoring
- **MITRE ATT&CK for Enterprise** — Tactic mapping
- **OWASP Top 10** — Vulnerability alignment

---

## Author

**Abdullah Zubair**
- GitHub: [@AvatarParzival](https://github.com/AvatarParzival)
- LinkedIn: [Abdullah Zubair](https://www.linkedin.com/in/abdullahzubairr)
- Email: [abdullah69zubair@gmail.com](mailto:abdullah69zubair@gmail.com)
