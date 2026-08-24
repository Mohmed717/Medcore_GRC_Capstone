# Scope and Assumptions

## In scope

This design-phase assessment covers MedCore Clinics' planned migration of patient records from 14 local practice-management systems across three cities to the ClinicCloud multi-tenant SaaS EHR. It covers the contracted ClinicCloud SaaS tenant and service configuration, the vendor-hosted patient data repository, staff identities and roles, clinic-owned Windows laptops and access sessions, the public-internet access path, legacy CSV exports and the shared migration folder, the vendor migration pipeline, nightly backup storage, the billing clearinghouse, the SMS/email reminder service, and the IT helpdesk contractor's remote-access path. The vendor-owned application software and infrastructure remain outside MedCore's asset inventory; MedCore governs the tenant, data, identities, endpoints, service dependencies, and contractual evidence.

The assessment includes governance, qualitative risk analysis, control and framework mapping, evidence expectations, business impact analysis, access-control policy, and a prioritized remediation roadmap before go-live and after launch.

## Out of scope

The assessment does not claim that any design component has been implemented, tested, or certified. It does not perform penetration testing, source-code review, vendor audit, financial loss modelling, clinical safety validation, or a legal determination of HIPAA applicability. It also does not assess unrelated corporate systems, physical clinic security, non-patient business data, or the internal infrastructure of third parties beyond the interfaces and assurance commitments visible in the design package.

## Explicit assumptions

| Assumption | Why it is needed | Treatment |
|---|---|---|
| Ownership labels marked “inferred” are working governance assignments, not facts stated by the design. | The resource pack requires an owner for every asset but does not name all owners. | Confirm before go-live. |
| The regulatory context is treated as HIPAA-style for this exercise, including minimum-necessary access, audit trails, and breach notification. | This is explicitly required by the resource pack. | Legal counsel must confirm the actual jurisdiction and obligations. |
| NIST CSF 2.0 is used as the single reference framework. | The pack permits either NIST CSF 2.0 or ISO/IEC 27001:2022. | All risk and gap references in this repository use NIST CSF 2.0 only. |
| Clinic-level segmentation is treated as not designed because the pack says it is pending. | Needed to rate cross-clinic exposure. | Do not approve go-live until the design is documented and tested. |
| Evidence entries labelled “Requested” or “Design statement” are not proof of operation. | The project is pre-implementation. | Replace with implementation evidence after deployment. |

## Constraints

The environment is fictional and pre-implementation. The assessment stays qualitative; it does not invent dollar values or statistical frequencies. No real patient data, credentials, API keys, or secrets are included.

## Source boundary

Every asset, threat, risk, gap, and recommendation is traced to Section 3 of the MedCore Clinics GRC Track Resource Pack or to an explicitly labelled assumption above. No real patient data or secrets are included.
