# Lab Setup

## Overview

The lab was designed as an isolated virtualised environment for practicing Active Directory administration, Windows security monitoring, SIEM analysis, and controlled attack simulation.

## Lab Components

| System | Role |
|---|---|
| Windows Server 2022 | Active Directory Domain Controller |
| Windows 10 Pro | Domain-joined endpoint |
| Splunk | SIEM and log analysis |
| Kali Linux | Security testing and attack simulation |

## Network Architecture

The systems communicate within an isolated lab network. The Active Directory Domain Controller provides domain services to the Windows endpoint, while security telemetry is collected for analysis through Splunk.

![Network Architecture](../architecture/network-diagram.png)

## Lab Objectives

The environment was created to provide practical experience with:

- Active Directory administration
- Windows endpoint configuration
- Security event collection
- Endpoint telemetry
- SIEM analysis
- Attack simulation
- Detection engineering

## Security Considerations

The environment is intended for controlled security testing and educational purposes. Attack simulations were performed against systems within the isolated lab environment rather than production infrastructure.
