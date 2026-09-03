# Attack Simulation

## Overview

A controlled RDP brute-force simulation was performed within the isolated lab environment to generate realistic authentication telemetry for security monitoring and investigation.

## Objective

The objective was to simulate repeated authentication attempts against a Remote Desktop Protocol (RDP) service and analyse the resulting Windows security events through Splunk.

## Attack Execution

The attack was performed against the Windows environment using repeated password attempts against the RDP service.

![Attack Execution](../screenshots/attacks/attack-execution.png)

The activity was performed exclusively within the isolated lab environment for security testing and educational purposes.

## Resulting Telemetry

The repeated authentication attempts generated Windows Security Event ID 4625 events representing failed logon attempts.

The resulting telemetry was collected and analysed through Splunk.

![Attack Telemetry](../screenshots/attacks/attack-telemetry-splunk.png)

## Detection

The generated authentication events were searched and filtered in Splunk to identify repeated failed logon attempts.

The investigation focused on:

- Timestamp
- User account
- Source system
- Target system
- Logon information
- Number of failed attempts
- Frequency of authentication failures

## MITRE ATT&CK Mapping

The simulated activity can be mapped to the following MITRE ATT&CK techniques:

| Technique | Description |
|---|---|
| T1110 | Brute Force |
| T1110.001 | Password Guessing |
| T1021.001 | Remote Services: Remote Desktop Protocol |

Windows Security Event ID 4625 was used as the primary telemetry source for identifying the failed authentication attempts.

## Outcome

The simulation demonstrated how controlled attack activity can generate observable endpoint telemetry that can subsequently be ingested, detected, and investigated within a SIEM.

**RDP Brute Force → Event ID 4625 → Splunk → Detection → Investigation**
