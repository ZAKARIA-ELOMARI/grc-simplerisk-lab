```
# 🛡️ Enterprise Cybersecurity Governance, Risk, and Compliance (GRC) Portfolio

[![Standard: ISO/IEC 27001:2022](https://img.shields.io/badge/Standard-ISO%2FIEC_27001%3A2022-blue.svg)](https://www.iso.org/standard/27001)
[![Framework: NIST CSF 2.0](https://img.shields.io/badge/Framework-NIST_CSF_2.0-green.svg)](https://www.nist.gov/cyberframework)
[![Law: Morocco Loi 05-20](https://img.shields.io/badge/Regulation-Morocco_Loi_05--20-red.svg)](https://www.dgssi.gov.ma)
[![Law: Morocco Loi 09-08](https://img.shields.io/badge/Data_Privacy-CNDP_Loi_09--08-orange.svg)](https://www.cndp.ma)
[![Tools: SimpleRisk &amp; Eramba](https://img.shields.io/badge/Tools-SimpleRisk_%7C_Eramba-purple.svg)](#-%EF%B8%8F-tooling--grc-stack)

An enterprise-grade, audit-ready **Governance, Risk, and Compliance (GRC) Portfolio** implementing a full Information Security Management System (ISMS / SGSI) for a Critical Infrastructure / Infrastructure d'Importance Vitale (IIV) under the **Moroccan National Regulatory Framework** and international standards.

---

## 🎯 Project Overview &amp; Objective

This repository serves as a **practical, end-to-end case study** demonstrating how to transition theoretical security governance and legal mandates into operational, audit-proven security controls.

### Core Objectives:
1. **Audit-Readiness**: Build a complete compliance artifact suite suitable for a formal **PASSI** (Prestataire d'Audit de la Sécurité des Systèmes d'Information) audit under **Loi n° 05-20 Article 20**.
2. **Hybrid Regulatory Alignment**: Bridge national mandatory directives (**DNSSI v2**, **Loi n° 05-20**, **Loi n° 09-08**) with global standards (**ISO/IEC 27001:2022**, **NIST CSF 2.0**, **EBIOS RM**).
3. **Automated Risk Management**: Leverage open-source GRC engines (**SimpleRisk Core**, **Eramba**) to track, score, and remediate technical and organizational risks.
4. **Demonstrable Proof**: Apply the ISO 19011 audit principle: **Dire (Policy) ➔ Montrer (Procedure) ➔ Prouver (Evidence)**.

---

## 🏛️ Regulatory &amp; Framework Mapping

| Reference / Standard | Authority / Issuer | Key Application in Portfolio |
| :--- | :--- | :--- |
| **Loi n° 05-20** | DGSSI / ADN (Morocco) | IIV scope, mandatory incident reporting to maCERT (Art. 8), 100% national data hosting (Art. 11), 1-year log retention (Art. 26). |
| **DNSSI v2** | DGSSI (Morocco) | Technical security baseline used as audit criteria (*Critères*) across 11 security domains. |
| **Loi n° 09-08** | CNDP (Morocco) | Personal data protection, express consent (*Opt-in*), CNDP authorization, and data subject rights. |
| **ISO/IEC 27001:2022** | ISO / IEC | ISMS Clauses 4–10 (PDCA Governance) and 93 Annex A controls across 4 themes (Organizational, People, Physical, Tech). |
| **NIST CSF 2.0** | NIST | High-level cybersecurity lifecycle mapping: **Govern, Identify, Protect, Detect, Respond, Recover**. |
| **EBIOS RM** | ANSSI / DGSSI | Risk assessment methodology across 5 strategic workshops (*Ateliers*). |

---

## 📂 Repository Architecture

```text
cybersecurity-grc-portfolio/
├── README.md                           ──► Repository documentation &amp; GRC architecture overview
├── 01-Policies/                        ──► Corporate Information Security Policies (PSSI)
│   ├── Acceptable_Use_Policy.md        ──► User behavior, classification (Art. 5), local hosting (Art. 11)
│   └── Access_Control_Policy.md        ──► IAM, MFA, RBAC, FSSO, mapped to ISO 27001 Control A.5.15 &amp; DNSSI v2
├── 02-Risk-Register/                   ──► Master Risk Management artifacts
│   └── Master_Risk_Register.md         ──► Quantitative &amp; qualitative risk scoring (ISO 31000 / SimpleRisk export)
├── 03-SoA/                             ──► ISO/IEC 27001 Compliance Statement
│   └── Statement_of_Applicability.md   ──► 93 Annex A controls evaluation with justification &amp; DNSSI v2 cross-mapping
├── 04-Audit-Pack/                      ──► Formal Audit Evidence &amp; Verification Pack
│   └── Evidence_Matrix.md              ──► Audit triad mapping (Critères ➔ Preuves ➔ Constats) for PASSI auditors
└── 05-Tool-Exports/                    ──► Open-source GRC software integrations
    ├── simplerisk_export.csv           ──► Raw risk register dump from SimpleRisk Core (Docker)
    └── eramba_compliance_map.json      ──► Security control mappings exported from Eramba Community

```

---

## 🛠️️ Tooling &amp; GRC Stack

* **SimpleRisk Core**: Deployed via Docker (`simplerisk/simplerisk:latest`) for risk assessment, scoring (Impact × Likelihood), and tracking risk mitigation workflows.
* **Eramba (Community Edition)**: Used for mapping enterprise policies to ISO 27001 Annex A controls and tracking compliance gaps.
* **Splunk / Wazuh SIEM**: Source of technical evidence logs proving 1-year log retention compliance under Loi 05-20 Article 26.

---

## 📝 Document Descriptions

### 1\. `01-Policies/`

Contains enforceative security policies written for employees, contractors, and IT administrators. Translates complex legal constraints into actionable operational rules.

### 2\. `02-Risk-Register/`

Maintains the centralized risk inventory. Each entry evaluates threat scenarios (e.g., *Kerberoasting*, *LFI*, *Unpatched Edge Firewalls*), assigns inherent risk ratings, details risk response decisions (Mitigate, Accept, Transfer, Avoid), and calculates residual risk.

### 3\. `03-SoA/`

The mandatory **Statement of Applicability** required by ISO 27001 Clause 6.1.3\. Explicitly states which of the 93 controls are in-scope or excluded, with formal justification and alignment to Moroccan DNSSI v2 rules.

### 4\. `04-Audit-Pack/`

Contains the **Evidence Matrix** designed for internal and external auditors. Mapped to the CCCER structure (Condition, Criteria, Cause, Effect, Recommendation) to streamline compliance verification.

---

## 👤 Maintainer &amp; Context

* **Author**: Zakaria El Omari
* **Academic Program**: Cybersecurity &amp; Digital Trust (S5) — ENSET Mohammedia
* **Certifications &amp; Track**: Fortinet NSE 3 Certified, PJPT Practical Pentesting, ISO 27001 Lead Implementer studies.

---

*This repository is maintained for professional demonstration, audit preparation, and GRC portfolio review.*