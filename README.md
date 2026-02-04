# SOC Detection + Response Lab

## Overview
This project demonstrates an end-to-end Security Operations Center (SOC) workflow, from detection engineering to incident response. The lab simulates realistic attacker behavior against a Windows endpoint and uses Sysmon telemetry ingested into Splunk to detect, investigate, and respond to suspicious activity.

## Architecture
- **Attacker:** Kali Linux
- **Endpoint:** Windows Server with Sysmon + Splunk Universal Forwarder
- **SIEM:** Splunk Enterprise (Ubuntu)

All telemetry is generated through controlled attack simulation and analyzed using behavioral detection logic.

## Objectives
- Generate real attacker network activity
- Ingest endpoint telemetry into Splunk
- Build and operationalize detections
- Trigger and investigate alerts
- Perform containment and response actions

## Detection Summary
The primary detection identifies repeated external TCP connections to a Windows endpoint, which may indicate reconnaissance or unauthorized access attempts.

## Tools Used
- Sysmon
- Splunk Enterprise
- Splunk Universal Forwarder
- Kali Linux
- PowerShell

## Key Skills Demonstrated
- Detection engineering
- SIEM alerting
- SOC investigation
- Incident response decision-making
- Security telemetry analysis
