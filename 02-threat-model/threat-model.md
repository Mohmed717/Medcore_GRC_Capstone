# ClinicCloud Threat Model

## Method and boundary

The threat model is limited to the design described in Section 3 of the MedCore Clinics Resource Pack. It uses a lightweight STRIDE-inspired review of the ClinicCloud web application, identities, endpoints, migration path, third-party integrations, backup storage, and remote support path. The system is pre-implementation; the entries identify plausible paths that the design must address, not confirmed incidents.

## Threat actors

| Actor | Access or motive | Primary paths |
|---|---|---|
| External credential attacker | Uses reused or weak credentials to reach the public login. | ClinicCloud identity store and web app. |
| Malicious or curious insider | Holds a legitimate staff role and abuses broad access. | Cross-clinic patient search and record access. |
| Opportunistic thief or malware operator | Obtains a clinic laptop or compromises an endpoint. | Chrome sessions, credentials, and workstation access. |
| Compromised helpdesk contractor | Abuses remote-support privileges or a compromised tool. | Clinic workstation fleet. |
| Careless or compromised vendor operator | Misuses migration, backup, or third-party service access. | Shared migration folder, import pipeline, backups, APIs. |
| Cloud or network failure | Causes loss of availability rather than intentional disclosure. | Public internet path, ClinicCloud, backup/recovery dependencies. |

## Trust boundaries

The design crosses trust boundaries between clinic workstations and the public internet, the public internet and ClinicCloud, ClinicCloud and its primary database, ClinicCloud and the billing/reminder providers, legacy systems and the migration folder, and the IT contractor and endpoints. Every boundary carrying patient, diagnosis, billing, or identity data requires explicit authentication, authorization, encryption, logging, supplier assurance, and lifecycle controls.

## Traceability

The detailed threat inventory is in `threat-model.csv`. The primary multi-step chain is in `attack-scenarios/stolen-laptop-no-mfa.md`. Threat IDs map to the risk register in `03-risk-analysis/risk-register.csv`; the mapping is intentional so the team can defend each priority using the documented architecture.
