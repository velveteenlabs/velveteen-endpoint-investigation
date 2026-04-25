# Analyst Perspective

This investigation focused on determining whether a set of unusual system behaviors represented benign activity or a coordinated intrusion.

The key turning point was identifying a scheduled task configured to execute a PowerShell script at user logon. This indicated persistence, which strongly suggests intentional and repeatable system interaction.

From there, the analysis shifted toward correlating multiple indicators:

* PowerShell execution with execution policy bypass
* Persistence via scheduled task
* Suspicious file artifacts consistent with DLL side-loading
* Outbound encrypted communication to external infrastructure

Individually, these signals could be explained as benign. When analyzed together, they form a sequence consistent with a structured attack chain.

This project reinforced the importance of:

* Correlating signals across multiple system layers
* Evaluating persistence mechanisms as indicators of intent
* Interpreting technical activity through a behavioral lens

The goal was not attribution, but understanding capability and behavior through observable evidence.
