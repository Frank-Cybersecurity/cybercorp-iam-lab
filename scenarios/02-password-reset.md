# Delegated password reset and privilege boundary

## Objective
Delegate ordinary-user password resets without granting Help Desk the same authority over the privileged administrator.

## Recovered sequence
1. Evidence 16 records the reset delegation ACL on the Users OU.
2. Evidence 17 identifies Jordan Lee (`jlee`) and the Help Desk role.
3. Evidence 18 captures the reset operation for Elena Garcia (`egarcia`).
4. Evidence 19 captures Event 4724 with the operator and target identities.
5. Evidence 20A–20B records the effective-access subject and shows Reset password not allowed for the privileged-account boundary.
6. Evidence 21–23 records the forced-change flag, prompt and post-reset identity.
7. Evidence 24 captures Event 4723 for the employee password change.

[Open the evidence index](../docs/evidence-index.md).

The effective-access screenshot is an ACL evaluation. It should not be described as a captured live failed reset command unless a separate execution record is added. A mock identity-verification ticket is a suggested exercise in the study brief; no completed ticket was recovered here.
