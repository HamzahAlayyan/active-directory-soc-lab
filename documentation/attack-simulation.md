# Attack Simulation

## Overview

Controlled attack simulations were performed within the isolated lab environment to generate security telemetry and evaluate the effectiveness of the monitoring configuration.

## Objective

The objective was to generate realistic security events and investigate the resulting telemetry using Splunk.

## Attack Execution

The security testing system was used to perform controlled activity against the lab environment.
(RDP Brute Force)

![Attack Execution](../screenshots/attacks/attack-execution.png)

## Resulting Telemetry

The simulated activity generated security events that were collected and analysed through Splunk.

![Attack Telemetry](../screenshots/attacks/attack-telemetry-splunk.png)

## Investigation

The resulting events were investigated by examining:

- Event timestamps
- User accounts
- Source systems
- Process information
- Related Windows security events

## Detection

The generated telemetry was used to develop and validate detection logic.

The investigation demonstrated how activity performed on an endpoint can generate multiple telemetry sources that can subsequently be analysed by a SOC analyst.

## Outcome

The exercise provided practical experience with the relationship between attack activity, endpoint telemetry, SIEM ingestion, detection logic, and security investigation.
