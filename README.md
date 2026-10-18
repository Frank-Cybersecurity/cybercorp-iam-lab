# CyberCorp IAM Lab

**Frank Andriulli III | Active Directory identity and access management portfolio**

CyberCorp is an enterprise-style home lab for practicing identity administration, least privilege, access governance, troubleshooting, and evidence collection. These are lab exercises, not production client deployments.

## Start here

- [Evidence index](docs/evidence-index.md): original screenshots, grouped by topic.
- [Excessive-access case study](scenarios/01-excessive-access.md): contractor entitlement review and remediation.
- [Delegated password reset](scenarios/02-password-reset.md): authorized reset and privileged-account boundary.
- [Architecture and scope](docs/architecture.md).
- [Current status and evidence limitations](docs/status-and-gaps.md).
- [Governance register](governance/Cybercorp_Phase_3_IAM_Governance_Register.xlsx): identity inventory, access matrix, and review record.

## Demonstrated work

| Area | Evidence | Scope |
| --- | --- | --- |
| AD DS and DNS | 01–08 | Services, DNS troubleshooting, shares, FSMO and Global Catalog |
| Domain-joined workstation | 10–13 | DNS discovery, secure channel, computer object and OU placement |
| Roles and delegation | 14–24 | Group nesting, admin separation, scoped password reset and audit events |
| Service identity | 25A–27 | Event Log Readers authorization, account restrictions, denied workstation sign-in |
| Access review | 28–35 | Identity and role baseline, excessive membership, removal and audit trail |
| Privileged identity protection | 36–40 | Protected Users baseline/enrollment, Kerberos ticket and AD lookup captures |

File labels summarize the capture subject. They do not establish that every command succeeded or that all resource permissions were tested. See the evidence limitations before interpreting results.

## Repository contents

`docs/` contains the inventory and status notes; `scenarios/` contains case studies; `evidence/` contains the recovered screenshots; `governance/` holds the original workbook; `learning/` holds the study brief; `templates/` provides a future lab write-up template.

Prepared on October 18, 2026 from the recoverable CyberCorp files. Original screenshot bytes and workbook content are preserved. New Markdown explanations were prepared from those sources. No original PowerShell script files or native EVTX exports were recovered.
