# SOC Detection + Response Lab

## Overview

This project demonstrates an end-to-end Security Operations Center (SOC) detection and response workflow using **Sysmon** and **Splunk**. Realistic attacker behavior was simulated against a Windows endpoint, telemetry was ingested into Splunk, and multiple behavioral detections were engineered, validated, and documented.

The focus of this lab is **detection engineering**, **alert validation**, and **investigation workflows**, mirroring real-world SOC operations.

---

## Architecture

**Attacker:** Kali Linux
**Endpoint:** Windows Server with Sysmon + Splunk Universal Forwarder
**SIEM:** Splunk Enterprise (Ubuntu)

Telemetry is generated through controlled attack simulations and analyzed using behavioral detection logic.

---

## Detection Coverage

| # | Detection Name                | Technique                               |
| - | ----------------------------- | --------------------------------------- |
| 1 | Suspicious Network Connection | Unexpected inbound/outbound connections |
| 2 | Multi-Port Reconnaissance     | Port scanning / network discovery       |
| 3 | Abnormal Process Creation     | Non-interactive PowerShell execution    |
| 4 | PowerShell Abuse              | Obfuscation and stealth flags           |
| 5 | Suspicious Parent–Child Chain | LOLBin execution chains                 |

---

## Tools Used

* Sysmon
* Splunk Enterprise
* Splunk Universal Forwarder
* Kali Linux
* PowerShell

---

## Key Skills Demonstrated

* Detection engineering (behavior-based SPL)
* Sysmon telemetry analysis
* SOC investigation workflows
* Alert validation and tuning
* Incident documentation

---

## Repository Structure

```
soc-detection-response-lab/
├── README.md
├── architecture/
│   └── architecture-diagram.png
├── detections/
│   ├── multi-port-recon.spl
│   ├── abnormal-powershell-execution.spl
│   ├── powershell-abuse-flags.spl
│   └── suspicious-parent-child-chain.spl
├── evidence/
│   ├── detection2-multiport-recon.png
│   ├── detection3-abnormal-powershell.png
│   ├── detection4-powershell-abuse.png
│   └── detection5-parent-child-chain.png
└── incident-report/
    └── incident-report.md
```

---

## Outcome

This lab simulates real SOC workflows from attacker activity through detection, investigation, and response documentation, producing a portfolio artifact suitable for **SOC Analyst**, **Detection Engineer**, or **Security Engineer** roles.

