***Evidence***

This folder contains screenshots captured during alert triggering, detection validation, and investigation workflows.
Screenshots are ordered to reflect the SOC investigation timeline, starting from the initial alert and progressing through correlated detections.

alert-fired.png
Initial Splunk alert confirming detection logic successfully triggered.

detection2-multiport-recon.png
Detection of suspicious multi-port network activity indicative of reconnaissance behavior (Sysmon Event ID 3).

detection3-abnormal-powershell.png
Abnormal PowerShell execution detected based on non-standard parent process and execution context (Sysmon Event ID 1).

detection4-powershell-abuse.png
PowerShell abuse identified using suspicious command-line flags such as -nop, -w hidden, and encoded commands.

detection5-parent-child-chain.png
Parent–child process chain analysis highlighting suspicious execution paths (e.g., cmd.exe → powershell.exe).
