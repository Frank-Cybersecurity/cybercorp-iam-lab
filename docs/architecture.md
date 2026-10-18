# Architecture and scope

| Component | Recovered evidence |
| --- | --- |
| Virtualization | VirtualBox, identified in screenshots and the study brief |
| Domain | `corp.cyberlab.test` |
| NetBIOS name | `CORP` |
| Domain controller | `ATL-DC01`, Windows Server 2022 |
| Workstation | `ATL-W11-01`, Windows 11 |
| Directory layout | CORP OUs for admins, disabled objects, groups, servers, service accounts, users and workstations |
| Role design | Accounts → global role groups → domain-local resource groups → permissions (AGDLP) |

The governance workbook describes eight identities: a privileged administrator, five employee identities, a service account and a contractor. Its role matrix records Finance, HR, Help Desk, Security and audit-export mappings, plus the contractor default-deny baseline.

Group nesting is evidence of an authorization path. It does not alone prove a file share exists, its ACL is enforced, or a user successfully accessed its contents. The Help Desk workstation local-administrator mapping is explicitly pending GPO enforcement in the workbook.

Supplemental screenshots with `corp.lab` in their filename are retained as historical material. They must not be assumed to describe the current domain without inspecting their content.
