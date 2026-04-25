# Velveteen Endpoint Investigation

## Overview

This project presents a structured investigation of suspicious endpoint activity involving persistence, script-based execution, and external communication.

The analysis was conducted using a custom-built threat hunting framework (**Velveteen**) and focuses on correlating technical indicators into a complete and coherent attack chain.

---

## What This Project Demonstrates

* Identification of persistence mechanisms (scheduled tasks)
* Analysis of PowerShell-based execution techniques
* Detection of suspicious file artifacts (DLL side-loading indicators)
* Correlation of endpoint, file, and network activity
* Translation of technical findings into structured intelligence reporting

---

## Key Findings

* PowerShell execution using `ExecutionPolicy Bypass`
* Persistence established via scheduled task (`WinReconService`)
* Suspicious DLL artifacts consistent with side-loading behavior
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

## Investigation Approach

The investigation followed a structured DFIR workflow:

1. Process and script analysis
2. Persistence identification
3. File artifact inspection
4. Network activity correlation
5. Behavioral interpretation

This approach allowed individual signals to be connected into a full intrusion lifecycle.

---

## Tools & Methods

* PowerShell analysis
* Log inspection
* Persistence analysis (scheduled tasks, autoruns)
* Indicator correlation
* MITRE ATT&CK mapping

---

## MITRE ATT&CK Techniques

* **T1053.005** – Scheduled Task
* **T1086** – PowerShell
* **T1218.011** – DLL Side-Loading
* **T1071.001** – Web Protocols

---

## Additional Documentation

* [Attack Chain Breakdown](attack_chain.md)
* [Report Excerpt](report_excerpt.md)
* [Velveteen Framework Overview](velveteen_overview.md)

---

## About Velveteen

Velveteen is a modular endpoint detection and threat hunting framework designed to:

* Identify suspicious system behavior
* Analyze persistence mechanisms
* Correlate activity across system layers
* Support structured forensic investigation

It combines elements of Endpoint Detection & Response (EDR), threat hunting workflows, and forensic analysis.

---

## Key Insight

This project highlights that effective threat detection requires:

* Correlation across multiple system layers
* Understanding attacker behavior, not just indicators
* Translating technical signals into a clear analytical narrative

---

## Notes

This project is a sanitized and generalized case study derived from real-world analysis patterns. All identifiers and sensitive details have been removed.

---
