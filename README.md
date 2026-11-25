# Web-Application-penetration-testing---Altoro-mutual-
Web Application Penetration Testing project on Altoro Mutual documenting a Reflected XSS vulnerability, PoC, and remediation.


## Overview
This repository documents a web application penetration testing assessment performed on **Altoro Mutual** (`demo.testfire.net`), a simulated online banking application designed for authorized security testing and vulnerability assessment practice.

The objective of this project is to identify security flaws, document reproducible Proofs of Concept (PoCs), evaluate business and technical impact, and provide actionable remediation recommendations.

---

## Scope & Methodology
- **Target Application:** Altoro Mutual (`http://demo.testfire.net`)
- **Testing Type:** Black-Box / Grey-Box Web Application Penetration Testing
- **Reference Standards:** OWASP Web Security Testing Guide (WSTG), OWASP Top 10, CWE
- **Tools Used:** Web Browser DevTools, Burp Suite

---

## Summary of Findings

| ID | Vulnerability | Severity | Status | Report |
| :--- | :--- | :--- | :--- | :--- |
| **VULN-01** | Reflected Cross-Site Scripting (XSS) | Medium | Documented | [View Report](./reports/01-reflected-xss.md) |

---

## Repository Structure
```text
web-app-pentest-altoro-mutual/
├── README.md
├── reports/
│   └── 01-reflected-xss.md
└── evidence/
    └── screenshots/
