# MedCore ClinicCloud Access Control Policy

**Policy owner:** Compliance Officer
**Approver:** Chief Operating Officer
**Version:** 1.0 — Design approval draft
**Status:** Must be approved before go-live

## Purpose

This policy establishes testable rules for protecting patient, billing, appointment, and staff identity data in ClinicCloud. It directly addresses the highest-priority design gaps in R-001, R-003, R-013, and R-015: MFA is not enabled, clinic-level access is not designed, password requirements are not defined, and offboarding is missing.

## Scope

The policy applies to all MedCore staff, clinicians, front-desk users, contractors, vendor migration personnel, and service accounts that access ClinicCloud, the shared migration folder, the billing clearinghouse integration, or the SMS/email reminder service. It applies to all 14 clinics and to access from clinic-owned Windows laptops or approved remote-support sessions.

## Policy statements

1. **MFA required.** Every human account accessing ClinicCloud must use vendor-supported multi-factor authentication before the account is activated. A user without MFA must not access patient data.
2. **Unique identities.** Each staff member and contractor must use an individually assigned account. Shared human accounts are prohibited. Service accounts must have a named owner and documented purpose.
3. **Least privilege.** ClinicCloud permissions must be limited to the user's job function and assigned clinic. A Clinician must not view or modify patients outside the approved care relationship, and Front Desk access must remain limited to scheduling and demographic data.
4. **Access approval.** The manager and Control Owner / Auditor must approve access before activation. The request must record the person, clinic, role, purpose, start date, and expiry date where access is temporary.
5. **Joiner, mover, leaver control.** The manager must notify the Control Owner / Auditor of a joiner, mover, or leaver. Leaver access must be disabled within the approved operational window and no later than the end of the person's final working day. Vendor and migration access must expire automatically at the end of the approved task.
6. **Password protection.** Where a password is used, it must be at least 12 characters, unique to ClinicCloud, screened against known compromised passwords, and protected by rate limiting or lockout. Password reuse and storage in plain text are prohibited.
7. **Endpoint condition.** ClinicCloud access is permitted only from an approved, managed device with supported operating-system patches, screen lock, full-disk encryption, and endpoint protection. The Control Owner / Auditor may block unmanaged devices.
8. **Review and monitoring.** The Control Owner / Auditor must review privileged accounts and a sample of patient-record access at least quarterly. ClinicCloud audit logs must be retained and made available to MedCore for investigation.
9. **Remote support.** Helpdesk remote access must use an approved tool with MFA, ticket approval, time-limited access, session recording, and named contractor identities. Persistent unattended access is prohibited unless specifically approved.
10. **Exceptions.** An exception must document the business reason, affected data, compensating controls, expiry date, and accountable approver. Exceptions affecting restricted PHI require Compliance Officer review and COO approval; no exception may waive incident reporting.

## Roles and responsibilities

The **COO** approves this policy, material exceptions, and go-live risk acceptance. The **Compliance Officer** owns the policy and checks its regulatory alignment. The **Control Owner / Auditor** maintains the access review, evidence, and monitoring process. **Clinical Directors and managers** approve staff access and report changes. The **IT Helpdesk Contractor** follows the remote-support rules and supplies access records. The **ClinicCloud vendor** implements technical settings and supplies logs and assurance evidence. All users protect their credentials and report suspected compromise immediately.

## Enforcement

Non-compliant access must be suspended while the issue is investigated. Repeated or intentional violations may result in removal of access, contract action, or disciplinary action. Suspected compromise or unauthorized patient-record access must be escalated under the incident-response and breach-notification procedure.

## References and traceability

This policy implements R-001, R-003, R-013, and R-015; controls C-001 and C-002; and NIST CSF 2.0 PR.AA-03 and PR.AA-05. Design evidence is in the MedCore Clinics Resource Pack §3.1, §3.4, and §3.5. The linked roadmap actions are `RM-01`, `RM-02`, `RM-03`, and `RM-05` in `08-final-report/roadmap.md`.
