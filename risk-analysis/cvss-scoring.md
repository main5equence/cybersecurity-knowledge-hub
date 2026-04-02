# CVSS Scoring

## Overview

The Common Vulnerability Scoring System (CVSS) is a standardized framework used to assess the severity of security vulnerabilities.

It provides a numerical score (0–10) that reflects the risk associated with a vulnerability and helps prioritize remediation efforts.

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/d243bded-9189-4101-a986-8d54c69c8b31" />


---

## CVSS Score Range

| Score | Severity |
|------|---------|
| 0.0  | None |
| 0.1 – 3.9 | Low |
| 4.0 – 6.9 | Medium |
| 7.0 – 8.9 | High |
| 9.0 – 10.0 | Critical |

---

## CVSS Components

CVSS is based on three main metric groups:

### 1. Base Metrics
Represent the intrinsic characteristics of a vulnerability.

- Attack Vector (Network, Local, Physical)
- Attack Complexity
- Privileges Required
- User Interaction
- Impact (Confidentiality, Integrity, Availability)

---

### 2. Temporal Metrics
Reflect characteristics that change over time.

- Exploit availability
- Patch availability
- Confidence in the vulnerability report

---

### 3. Environmental Metrics
Customize the score based on a specific organization.

- Asset value
- Security controls in place
- Business impact

---

## How CVSS Works

CVSS combines multiple factors to produce a standardized risk score.

Higher scores indicate higher severity and priority for remediation.

---

## CVSS Scoring Flow

<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/269980db-67ca-4c8c-a4df-a2a2dfe6d5c0" />


---

## Example

A remotely exploitable vulnerability with no authentication required:

Attack Vector: Network
Privileges Required: None
Impact: High

→ CVSS Score: High / Critical

---

## Why CVSS Matters
- Provides a standardized way to evaluate vulnerabilities
- Supports prioritization of remediation
- Enables consistent communication across teams

---

## Key Takeaways
- CVSS scores range from 0 to 10
- Higher scores indicate higher risk
- CVSS combines technical and contextual factors
- It is widely used in vulnerability management

---

## Notes

CVSS is commonly used alongside vulnerability scanners and security tools.

It should be combined with business context for accurate risk prioritization.







