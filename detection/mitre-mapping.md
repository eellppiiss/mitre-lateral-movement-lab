# MITRE ATT&CK Mapping

## Lateral Movement Techniques

The investigated activity was mapped to the MITRE ATT&CK framework.

| Technique | ID | Description | Detection Approach |
|---|---|---|---|
| Pass the Hash | T1550.002 | Authentication using a valid NTLM hash | Correlate authentication events with suspicious process activity |
| Remote Services | T1021 | Lateral movement using remote services | Analyze remote authentication and service activity |
| Remote Desktop Protocol | T1021.001 | Lateral movement using RDP | Monitor RDP authentication events |
| SMB / Windows Admin Shares | T1021.002 | Lateral movement using SMB and administrative shares | Analyze network logons and access to administrative shares |
| Windows Remote Management | T1021.006 | Remote command execution using WinRM | Monitor WinRM-related activity and process creation |
| Windows Management Instrumentation | T1047 | Remote execution using WMI | Analyze WMI activity and process creation |
| Lateral Tool Transfer | T1570 | Transfer of tools between systems | Monitor file transfers and suspicious process execution |

## Main Investigated Technique

**T1550.002 — Pass the Hash**

Pass the Hash was the main technique investigated during the laboratory exercise.

The activity was analyzed using Windows Security Event Logs and Sysmon telemetry.

## Detection

Detection should combine multiple sources of telemetry rather than relying on a single event.

Relevant data sources include:

- Windows Security Event Logs
- Sysmon
- Process creation events
- Authentication events
- Privilege assignment events
- Process access events

## Conclusion

MITRE ATT&CK provides a structured way to describe and classify observed Lateral Movement activity.

Mapping security events to ATT&CK techniques helps organize investigation and identify potential detection opportunities.
