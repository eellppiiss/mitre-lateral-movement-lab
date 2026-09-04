# Attack Scenario

## Environment

The laboratory environment was used to study Lateral Movement techniques in Windows.

The lab included Windows 10 systems and an Active Directory environment.

## Objective

The objective was to investigate how Lateral Movement activity can be simulated and detected using Windows security telemetry.

The main investigated technique was:

**T1550.002 — Pass the Hash**

## Attack Simulation

The Pass the Hash technique was simulated in an isolated laboratory environment.

The purpose of the simulation was to generate security telemetry that could later be analyzed.

No real-world systems or accounts were targeted.

## Investigation

After the simulation, Windows Security Event Logs and Sysmon telemetry were collected.

The following events were examined:

- 4624 — Successful Logon
- 4625 — Failed Logon
- 4648 — Explicit Credential Logon
- 4672 — Special Privileges Assigned
- 4688 — Process Creation
- 4776 — Credential Validation
- 7045 — Service Installation
- Sysmon Event ID 10 — Process Access

## Detection Approach

The collected events were analyzed to identify suspicious authentication, process and remote access activity.

The observed activity was then mapped to relevant MITRE ATT&CK techniques.
