# Capstone 01: Healthcare Security Posture Assessment

## Project Title & Objective
A security posture assessment for AITEE Community Health Center, a fictional 50-person healthcare provider. The objective was to identify critical assets, map realistic threats and vulnerabilities, define and prioritize risk, and recommend controls a small IT team could actually implement, then write it all up the way you'd hand it to non-technical leadership.

This is a theoretical, scenario-based exercise. No real host, hospital system, or live network was scanned, probed, or tested at any point.

**Role:** Junior Cybersecurity Analyst
**Client:** AITEE Community Health Center (fictional)
**Focus:** Asset, Threat & Risk Analysis

## Key Audit Findings
Three of the eight weaknesses the baseline audit turned up stood out as the ones doing the most damage:

1. **No MFA on critical or admin systems** — combined with weak, reused passwords, this meant one phished credential was enough to reach the EHR.
2. **Unencrypted patient data on shared network drives** — with excessive access permissions on top, far more people (and attackers) could read it than should ever have been able to.
3. **Untested backups** — backups existed, but restoration was never verified, so a ransomware hit would have met almost no real safety net.

## Top Prioritized Risks
| # | Risk | Priority |
|---|------|----------|
| 1 | Phishing + no MFA leading to direct EHR compromise | CRITICAL |
| 2 | Ransomware via unpatched systems, worsened by untested backups | CRITICAL |
| 3 | Unencrypted shared-drive data exposed via device theft or network access | HIGH |

Full reasoning, the complete asset/threat/vulnerability/risk tables, and the executive summary are in the assessment PDF.

## Actionable Recommendations
- Enforce MFA on every admin and clinical account, and run real phishing simulation training (not a slideshow).
- Put a formal patch management cadence in place and actually test backup restoration on a schedule.
- Encrypt data at rest on shared drives and lock down access by role.
- Full-disk encryption + remote wipe on every laptop and mobile device.
- Segment the guest Wi-Fi from the staff and clinical network so a compromised guest device can't reach anything that matters.

## Key Skills Demonstrated
Risk Management · Security Governance · Threat Modeling · Control Selection & Mapping · Executive Communication · HIPAA-Aware Risk Framing

## Repository Structure
```
capstone-01-healthcare-security/
├── README.md
├── healthcare-security-posture-assessment.pdf
└── evidence/
    ├── asset-inventory.csv
    └── risk-matrix-notes.txt
```

## Deliverables
- **[healthcare-security-posture-assessment.pdf](./healthcare-security-posture-assessment.pdf)** — full assessment: assets, threats, vulnerabilities, risks, prioritization, controls, and executive summary.
- **[Evidence/asset-inventory.csv](./Evidence/asset-inventory.csv)** — structured asset list with CIA impact notes.
- **[Evidence/risk-matrix-notes.txt](./Evidence/risk-matrix-notes.txt)** — working notes on how likelihood and impact were scored for prioritization.
