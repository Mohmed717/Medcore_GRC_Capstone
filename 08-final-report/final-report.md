# MedCore Clinics GRC Capstone — Final Report

## 1. Executive summary

See [`executive-summary.md`](executive-summary.md). MedCore's design-phase posture is Critical before go-live because the planned ClinicCloud migration concentrates restricted patient data and access in a public-internet SaaS architecture while key identity, authorization, endpoint, monitoring, supplier, migration, response, and recovery controls remain unresolved.

## 2. Organization and business context

MedCore Clinics is a fictional chain of 14 outpatient clinics across three cities. Leadership plans to migrate local patient records to a single cloud EHR so that clinics can retrieve histories, schedule appointments centrally, and consolidate billing. No security function, formal access-control process, security policy, or prior risk assessment exists in the scenario.

## 3. Scope and assumptions

The assessment covers the contracted ClinicCloud SaaS tenant and service configuration, the vendor-hosted patient data repository, identity store, clinic endpoints, access sessions, internet access path, legacy export data, CSV migration folder and pipeline, backup storage, billing clearinghouse, reminder service, helpdesk remote access, logging capability, and supplier governance. Vendor-owned application software and infrastructure are outside MedCore's asset inventory and are treated as supplier dependencies and trust boundaries. It is design-phase only. The complete boundaries and labelled assumptions are in [`01-project-scope/scope.md`](../01-project-scope/scope.md).

## 4. System design and data flow

Each clinic accesses ClinicCloud through a browser over the public internet. The vendor-hosted ClinicCloud service connects internally to its managed data repository, and externally through HTTPS APIs to the billing clearinghouse and SMS/email reminder service. Legacy systems export CSV files to a shared migration folder for a one-time vendor import. Nightly backups go to vendor storage, but region and encryption are unspecified. The helpdesk contractor will use a remote-access tool that has not been selected.

## 5. Asset inventory

The inventory contains 16 governed assets across tenant configuration, data stores, identities, endpoints, access sessions, interfaces, third parties, processes, and governance. It intentionally excludes vendor-owned application software and infrastructure. The complete register is [`01-project-scope/assets.csv`](../01-project-scope/assets.csv). Restricted assets include patient records, clinical notes, staff credentials, migration exports, the vendor-hosted data repository, and backup storage.

## 6. Threat model

Threat actors include external credential attackers, malicious or curious insiders, laptop thieves and malware operators, compromised helpdesk contractors, careless or compromised vendors, and cloud/network failures. Trust boundaries exist at the clinic endpoint, public internet, the ClinicCloud SaaS tenant, the vendor-hosted data repository, third-party APIs, the migration folder, the backup environment, and the remote-support path. The detailed model is [`02-threat-model/threat-model.md`](../02-threat-model/threat-model.md) and [`02-threat-model/threat-model.csv`](../02-threat-model/threat-model.csv). The stolen-laptop-to-no-MFA chain is documented in [`02-threat-model/attack-scenarios/stolen-laptop-no-mfa.md`](../02-threat-model/attack-scenarios/stolen-laptop-no-mfa.md).

## 7. Risk assessment method

Risk score equals Likelihood × Impact on a qualitative 5×5 scale. Risk levels are Low (1–4), Medium (5–9), High (10–15), and Critical (16–25). The register contains 16 risks, nine Critical and seven High, with one-line justifications and Section 3 evidence for every rating. See [`03-risk-analysis/risk-register.csv`](../03-risk-analysis/risk-register.csv), [`03-risk-analysis/risk-matrix.md`](../03-risk-analysis/risk-matrix.md), and [`03-risk-analysis/risk-treatment.md`](../03-risk-analysis/risk-treatment.md).

## 8. Framework and gap analysis

The project selected NIST CSF 2.0 as its single framework. It provides a flexible taxonomy of cybersecurity outcomes for understanding, assessing, prioritizing, and communicating risk. The mapping assesses 16 areas: nine Not Addressed, seven Partially Addressed, and zero Fully Addressed because the project is pre-implementation. The greatest gaps are identity and MFA, clinic-level authorization, endpoint management, migration lifecycle, supplier assurance, log access, incident response, and backup recovery. See [`01-project-scope/framework-decision.md`](../01-project-scope/framework-decision.md), [`05-compliance/framework-mapping.csv`](../05-compliance/framework-mapping.csv), and [`05-compliance/gap-assessment.md`](../05-compliance/gap-assessment.md).

## 9. Controls and evidence

The control matrix defines 16 administrative, technical, detective, response, and recovery controls. The auditor verified that design citations support the ratings, but no operating effectiveness conclusion is permitted. Evidence marked as a vendor statement, design statement, or project artifact must be replaced or supplemented by implementation evidence after deployment. See [`04-controls/control-matrix.csv`](../04-controls/control-matrix.csv), [`04-controls/control-assessment.md`](../04-controls/control-assessment.md), and [`04-controls/evidence-register.csv`](../04-controls/evidence-register.csv).

## 10. Business impact analysis

The BIA identifies ClinicCloud patient-record access and migration cutover as Mission-Critical, with appointment scheduling, claims/billing, and identity/log monitoring as Important. The impact dimensions are Financial, Operational, Reputational, and Legal/Regulatory. MTD/RTO/RPO values are qualitative planning assumptions that require validation through vendor commitments, downtime exercises, and restore tests. See [`04-controls/bia.md`](../04-controls/bia.md).

## 11. Policy

The standalone Access Control Policy addresses the highest-priority identity and authorization gaps. It requires MFA, unique identities, clinic-level least privilege, approvals, leaver and temporary-access expiry, stronger passwords, managed endpoints, audit-log availability, controlled remote support, and documented exceptions. See [`06-policies/policies/access-control-policy.md`](../06-policies/policies/access-control-policy.md) and [`06-policies/policy-mapping.csv`](../06-policies/policy-mapping.csv).

## 12. Remediation roadmap

The roadmap contains eight must-fix actions before go-live, four actions for the first 90 days, and three longer-term improvements. The launch gate requires evidence, not just vendor promises or planned controls. See [`roadmap.md`](roadmap.md).

## 13. Governance and decision

The COO owns go-live approval and residual-risk acceptance. The Team Lead coordinates integration; the Risk Analyst owns the register; the Threat Modeler owns attack paths; the Compliance Officer owns framework choice and policy; the Control Owner / Auditor verifies evidence and BIA; and the Policy Writer maintains the standalone policy. These are role assignments, not named individuals.

## 14. Limitations

The assessment does not perform penetration testing, legal analysis, vendor audit, source-code review, financial loss modelling, or clinical safety validation. It relies on the fictional design package and clearly labels inferred ownership and recovery assumptions. It should be updated when vendor assurance documents, technical configurations, contracts, or implementation evidence become available.

## 15. References

1. MedCore Clinics GRC Track Resource Pack, Section 2–4, supplied as `MedCore_Clinics_GRC_Resource_Pack.pdf`.
2. MedCore GRC Unified Handbook, supplied as `MedCore_GRC_Unified_Handbook.pdf`.
3. NIST, *The NIST Cybersecurity Framework (CSF) 2.0*, NIST CSWP 29, published February 26, 2024: [official publication](https://www.nist.gov/publications/nist-cybersecurity-framework-csf-20) and [DOI](https://doi.org/10.6028/NIST.CSWP.29).
