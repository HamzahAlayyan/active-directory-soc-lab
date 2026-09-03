# Attack Detection

## Objective

Validate whether controlled attack activity generated observable security telemetry that could be identified through SIEM analysis.

## Attack Activity

Controlled security testing was performed within the isolated lab environment.

![Attack Execution](../screenshots/attacks/attack-execution.png)

## Telemetry Generated

The activity generated Windows and/or Sysmon telemetry that was subsequently analysed in Splunk.

![Attack Telemetry](../screenshots/attacks/attack-telemetry-splunk.png)

## Detection

The resulting events were searched and filtered within Splunk to identify activity associated with the simulated behaviour.

## Investigation

The investigation considered:

- Event timestamps
- Source system
- Target system
- User account
- Process information
- Related security events

## MITRE ATT&CK

Where applicable, the observed activity can be mapped to relevant MITRE ATT&CK techniques.

The technique mapping should be based on the specific activity performed during the simulation rather than assumed from the tool used.

## Result

The exercise demonstrated the complete security monitoring workflow:

**Attack Activity → Endpoint Telemetry → SIEM Ingestion → Detection → Investigation**
