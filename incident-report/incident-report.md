# Incident Report – Suspicious Network Activity

## Incident Summary
A Splunk alert triggered after detecting repeated TCP connections from an external source IP to a Windows endpoint. The activity was identified through Sysmon network telemetry and reviewed to determine scope and impact.

## Detection Source
- Splunk Enterprise
- Sysmon Event ID 3 (Network Connection)

## Timeline (UTC)
- Initial detection: 2026-02-03
- Activity duration: Short burst of repeated connections

## Investigation Findings
- Source IP: External host
- Target: Single Windows endpoint
- Ports targeted: TCP 4444
- Process involved: PowerShell
- Scope: Limited to one host, no lateral movement observed

## Containment Actions
- Blocked the source IP to prevent further connection attempts
- Placed the affected host under enhanced monitoring

## Eradication
No eradication was required as no evidence of exploitation or persistence was found.

## Recovery
The system was returned to normal monitoring after validation.

## Lessons Learned
- Behavioral detections are effective for identifying early-stage reconnaissance
- Accurate SIEM scoping is critical to avoid false negatives
- Sysmon provides valuable visibility into endpoint network activity
