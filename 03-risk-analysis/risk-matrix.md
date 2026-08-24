# Qualitative Risk Matrix

## Scoring method

Risk score equals **Likelihood × Impact**. Likelihood and impact are rated from 1 to 5 using the design-phase definitions in the resource pack. The bands are Low (1–4), Medium (5–9), High (10–15), and Critical (16–25). Scores are qualitative prioritization aids, not probabilities or financial estimates.

| Likelihood \ Impact | 1 Negligible | 2 Minor | 3 Moderate | 4 Major | 5 Severe |
|---|---:|---:|---:|---:|---:|
| 5 Almost Certain | 5 Medium | 10 High | 15 High | 20 Critical | 25 Critical |
| 4 Likely | 4 Low | 8 Medium | 12 High | 16 Critical | 20 Critical |
| 3 Possible | 3 Low | 6 Medium | 9 Medium | 12 High | 15 High |
| 2 Unlikely | 2 Low | 4 Low | 6 Medium | 8 Medium | 10 High |
| 1 Rare | 1 Low | 2 Low | 3 Low | 4 Low | 5 Medium |

## Portfolio view

| Level | Count | Risk IDs |
|---|---:|---|
| Critical | 9 | R-001, R-002, R-003, R-004, R-005, R-009, R-011, R-013, R-015 |
| High | 7 | R-006, R-007, R-008, R-010, R-012, R-014, R-016 |
| Medium | 0 | — |
| Low | 0 | — |

The concentration of Critical and High risks is expected in a pre-implementation design with no established security function, no enabled MFA, no clinic-level segmentation, no MedCore logging access, and unresolved supplier and migration controls.

## Priority order

| Priority | Risk | Score | Why it leads |
|---:|---|---:|---|
| 1 | R-001 Credential stuffing | 20 | Public access plus no MFA creates a direct path to restricted records. |
| 2 | R-003 Cross-clinic access | 20 | The defined role model permits access beyond minimum necessity. |
| 3 | R-005 Migration-folder disclosure | 20 | Restricted legacy CSVs are held in a shared location without lifecycle controls. |
| 4 | R-002 Stolen laptop/session | 20 | Endpoint and session protections are not specified for all clinic devices. |
| 5 | R-009 Undetected access | 16 | Lack of MedCore log access weakens detection and breach investigation. |
| 6 | R-011 Supplier control failure | 16 | Multiple critical data flows depend on unverified vendors and missing contract terms. |

All detailed justifications, treatments, owners, and sources are maintained in `risk-register.csv`.
