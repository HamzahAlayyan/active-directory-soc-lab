# Sysmon Endpoint Monitoring

## Overview

Sysmon was deployed to provide additional visibility into activity occurring on the Windows endpoint.

Unlike standard Windows security logging, Sysmon provides detailed telemetry that can assist with investigating process execution and other endpoint activity.

## Sysmon Operational Log

Sysmon events were reviewed through the Windows Event Viewer under:

`Applications and Services Logs → Microsoft → Windows → Sysmon → Operational`

## Security Monitoring Value

Process creation telemetry can help analysts identify suspicious programs, unusual parent-child process relationships, command execution, and potentially malicious activity.

## SIEM Integration

Sysmon telemetry was forwarded to Splunk where it could be searched alongside Windows security events.

This allowed endpoint activity to be investigated within the same SIEM environment as authentication events.
