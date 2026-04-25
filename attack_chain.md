# Attack Chain Breakdown

This document provides a structured breakdown of the attack sequence identified during analysis.

## Stages

1. **Initial Execution**
   PowerShell script executed with execution policy bypass

2. **Persistence**
   Scheduled task created to ensure repeated execution

3. **Reconnaissance**
   Script performs system-level data collection

4. **Defense Evasion**
   DLL side-loading used for stealth execution

5. **Command & Control**
   Outbound encrypted communication established

6. **Sustained Access**
   Combined persistence and communication enable continued access

## Key Insight

Individually, these events may appear benign.
Together, they form a complete intrusion workflow.
