# EP-001: Excessive contractor access

## Objective
Identify and remove a role assignment outside a contractor's approved baseline, retaining before-and-after membership and audit evidence.

## Baseline and finding
The governance register identifies Taylor Brooks (`tbrooks`) as the contractor, with `GG_Contractors` as the approved business-role group. `Domain Users` is also visible in the baseline capture. The exercise temporarily added `GG_Finance_Users`, creating a group path toward `DL_Finance_Data_RW` outside that baseline.

## Evidence sequence

| Step | Capture | What it supports |
| --- | --- | --- |
| Baseline | 31 | Contractor memberships before the change |
| Detect | 32 | Finance membership appears alongside the contractor role |
| Audit addition | 33 | Event 4728 capture records the group addition |
| Remediate | 34 | Removal and a subsequent membership listing |
| Audit removal | 35 | Event 4729 capture records removal |

See [the index](../docs/evidence-index.md) for direct image links.

## Outcome and limits
The workbook marks EP-001 closed: the inappropriate Finance role was removed and the contractor baseline restored. The evidence supports membership remediation. It does not establish that Finance files were accessed or exfiltrated, or that a fresh-session file-access denial test was performed.

The register reviewed October 7 lists the contractor expiration as September 14, 2026. Do not confuse the later lifecycle status with the state at every earlier screenshot. Expiration is not the same as disabling an account, and a historical capture does not establish today's live state.

## Operational takeaway
A defensible access review links the approved role, actual membership, discrepancy, remediation, and validation. For a future rerun, record the request/review identifier, exact timestamps, native event exports, and a fresh-session resource-access test.
