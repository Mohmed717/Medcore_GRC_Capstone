# MedCore Clinics GRC Capstone

This repository contains a complete **design-phase GRC assessment** for MedCore Clinics, a fictional chain of 14 outpatient clinics migrating patient records to the ClinicCloud cloud EHR. The work follows the supplied MedCore GRC Resource Pack and Unified Handbook and deliberately does not claim that the design has been implemented or tested.

## Decision summary

The project uses **NIST Cybersecurity Framework (CSF) 2.0** consistently. The assessment contains 16 assets, 16 threats, 16 qualitative risks scored with Likelihood × Impact, 16 mapped control areas, a control and evidence assessment, a five-process BIA, a standalone Access Control Policy, an executive summary, a final report, and a three-horizon remediation roadmap.

The current design posture is **Critical before go-live**: nine risks are Critical and seven are High. The launch gate is conditional on MFA, clinic-level least privilege, endpoint management, migration-file protection and reconciliation, supplier assurance, MedCore audit-log access, incident response, and backup/recovery evidence.

## Deliverables

| Area | Main files |
|---|---|
| Scope and assets | [`01-project-scope/scope.md`](01-project-scope/scope.md), [`01-project-scope/assets.csv`](01-project-scope/assets.csv), [`01-project-scope/framework-decision.md`](01-project-scope/framework-decision.md) |
| Threat model | [`02-threat-model/threat-model.md`](02-threat-model/threat-model.md), [`02-threat-model/threat-model.csv`](02-threat-model/threat-model.csv), [`02-threat-model/attack-scenarios/stolen-laptop-no-mfa.md`](02-threat-model/attack-scenarios/stolen-laptop-no-mfa.md) |
| Risk analysis | [`03-risk-analysis/risk-register.csv`](03-risk-analysis/risk-register.csv), [`03-risk-analysis/risk-matrix.md`](03-risk-analysis/risk-matrix.md), [`03-risk-analysis/risk-treatment.md`](03-risk-analysis/risk-treatment.md) |
| Controls and BIA | [`04-controls/control-matrix.csv`](04-controls/control-matrix.csv), [`04-controls/control-assessment.md`](04-controls/control-assessment.md), [`04-controls/evidence-register.csv`](04-controls/evidence-register.csv), [`04-controls/bia.md`](04-controls/bia.md) |
| Compliance | [`05-compliance/framework-mapping.csv`](05-compliance/framework-mapping.csv), [`05-compliance/gap-assessment.md`](05-compliance/gap-assessment.md) |
| Policy | [`06-policies/policies/access-control-policy.md`](06-policies/policies/access-control-policy.md), [`06-policies/policy-mapping.csv`](06-policies/policy-mapping.csv) |
| System analysis | [`07-system-analysis/dependencies.csv`](07-system-analysis/dependencies.csv), [`07-system-analysis/diagrams/data-flow.mmd`](07-system-analysis/diagrams/data-flow.mmd), [`07-system-analysis/diagrams/data-flow.png`](07-system-analysis/diagrams/data-flow.png) |
| Final package | [`08-final-report/executive-summary.md`](08-final-report/executive-summary.md), [`08-final-report/final-report.md`](08-final-report/final-report.md), [`08-final-report/roadmap.md`](08-final-report/roadmap.md), [`09-presentation/presentation-notes.md`](09-presentation/presentation-notes.md) |
| Evidence and references | [`10-evidence/references/source-register.md`](10-evidence/references/source-register.md), [`docs/project-status.md`](docs/project-status.md) |

## Workflow and governance

The repository follows the supplied workflow: assets and scope → threats → risks → controls and BIA → framework mapping → policy → roadmap and final integration → presentation. Work should be reviewed by another role before merge. Named team members are intentionally not invented and remain a team decision.

## Important limitation

All records are fictional and qualitative. Design statements and vendor claims are not operating evidence. Before a real go-live decision, the team must collect configurations, signed supplier terms, access reviews, audit logs, restore tests, migration reconciliation, and an exercised incident-response record.

## References

The primary scenario source is the supplied `MedCore_Clinics_GRC_Resource_Pack.pdf`; the workflow and ownership source is the supplied `MedCore_GRC_Unified_Handbook.pdf`. The external framework reference is [NIST CSF 2.0](https://www.nist.gov/publications/nist-cybersecurity-framework-csf-20) and [NIST CSWP 29](https://doi.org/10.6028/NIST.CSWP.29).
