# Remediation Roadmap

The roadmap is ordered by patient-data exposure, regulatory consequence, and dependency. “Before go-live” items are launch gates, not optional improvements. Effort is a qualitative estimate for planning.

## Before go-live — must fix

| ID | Action | Risks / gaps addressed | Owner | Effort | Definition of done |
|---|---|---|---|---|---|
| RM-01 | Enable MFA and strengthen password/account-protection settings. | R-001, R-013; CM-007; C-001 | Compliance Officer / ClinicCloud Vendor | Medium | MFA enrollment, password settings, recovery and lockout tests are evidenced. |
| RM-02 | Design and test clinic-level least privilege for Clinician and Front Desk roles. | R-003; CM-008; C-002 | Control Owner / Clinical Directors | High | Approved authorization matrix and cross-clinic negative tests pass. |
| RM-03 | Establish managed endpoint baseline and patch compliance for clinic laptops. | R-002, R-004; CM-011; CM-012; C-009; C-010 | Control Owner / IT Helpdesk Contractor | High | Device inventory, encryption, screen lock, endpoint protection and patch report are approved. |
| RM-04 | Secure the migration lifecycle: Restricted classification, encrypted files, access limits, checksums, reconciliation, dual approval, and disposal. | R-005, R-006, R-016; CM-009; CM-010; C-016 | Team Lead / Vendor Migration Team | Medium | Migration runbook, chain-of-custody log, reconciliation sign-off and deletion approval exist. |
| RM-05 | Contract for ClinicCloud, clearinghouse, and reminder-service assurance, breach SLA, audit rights, data location, and offboarding. | R-007, R-008, R-011, R-015; CM-003; C-003 | COO / Procurement | Medium | Signed addenda and reviewed assurance artifacts are stored in the evidence register. |
| RM-06 | Obtain MedCore audit-log access and define monitoring and retention. | R-009; CM-013; C-011 | Control Owner / ClinicCloud Vendor | Medium | Log export, alert rules, retention, review owner, and a sample review are evidenced. |
| RM-07 | Approve and exercise incident-response and breach-notification procedures. | R-010; CM-015; C-013 | Team Lead / Compliance Officer | Medium | Plan, contact list, tabletop exercise, escalation and decision records are approved. |
| RM-08 | Confirm backup encryption/region and test restore against BIA objectives. | R-008, R-014; CM-009; CM-016; C-014 | Control Owner / ClinicCloud Vendor | Medium | RTO/RPO approval, restore record and downtime runbook are complete. |

## First 90 days post-launch

| ID | Action | Risks / gaps addressed | Owner | Effort | Definition of done |
|---|---|---|---|---|---|
| RM-09 | Perform quarterly access review and sample patient-record access review. | R-003, R-009, R-015 | Control Owner / Clinical Directors | Low | Review results, removals, exceptions and approvals are retained. |
| RM-10 | Review provider activity, API data minimization, and service-account access. | R-007, R-011, R-015; CM-014 | COO / Procurement | Medium | Provider attestations, logs, minimization review and actions are documented. |
| RM-11 | Run endpoint patch and remote-support compliance reviews. | R-002, R-004, R-012 | Control Owner / IT Helpdesk Contractor | Medium | Monthly compliance trend and session samples are reviewed. |
| RM-12 | Conduct a downtime and restore exercise with Clinical Directors and billing owners. | R-008, R-014 | Control Owner / Clinical Directors | Medium | Exercise results and corrective actions are approved. |

## Longer term / continuous improvement

| ID | Action | Risks / gaps addressed | Owner | Effort | Definition of done |
|---|---|---|---|---|---|
| RM-13 | Establish quarterly NIST CSF profile review and annual risk reassessment. | R-001–R-016; CM-002; CM-006 | Team Lead / Risk Analyst | Medium | Updated profile, risk register and executive review are recorded. |
| RM-14 | Evaluate stronger identity federation, phishing-resistant MFA, and adaptive access. | R-001, R-013 | Compliance Officer / ClinicCloud Vendor | High | Roadmap decision and tested target architecture are approved. |
| RM-15 | Review vendor concentration, backup portability, and exit/migration plan. | R-008, R-011, R-014 | COO / Procurement | High | Exit plan, data-return test and supplier resilience review are completed. |
