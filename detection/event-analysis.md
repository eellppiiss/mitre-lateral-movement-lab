# Windows Event Analysis

## Overview

Windows Security Event Logs and Sysmon telemetry were used to investigate suspicious activity related to Lateral Movement.

The analysis focused on authentication events, process creation, privilege assignment and process access activity.

## Windows Security Events

| Event ID | Description | Detection Relevance |
|---|---|---|
| 4624 | Successful Logon | Can indicate successful authentication to a system |
| 4625 | Failed Logon | Can indicate failed authentication attempts |
| 4648 | Explicit Credential Logon | Indicates the use of explicit credentials |
| 4672 | Special Privileges Assigned | Indicates assignment of special privileges |
| 4688 | Process Creation | Useful for identifying suspicious processes and command execution |
| 4776 | Credential Validation | Provides information about credential validation |
| 7045 | Service Installation | Can indicate creation of a new Windows service |

## Sysmon

Sysmon was used to provide additional endpoint telemetry.

### Event ID 10 — Process Access

Sysmon Event ID 10 records process access activity.

This event can be useful for detecting suspicious access to sensitive processes such as LSASS.

## Detection Logic

Individual events should not always be treated as malicious on their own.

A more effective approach is to correlate multiple events and examine:

- unusual authentication activity
- successful logons following failed attempts
- use of explicit credentials
- unexpected privilege assignment
- suspicious process creation
- process access to sensitive processes
- unexpected service installation

## Investigation

The collected events were reviewed in Windows Event Viewer and Sysmon logs.

The observed activity was analyzed in the context of the simulated Pass the Hash scenario and mapped to the corresponding MITRE ATT&CK technique.

## Conclusion

Windows Security Event Logs combined with Sysmon provide useful telemetry for investigating suspicious Lateral Movement activity.

Event correlation and contextual analysis can help distinguish normal administrative activity from potentially malicious behavior.
