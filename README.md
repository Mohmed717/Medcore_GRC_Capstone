# MedCore GRC Capstone

A collaborative GRC capstone for **MedCore Clinics**, a fictional clinic chain moving patient records to a cloud-based system without an existing security policy.

> **Official project requirements:** the capstone is a team-of-6 project with six listed roles: Risk Analyst, Compliance Officer, Threat Modeler, Control Owner / Auditor, Policy Writer, and Team Lead / Presenter. The project requires a real framework (ISO 27001 or NIST CSF), a scored risk matrix using likelihood × impact, at least 12 risks, a written report, presentation, and evidence.  
> This repository adds **System Analysis / project coordination as an internal responsibility of the Team Lead** only if the instructor approves that arrangement.

## Project Goals

- Build a patient-data risk register.
- Identify realistic threats.
- Assess and prioritize at least 12 risks.
- Map findings to a recognized framework.
- Define security controls and evidence.
- Produce policies and prioritized recommendations.
- Prepare the final report and 10–15 minute presentation.

## Team

| Member | Role | Main Output |
|---|---|---|
| TBD | Risk Analyst | Risk Register, Risk Matrix, Risk Treatment |
| TBD | Compliance Officer | Framework Mapping, Gap Assessment |
| TBD | Threat Modeler | Threat Model, Attack Scenarios |
| TBD | Control Owner / Auditor | Control Matrix, Evidence, Findings |
| TBD | Policy Writer | Security Policies |
| TBD | Team Lead / Presenter + System Analysis coordination | Workflow, Integration, Final Report, Presentation |

## Recommended Workflow

```text
Scope / Scenario
      ↓
Assets & Processes
      ↓
Threat Identification
      ↓
Risk Identification & Assessment
      ↓
Controls
      ↓
Compliance / Framework Mapping
      ↓
Policies & Recommendations
      ↓
Integration Review
      ↓
Final Report + Presentation
```

Some activities can run in parallel after their required inputs exist.

## Repository Structure

- `01-project-scope/` — scope, requirements, assumptions, assets
- `02-threat-model/` — threats and attack scenarios
- `03-risk-analysis/` — risk register, matrix, treatment, recommendations
- `04-controls/` — controls, assessment, evidence
- `05-compliance/` — framework mapping and gaps
- `06-policies/` — policy documents and mapping
- `07-system-analysis/` — workflow, dependencies, requirements
- `08-final-report/` — final report
- `09-presentation/` — slides and speaker notes
- `10-evidence/` — screenshots, logs, references
- `docs/` — project-level documentation
- `templates/` — reusable templates
- `.github/ISSUE_TEMPLATE/` — GitHub task templates

## Branching

Use one branch per role:

- `risk-analyst`
- `threat-modeler`
- `control-owner`
- `compliance`
- `policy-writer`
- `team-lead`

Do not commit directly to `main`. Open a Pull Request when a deliverable is ready for review.

## Definition of Done

A deliverable is done when:

- [ ] The required fields are complete.
- [ ] Sources/references are recorded where applicable.
- [ ] Evidence is attached or linked.
- [ ] Dependencies are satisfied.
- [ ] Another team member has reviewed it.
- [ ] The Team Lead has approved integration into `main`.

## Framework

Choose **one** framework and record the decision in `01-project-scope/framework-decision.md`.

Options specified by the project:
- NIST CSF
- ISO 27001

## Evidence

Keep screenshots, logs, diagrams, and notes as work progresses. Do not include secrets, passwords, API keys, personal data, or real patient information.

## Presentation

The final presentation should tell a clear story:

**Company → Scope → Threats → Risks → Risk Matrix → Controls → Compliance → Policies → Recommendations → Conclusion**

