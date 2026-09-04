# MITRE ATT&CK Lateral Movement Lab

Practical cybersecurity lab for studying and detecting Lateral Movement techniques in Windows.

## About

This project focuses on the analysis of Lateral Movement techniques using MITRE ATT&CK, Windows Event Logs and Sysmon.

The main investigated technique was Pass the Hash (T1550.002).

## Technologies

- Windows 10
- Active Directory
- MITRE ATT&CK
- Sysmon
- Windows Event Logs
- Mimikatz
- PowerShell

## Lab

The project included:

- setting up an isolated Windows lab environment
- configuring Windows logging and Sysmon
- simulating Pass the Hash activity
- collecting and analyzing security events
- identifying suspicious activity
- mapping observations to MITRE ATT&CK

## Detection

Analyzed Windows Security Event IDs:

- 4624 — Successful Logon
- 4625 — Failed Logon
- 4648 — Explicit Credential Logon
- 4672 — Special Privileges Assigned
- 4688 — Process Creation
- 4776 — Credential Validation
- 7045 — Service Installation

Sysmon Event ID 10 was also analyzed for process access activity.

## MITRE ATT&CK

Main technique:

**T1550.002 — Pass the Hash**

Other Lateral Movement techniques studied:

- Remote Services
- RDP
- SMB / Windows Admin Shares
- WinRM
- WMI

## Result

The project demonstrates how Windows Event Logs and Sysmon can be used to investigate and detect suspicious Lateral Movement activity.

## Disclaimer

This project was created for educational purposes in an isolated laboratory environment.
