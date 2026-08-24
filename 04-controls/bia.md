# Business Impact Analysis

This qualitative BIA covers the most critical processes and systems described in the ClinicCloud design. Ratings use Low, Medium, High, and Severe; no monetary values are invented. MTD, RTO, and RPO are planning assumptions for design approval and must be validated by Clinical Directors, the COO, and the vendor.

| Process / system | Criticality | Financial impact | Operational impact | Reputational impact | Legal / regulatory impact | MTD | RTO | RPO | Dependencies |
|---|---|---|---|---|---|---|---|---|---|
| ClinicCloud EHR and patient-record access | Mission-Critical | High | Severe | Severe | Severe | Hours | Hours | Near-zero for newly recorded clinical data | Clinic laptops, internet, vendor-hosted SaaS tenant/data repository, identity service, backup storage |
| Appointment scheduling and reminders | Important | Medium | High | High | Medium | Hours | Same business day | Same day | ClinicCloud SaaS tenant, public internet, SMS/email reminder service |
| Claims and billing submission | Important | High | High | High | High | 1–2 days | 1 business day | Same day | ClinicCloud, billing clearinghouse API, billing team |
| Patient-record migration and reconciliation | Mission-Critical during cutover | High | Severe | High | Severe | Hours during cutover | Same day with rollback | Last validated export | Legacy systems, CSV files, shared migration folder, vendor migration team, ClinicCloud import pipeline |
| Identity, access review, and audit monitoring | Important | Medium | High | High | Severe | Hours for suspected compromise | Hours for containment | Near-zero for security events | Vendor identity store, ClinicCloud audit logs, MedCore control owner, incident-response contacts |

## Rationale and constraints

ClinicCloud access is mission-critical because all 14 clinics are designed to rely on one cloud EHR for patient histories and centrally scheduled care. The resource pack states that nightly backup is planned, but it does not specify encryption, region, restore testing, or recovery objectives; therefore the BIA treats recovery as a dependency to be validated, not an achieved capability. The migration process receives a near-zero RPO only after a validated export and reconciliation checkpoint exists; until then, the risk remains open under R-006 and R-016.

## BIA sign-off

The Control Owner / Auditor confirms that the four impact dimensions, criticality tiers, and recovery objectives are consistent with the architecture and with the risk register. This sign-off is conditional: the objectives are qualitative planning values, and the organization must validate them through vendor commitments, downtime exercises, and restore tests before go-live.
