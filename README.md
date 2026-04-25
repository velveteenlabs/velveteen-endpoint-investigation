# Velveteen Endpoint Investigation

## Overview

This project demonstrates a structured investigation of suspicious endpoint activity involving persistence, script-based execution, and external communication.

The analysis was conducted using a custom-built threat hunting framework (Velveteen) and focuses on correlating technical indicators into a complete attack chain.

---

## Key Findings

* PowerShell execution using execution policy bypass
* Persistence established via scheduled task (`WinReconService`)
* Suspicious DLL artifacts consistent with side-loading
* Outbound encrypted communication to flagged infrastructure

These findings indicate coordinated activity rather than isolated anomalies.

---

## Attack Chain

```text
[Initial Execution]
PowerShell Script (ExecutionPolicy Bypass)
        ↓
[Persistence]
Scheduled Task (WinReconService)
        ↓
[Reconnaissance]
Script-Based System Enumeration
        ↓
[Defense Evasion]
DLL Side-Loading
        ↓
[Command & Control]
Outbound Encrypted Traffic (Port 443)
        ↓
[Sustained Access]
Persistent Execution + External Communication
```

---

## Approach

The investigation followed a structured DFIR workflow:

* Process and script analysis
* Persistence identification
* File artifact inspection
* Network correlation
* Behavioral interpretation

---

## Tools & Methods

* PowerShell analysis
* Log inspection
* Persistence analysis (scheduled tasks)
* YARA-based detection concepts
* MITRE ATT&CK mapping

---

## MITRE ATT&CK Techniques

* T1053.005 – Scheduled Task
* T1086 – PowerShell
* T1218.011 – DLL Side-Loading
* T1071.001 – Web Protocols

---

## Project Focus

This project emphasizes:

* Correlating multiple indicators into a single attack chain
* Understanding attacker behavior beyond surface-level signals
* Translating technical findings into structured analysis

---

## Notes

This project is a sanitized and generalized case study derived from real-world analysis patterns. All identifiers and sensitive details have been removed.

---
