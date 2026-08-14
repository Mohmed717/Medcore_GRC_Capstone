# Contributing Guide

## 1. Before You Start

1. Pull the latest `main`.
2. Work only inside your assigned area unless coordinating with another role.
3. Check `docs/dependency-map.md` before starting a dependent task.
4. Never use real patient data, passwords, tokens, API keys, or confidential information.

## 2. Branches

Create or use your role branch:

```text
risk-analyst
threat-modeler
control-owner
compliance
policy-writer
team-lead
```

## 3. Commits

Use clear commits:

```text
risk: add initial risk register
threat: add ransomware scenario
control: add MFA control assessment
compliance: map access control to framework
policy: add access control policy
lead: integrate final report
```

## 4. Pull Requests

Every PR should include:

- What changed?
- Why was it changed?
- Which assignment/deliverable does it satisfy?
- What dependencies were used?
- What should reviewers check?

## 5. Review Rule

At least one other team member reviews important deliverables before merge.

For cross-role deliverables, involve both roles. Example:

- Risk Register → Risk Analyst + Threat Modeler/Control Owner
- Control Mapping → Control Owner + Compliance Officer
- Policy Mapping → Policy Writer + Compliance Officer

## 6. Evidence

For every claim that requires proof, add evidence under `10-evidence/` or reference the appropriate source.

Do not commit secrets or sensitive data.

## 7. Pull Request Checklist

- [ ] My branch is up to date.
- [ ] Files are in the correct folder.
- [ ] No secrets/sensitive data are included.
- [ ] Deliverable is complete.
- [ ] Evidence/references are included where needed.
- [ ] I tested/checked the document or spreadsheet.
- [ ] Reviewer has enough context to review it.
