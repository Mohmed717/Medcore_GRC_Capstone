# Attack Chain: Stolen Clinic Laptop → Patient-Record Access

## Scenario

This is a design-phase attack narrative derived from the documented architecture. It is not evidence that the event has occurred.

1. An attacker steals a clinic-owned Windows laptop. The resource pack states that these laptops average approximately four years old and have unknown or unmanaged patch status.
2. The attacker opens the Chrome browser or uses an active session left on the device. The design does not state a device-management baseline, full-disk encryption, remote wipe, or session timeout.
3. The attacker reaches ClinicCloud through the public internet. The design confirms HTTPS/TLS 1.2 in transit, but TLS does not replace endpoint, session, or identity controls.
4. If the session is not active, the attacker attempts the staff username/password. MFA is available from the vendor but has not been enabled, and the only confirmed password baseline is the vendor default.
5. The compromised account receives one of the two defined roles. The design does not yet distinguish clinic locations, so a Clinician role at one clinic may see patients from another clinic.
6. The attacker searches and exports patient records from ClinicCloud. MedCore has no designed access to the platform's audit logs, so detection and investigation may be delayed.

## Consequences

The chain can expose restricted PHI and confidential PII, violate minimum-necessary access, interrupt clinical work if malware is introduced, and delay breach notification because no incident-response process is documented.

## Prevention and detection points

| Stage | Required safeguard | Linked records |
|---|---|---|
| Device theft | Full-disk encryption, screen lock, remote wipe, managed endpoint baseline | R-002, R-004; NIST PR.PS-01, PR.PS-03 |
| Login | MFA, password protection, rate limiting, anomaly alerts | R-001, R-013; NIST PR.AA-03, PR.AA-05 |
| Authorization | Clinic-level segmentation and quarterly access review | R-003; NIST PR.AA-05 |
| Activity | MedCore-accessible audit logs and alerting | R-009; NIST DE.CM-03 |
| Response | Tested containment and breach-notification procedure | R-010; NIST RS.MA-01, RS.CO-02 |
