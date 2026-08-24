# MedCore Clinics GRC Capstone — Six Voices, One Go-Live Decision

## Cover
MedCore Clinics GRC Capstone
Six voices, one go-live decision
Design-phase assessment for the ClinicCloud EHR migration

## Slide 1 — The decision before go-live
Visual direction: Executive decision room; deep navy, white space, and a single critical-red accent.

Central message: MedCore should not migrate or launch until security controls are implemented and evidenced.

- 14 clinics are moving patient records into one cloud EHR through the public internet.
- The design posture is Critical before go-live: 9 Critical risks and 7 High risks.
- The launch gate requires evidence for identity, authorization, endpoints, migration, suppliers, monitoring, response, and recovery.

Bottom line: approve a conditional go-live gate owned by the COO.

## Slide 2 — Role 1: Hana Saeed, Team Lead / Presenter
Visual direction: Command center; navy and teal, structured grid, directional arrows, calm executive tone.

Role mission: Turn scattered design notes into one defensible decision.

What Hana Saeed did:
- Extracted 16 assets from the architecture: systems, data stores, endpoints, interfaces, vendors, and processes.
- Defined scope, assumptions, ownership handoffs, and the order of work.
- Integrated threats, risks, controls, BIA, policy, roadmap, and final report without changing the design-phase boundary.

Her deliverables: asset inventory, executive summary, final report, roadmap, presentation flow, and integration review.

## Slide 3 — Role 2: Hassan Amin, Threat Modeler
Visual direction: Threat radar; charcoal background, amber paths, red attack nodes, high-contrast security operations feel.

Role mission: Show how an attacker could move through the ClinicCloud architecture.

What Hassan Amin did:
- Mapped external attackers, insiders, compromised vendors, helpdesk compromise, and availability failures.
- Traced 16 threats to real assets and trust boundaries in the documented data flow.
- Wrote the multi-step chain: stolen clinic laptop → no MFA → ClinicCloud access → cross-clinic visibility → delayed detection.

His deliverables: threat model, attack paths, and the stolen-laptop/no-MFA attack narrative.

## Slide 4 — Role 3: Mohamed Youssef, Risk Analyst
Visual direction: Risk laboratory; warm sand, crimson, and graphite with a precise matrix-led layout.

Role mission: Convert attack paths into prioritized business risk.

What Mohamed Youssef did:
- Wrote 16 risks using Threat + Vulnerability + Affected Asset.
- Scored every risk with the shared qualitative formula: Likelihood × Impact on a 5×5 matrix.
- Added one-line rationale, related NIST reference, current/planned controls, treatment, owner, and target residual risk.

Her result: 9 Critical and 7 High risks; no invented dollar values or statistical probabilities.

## Slide 5 — Role 4: Mahmoud Mamdouh, Compliance Officer
Visual direction: Regulatory ledger; ivory paper, royal blue, restrained gold rules, evidence-first editorial style.

Role mission: Test whether the design shows intent against one consistent framework.

What Mahmoud Mamdouh did:
- Selected NIST CSF 2.0 and prohibited mixed ISO/NIST references.
- Assessed 16 control areas across Govern, Identify, Protect, Detect, Respond, and Recover.
- Flagged the regulatory exposure around minimum-necessary access, audit trails, and breach notification.

His result: 9 areas Not Addressed, 7 Partially Addressed, and 0 Fully Addressed in a pre-implementation design.

## Slide 6 — Role 5: Islam Khodr, Control Owner / Auditor
Visual direction: Assurance dashboard; slate, white, and verified green with checkmarks, evidence tags, and BIA structure.

Role mission: Separate what the documents say from what the organization can prove.

What Islam Khodr did:
- Verified that the Section 3 citations support the gap ratings without treating vendor claims as operating evidence.
- Built 16 controls plus an evidence register that states what must be collected after implementation.
- Led the qualitative BIA for five critical processes using Financial, Operational, Reputational, and Legal/Regulatory impact.

Her sign-off: the findings are internally consistent, but operating effectiveness remains unproven until testing and evidence exist.

## Slide 7 — Role 6: Mikhail Sobhi, Policy Writer
Visual direction: Policy atelier; plum, rose, and parchment with strong typographic hierarchy and numbered rules.

Role mission: Turn the highest gap into rules people can follow and auditors can test.

What Mikhail Sobhi did:
- Wrote a standalone Access Control Policy for ClinicCloud.
- Converted the top gaps into 10 testable statements: MFA, unique identities, clinic-level least privilege, approvals, offboarding, endpoint condition, logging, remote support, and exceptions.
- Connected every rule to risks R-001, R-003, R-013, and R-015, controls C-001 and C-002, and NIST PR.AA-03 / PR.AA-05.

His success test: a policy that can be approved, enforced, reviewed, and evidenced.

## Slide 8 — From six roles to one traceability chain
Visual direction: Integrated pipeline; split-color bands from each role converging into one bright teal decision line.

- Hana Saeed starts with scope and assets.
- Hassan Amin turns architecture into threats and attack chains.
- Mohamed Youssef scores the resulting risks and recommends treatment.
- Mahmoud Mamdouh maps the risks and controls to NIST CSF 2.0 gaps.
- Islam Khodr verifies evidence and sets recovery priorities through the BIA.
- Mikhail Sobhi translates the priorities into policy rules.

Handoff principle: every recommendation must trace back to a design fact, a risk, a gap, a control, an owner, and evidence.

## Slide 9 — The conditional go-live gate
Visual direction: Decision room; dark navy field, eight illuminated gate tiles, critical-red to verified-teal progression.

Before go-live, MedCore must evidence:
- MFA and identity lifecycle.
- Clinic-level least privilege and access review.
- Managed endpoints, patching, and approved remote support.
- Restricted CSV handling, reconciliation, and secure disposal.
- Supplier assurance, security addenda, breach SLA, and audit rights.
- MedCore audit-log access, retention, alerting, and review.
- Incident response and breach-notification exercise.
- Backup encryption/region confirmation and restore testing against BIA objectives.

Decision: the COO accepts residual risk only after the Control Owner / Auditor confirms the evidence.

## Slide 10 — Closing: one team, one defensible decision
MedCore can gain the operational benefits of a shared cloud EHR, but only after the security design becomes an evidenced operating capability.

The team did not ask, “Does the vendor say it is secure?”

The team asked, “What could go wrong, which control outcome is missing, who owns the fix, and what evidence will prove it?”

Framework reference: NIST Cybersecurity Framework 2.0, NIST CSWP 29 — https://doi.org/10.6028/NIST.CSWP.29
Project evidence: MedCore GRC Resource Pack, Section 3 — design and architecture source of truth.

Thank you.
