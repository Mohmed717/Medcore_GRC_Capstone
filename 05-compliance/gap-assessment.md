# NIST CSF 2.0 Gap Assessment

## Assessment basis

This is a design-phase assessment, not an operating-effectiveness audit. A control is **Fully Addressed** only when the design package shows a defined intent and an accountable mechanism. A control is **Partially Addressed** when the architecture or a vendor statement provides a limited safeguard but important scope, ownership, or evidence is missing. A control is **Not Addressed** when the design contains no meaningful control intent.

The selected framework is NIST CSF 2.0. The full 16-area mapping, risk links, evidence, owners, priorities, and recommendations are in `framework-mapping.csv`.

## Results

| Status | Count | Interpretation |
|---|---:|---|
| Not Addressed | 9 | No meaningful design intent is documented. |
| Partially Addressed | 7 | A limited safeguard or architectural statement exists, but it is not sufficient to approve go-live. |
| Fully Addressed | 0 | No control area has operating evidence because the project is pre-implementation. |

## Regulatory exposure

The resource pack requires the team to consider HIPAA-style obligations for minimum-necessary access, audit trails, and breach notification. The highest direct exposure is **R-003 / CM-008**, because cross-clinic access is not segmented; **R-009 / CM-013**, because MedCore cannot access or monitor audit logs; and **R-010 / CM-015**, because no incident-response or breach-notification procedure exists. The shared migration folder and third-party integrations add further exposure because restricted or confidential patient data moves through temporary and external services without completed lifecycle and supplier controls.

## Go-live blockers

The following gaps should block go-live until design and evidence are approved: MFA and identity lifecycle, clinic-level authorization, endpoint baseline and patch management, restricted CSV handling and disposal, vendor security terms and assurance, MedCore audit-log access, incident response and notification, and backup encryption/region plus restore testing. The roadmap in `08-final-report/roadmap.md` converts these gaps into owners, effort, and horizons.

## Auditor verification rule

The Control Owner / Auditor must verify each cited Section 3 statement against the resource pack and must not treat a vendor claim, planned control, or requested artifact as evidence that the control is operating. The verification record is in `04-controls/control-assessment.md`.
