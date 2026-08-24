# MedCore Clinics GRC Presentation Notes

**Target duration:** 10–12 minutes
**Audience:** Executive sponsor and class review
**Framework:** NIST CSF 2.0

| Segment | Time | Presenter role | Core message |
|---|---:|---|---|
| 1. Business context | 1:00 | Hana Saeed — Team Lead / Presenter | MedCore has 14 clinics moving records to one cloud EHR before security governance exists. |
| 2. Scope and assets | 1:00 | Hana Saeed — Team Lead / Presenter | The design creates 16 governed assets, including restricted PHI, the SaaS tenant configuration, identities, endpoints, migration files, vendors, and backups. Do not list vendor-owned software or infrastructure as MedCore assets. |
| 3. Architecture and data flow | 1:00 | Hana Saeed — Team Lead / Presenter | The critical boundaries are the public internet, the ClinicCloud SaaS tenant, the vendor-hosted data repository, third-party APIs, migration folder, backups, and remote support. |
| 4. Threat actors and attack chain | 1:30 | Hassan Amin — Threat Modeler | A stolen laptop plus no MFA can lead to ClinicCloud access, cross-clinic visibility, and delayed detection. |
| 5. Risk method and top risks | 1:30 | Mohamed Youssef — Risk Analyst | Sixteen risks were scored qualitatively using Likelihood × Impact; nine are Critical and seven High. |
| 6. Risk matrix and treatment | 1:00 | Mohamed Youssef — Risk Analyst | The top priorities are MFA, clinic-level authorization, migration-folder protection, endpoint controls, logging, and supplier assurance. |
| 7. Framework and gaps | 1:15 | Mahmoud Mamdouh — Compliance Officer | NIST CSF 2.0 maps 16 areas; nine are Not Addressed and seven Partially Addressed in the design. |
| 8. Controls, evidence, and BIA | 1:15 | Islam Khodr — Control Owner / Auditor | Design citations support the ratings, but no operating effectiveness is claimed; EHR and migration cutover are Mission-Critical. |
| 9. Policy | 0:45 | Mikhail Sobhi — Policy Writer | The Access Control Policy turns the highest gaps into testable MFA, least-privilege, lifecycle, endpoint, logging, and exception rules. |
| 10. Roadmap and decision | 1:00 | Hana Saeed — Team Lead / Presenter | Go-live should be conditional on evidence for eight launch blockers; remaining improvements follow in 90 days and continuously. |

## Speaker prompts

### Hana Saeed — Team Lead / Presenter

Open with the decision: MedCore should not migrate or launch until the listed controls are evidenced. Explain that the repository is intentionally a design-phase assessment, not a claim that the system is already secure. Close by asking the COO to approve the launch gate, owners, and evidence requirements.

### Hassan Amin — Threat Modeler

Show the flow from a clinic laptop to ClinicCloud and the external services. Explain that TLS 1.2 protects transport but does not solve stolen sessions, missing MFA, broad authorization, or missing logs. Walk through the six-step stolen-laptop chain in the attack-scenarios folder.

### Mohamed Youssef — Risk Analyst

Explain the shared 5×5 method and why the ratings are qualitative. Emphasize that the Critical scores are driven by restricted PHI, broad access, and absent controls—not by invented probabilities or financial figures.

### Mahmoud Mamdouh — Compliance Officer

Explain why one framework was selected and used consistently. Point to the regulatory exposures required by the exercise: minimum-necessary access, audit trail, and breach notification. Distinguish design statements from operating evidence.

### Islam Khodr — Control Owner / Auditor

Explain the evidence rule and BIA. Nightly backup is a planned dependency, not a tested recovery capability. State that the sign-off is conditional on restore tests, log access, access reviews, and control evidence.

### Mikhail Sobhi — Policy Writer

Highlight that the policy contains numbered, testable statements. The most important rule is that every human account must use MFA before activation, followed by clinic-level least privilege and timely offboarding.

## GitHub Evidence Trail

Use the Evidence Trail slide during the discussion. Hana Saeed should open `scope.md` and `assets.csv`; Hassan Amin should open `threat-model.md` and the stolen-laptop scenario; Mohamed Youssef should open `risk-register.csv`; Mahmoud Mamdouh should open `framework-mapping.csv` and `gap-assessment.md`; Islam Khodr should open `control-matrix.csv`, `evidence-register.csv`, and `bia.md`; and Mikhail Sobhi should open `access-control-policy.md`. These links are included in the slide as clickable references to the reviewed `final-report` branch.

## Closing recommendation

Approve a **conditional go-live gate**: no migration or production access until RM-01 through RM-08 are complete, evidenced, and reviewed by the Control Owner / Auditor, with residual risk accepted by the COO. Then operate the 90-day monitoring and review plan and reassess the register annually.
