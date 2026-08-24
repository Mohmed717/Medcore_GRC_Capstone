# Control Assessment and Evidence Verification

## Assessment statement

The Control Owner / Auditor reviewed the evidence references used in the gap analysis against the MedCore design package. The review confirms that the citations support the **design observations** recorded, but none of the controls has operating evidence because the resource pack states that the project is still in design / pre-implementation.

## Verification register

| Control ID | Evidence cited | Does the citation support the design rating? | Operating evidence | Finding |
|---|---|---|---|---|
| C-001 | §3.1 authentication; §3.5 MFA open item | Yes | None | MFA must be enabled and tested. |
| C-002 | §3.1 roles; §3.5 segmentation and offboarding items | Yes | None | Authorization design and removal workflow are missing. |
| C-003 | §3.4 vendor assurance and contract gaps | Yes | None | Supplier due diligence and security terms are absent. |
| C-004 | §3.1–§3.3 system, data, endpoint, and integration descriptions | Yes | Project artifact only | Inventory exists in this repository; operational ownership must be confirmed. |
| C-005 | §3.5 open items and the documented architecture | Yes | Project artifact only | Risk analysis is complete for design; reassess after implementation. |
| C-006 | §3.4 no incident/recovery process | Yes | None | Improvement cadence is absent. |
| C-007 | §3.4 encryption statement and unknown key details | Yes | Vendor marketing statement only | Cryptography and key-management evidence is required. |
| C-008 | §3.2 TLS and API flows; §3.4 control gaps | Yes | TLS statement only | File, API, and certificate governance require evidence. |
| C-009 | §3.1 devices; §3.2 remote support; §3.5 remote-support tool not selected | Yes | None | Endpoint and remote tool baseline are not designed. |
| C-010 | §3.1 patch status unknown | Yes | None | Patch compliance cannot be established. |
| C-011 | §3.4 no MedCore logging or monitoring | Yes | Vendor logs may exist | Contractual log access and monitoring evidence are required. |
| C-012 | §3.2 third-party paths; §3.4 supplier gaps | Yes | None | Provider activity oversight is not designed. |
| C-013 | §2 regulatory context; §3.4 no response plan | Yes | None | Response and notification process must be approved and exercised. |
| C-014 | §3.2 nightly backup; §3.4 region/encryption open items | Yes | Backup intention only | Restore evidence and objectives are missing. |
| C-015 | §2 stakeholders; no security function described | Yes | None | Governance and risk-acceptance route are not formalized. |
| C-016 | §3.1–§3.3 CSV migration flow and classification | Yes | None | Chain of custody, reconciliation, and disposal evidence are required. |

## Sign-off

As Control Owner / Auditor, I confirm that the gap-analysis ratings are internally consistent with the design evidence cited above. I also confirm that the BIA does not assume recovery capabilities that the design has not evidenced: the nightly backup is treated as a planned dependency, not as proof of a tested recovery process. This sign-off is conditional on replacing requested and design-only entries with implementation evidence before go-live.
