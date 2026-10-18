# Status, provenance and gaps

## What was recovered
- Original evidence archive: 42 PNG files numbered 01–40, with A/B variants and no 09.
- Separate screenshots, including matching copies of 32–35 and additional historical/troubleshooting captures.
- The Phase 3 governance workbook, reviewed October 7, 2026, preserved unchanged.
- The October 9 study brief, preserved unchanged. It explicitly labels its exercises as suggestions, not completed work.
- Byte-identical screenshot copies are consolidated. See `source-file-map.csv` for original-to-repository mappings and SHA256 values.

## Naming reconciliation
| Workbook reference | Recovered archive file |
| --- | --- |
| 19-Audit-4724-Helpdesk-Password-Reset.png | 19-Audit-4724-Helpdesk-Password-Reset(2).png |
| 25-Service-Account-Authorization-Path.png | 25A-Service-Account-Authorization.png and 25B-Service-Account-Nested-Authorization.png |
| 28-Phase1-Identity-Inventory.png | 28-Phase1-Identity-Inventory(2).png |
| 29-Identity-Role-Membership-Baseline.png | Archive has (2); an additional standalone version was also recovered |
| 30-Role-to-Permission-Group-Baseline.png | 30B archive capture; standalone 30 also recovered |
| 31-Contractor-PreReview-Baseline.png | 31-Contractor-Preview-Baseline.png |

Repository filenames replace spaces and parentheses with hyphens; source bytes remain unchanged.

## Interpretation limits
- No screenshot 09 was found in the archive; do not silently renumber the series.
- DNS captures include timeout/troubleshooting output. Capture 05 includes an invalid command attempt followed by a quiet DCDIAG command; it is not a complete verbose health report.
- 30A and supplemental parser-error captures document troubleshooting, not successful permission validation.
- Group paths are not complete end-to-end resource-access tests.
- The workbook records planned workstation local-admin GPO enforcement. No subsequent evidence was recovered establishing completion.
- Protected Users captures 36–40 extend beyond the workbook's index ending at 35; the workbook was not rewritten to imply a new review.
- No source `.ps1` scripts, native EVTX exports, full ticket records, or complete deployment runbook were recovered in this collection.
- Entra ID, Okta, SAML/SCIM integrations and Conditional Access deployment are not established by this evidence set.
- Evidence captures historical lab state, not a live audit on the package preparation date.

## Next evidence to collect
1. Confirm the current lab state and reconcile it with the historical register.
2. Capture workstation GPO application and effective local-group membership when implemented.
3. Test positive and negative resource access in fresh user sessions.
4. Export relevant audit events with timestamps, actor, target and result.
5. Save reusable scripts with inputs, prerequisites and expected outputs.

## Publication review
This package preserves original evidence, including lab usernames, SIDs, private addresses and desktop context. Review each image at full resolution before making the repository public; remove any actual credentials, tokens, recovery codes or unrelated personal information. No screenshot redaction has been performed. Start with a private repository while reviewing.
