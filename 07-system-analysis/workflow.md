# Dependency Map

This is the team's working workflow. The instructor's official document does not provide a detailed dependency graph, so treat this as a project-management proposal and adjust it when actual assignments are issued.

## Core Flow

1. **Team Lead / System Analysis coordination**
   - Understand scenario and scope.
   - Record requirements and assumptions.
   - Identify initial assets/processes.
2. **Threat Modeler**
   - Uses scope/assets to identify threats and attack scenarios.
3. **Risk Analyst**
   - Uses assets + threats/vulnerabilities to build and score risks.
4. **Control Owner / Auditor**
   - Uses prioritized risks to propose/assess controls and evidence.
5. **Compliance Officer**
   - Maps controls/findings to the selected framework and identifies gaps.
6. **Policy Writer**
   - Uses risks, controls, and compliance gaps to draft policies.
7. **Team Lead**
   - Integrates deliverables into the final report and presentation.

## Parallel Work

Threat modeling and initial asset/process analysis can progress in parallel after the scope is clear.

## Key Handoffs

| From | Output | To |
|---|---|---|
| Team Lead/System Analysis | Scope, requirements, assets/processes | Threat Modeler, Risk Analyst |
| Threat Modeler | Threats, attack scenarios, vulnerabilities | Risk Analyst |
| Risk Analyst | Risk Register, scores, priorities | Control Owner, Compliance, Policy Writer |
| Control Owner | Controls, evidence, findings | Compliance, Policy Writer |
| Compliance | Framework mapping, gaps | Policy Writer, Team Lead |
| Policy Writer | Policies | Team Lead |
| All roles | Reviewed deliverables + evidence | Team Lead |

