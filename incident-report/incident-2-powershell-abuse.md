# Incident Report — Suspicious PowerShell Activity

## Summary

Multiple alerts were triggered indicating suspicious PowerShell execution on a Windows endpoint. The activity included abnormal process execution, PowerShell abuse flags, and suspicious parent–child process relationships.

---

## Timeline (UTC)

* **T0:** Multi-port network reconnaissance detected
* **T1:** PowerShell executed from non-interactive parent process
* **T2:** PowerShell executed with `-nop`, `-w hidden`, and encoded commands
* **T3:** Repeated suspicious execution chain observed (`cmd.exe → powershell.exe`)

---

## Detection Summary

| Detection                     | Result    |
| ----------------------------- | --------- |
| Multi-Port Recon              | Triggered |
| Abnormal Process Creation     | Triggered |
| PowerShell Abuse Flags        | Triggered |
| Suspicious Parent–Child Chain | Triggered |

---

## Investigation Findings

* PowerShell executions were not initiated by `explorer.exe`
* Commands used stealth and obfuscation techniques
* Execution chains matched known attacker tradecraft
* No evidence of persistence or lateral movement observed in this lab

---

## Response Actions (Simulated)

* Alert triaged and confirmed malicious behavior
* Endpoint flagged for containment
* Recommendation to isolate host from network
* Recommendation to reset credentials and review PowerShell logging policies

---

## Lessons Learned

* Behavioral detections reduce false positives
* Parent–child process analysis provides strong signal
* PowerShell abuse is a high-confidence indicator of compromise

---

## Conclusion

This incident demonstrates the effectiveness of Sysmon telemetry combined with Splunk detection engineering to identify attacker techniques early in the attack lifecycle.
