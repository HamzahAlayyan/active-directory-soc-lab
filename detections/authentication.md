# Authentication Detection

## Objective

Detect repeated failed authentication attempts that may indicate password guessing, brute-force activity, or other suspicious authentication behaviour.

## Data Source

Windows Security Event ID 4625 was used to identify failed logon attempts.

## Detection Logic

The detection searches for failed authentication events and identifies repeated attempts involving the same account, source system, or target system.

The detection was validated using the controlled RDP brute-force simulation performed within the lab environment.

## RDP Brute-Force Detection

During the simulation, repeated password attempts against the RDP service generated multiple Event ID 4625 events.

These events provided the telemetry required to identify the simulated password-guessing activity.

![Multiple Failed Logins](../screenshots/splunk/failed-logon-event.png)

## Investigation

When investigating repeated failed authentication attempts, the following information should be reviewed:

- Username
- Source system
- Destination computer
- Logon type
- Failure reason
- Timestamp
- Number of attempts
- Frequency of attempts

The combination of repeated failures, timing, account information, and source system can help determine whether the activity is consistent with password-guessing behaviour.

## MITRE ATT&CK Mapping

| Item | Mapping |
|---|---|
| Tactic | Credential Access |
| Technique | T1110 – Brute Force |
| Sub-technique | T1110.001 – Password Guessing |
| Targeted Service | T1021.001 – Remote Services: Remote Desktop Protocol |
| Telemetry | Windows Security Event ID 4625 |

The simulated attack involved repeated password attempts against an RDP service. Failed authentication attempts generated Windows Event ID 4625 events, which were collected and analysed in Splunk.

## Analyst Interpretation

A single failed authentication attempt may be benign. Multiple failures within a short period, particularly when targeting the same account or originating from the same source, may warrant further investigation.

In this lab, the repeated failures were generated intentionally as part of the controlled RDP brute-force simulation.

## Outcome

This detection demonstrates how Windows authentication telemetry can be used to identify and investigate potentially suspicious login behaviour within a SIEM environment.
