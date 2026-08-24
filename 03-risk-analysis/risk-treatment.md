# Risk Treatment Plan

The project uses the four permitted qualitative treatment choices: **Mitigate**, **Transfer**, **Accept**, and **Avoid**. No Critical or High risk is accepted in the design baseline. Transfer items remain MedCore responsibilities for oversight and verification.

| Treatment theme | Risk IDs | Decision | Required outcome |
|---|---|---|---|
| Identity and authorization | R-001, R-003, R-013 | Mitigate | MFA enabled, stronger authentication policy, and clinic-level least privilege tested before go-live. |
| Endpoint and remote support | R-002, R-004, R-012 | Mitigate | Managed endpoint baseline, approved remote tool, MFA, approvals, session recording, and offboarding. |
| Migration data lifecycle | R-005, R-006, R-016 | Mitigate | Restricted CSV handling, chain of custody, reconciliation, dual approval, and secure deletion. |
| Monitoring and response | R-009, R-010 | Mitigate | MedCore receives auditable logs and operates a rehearsed incident/breach process. |
| Suppliers, backups, and integrations | R-007, R-008, R-011 | Transfer plus mitigate | Contractual commitments, assurance review, encryption/region confirmation, minimization, and restore evidence. |
| Availability | R-014 | Mitigate | Downtime procedures, supplier commitments, communications, and recovery testing. |
| Temporary and third-party access | R-015 | Mitigate | Access inventory, expiration, approvals, and owner attestations. |

## Residual-risk rule

The target residual levels in `risk-register.csv` are planning targets after the listed safeguards are implemented and evidenced. They are not current ratings and must be reassessed after design approval, implementation, and control testing.

## Decision log

| Risk IDs | Current level | Treatment | Acceptance authority |
|---|---|---|---|
| R-001, R-002, R-003, R-005 | Critical | Mitigate before go-live | COO after evidence review |
| R-004, R-009, R-011, R-013, R-015 | Critical | Mitigate before go-live | COO after control-owner sign-off |
| R-006, R-007, R-008, R-010, R-012, R-014, R-016 | High | Mitigate or transfer with tracked owner | COO with Compliance Officer |
