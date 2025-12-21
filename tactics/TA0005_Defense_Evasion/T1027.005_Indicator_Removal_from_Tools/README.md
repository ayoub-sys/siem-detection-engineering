# T1027.005 – Indicator Removal from Tools

## Tactic
TA0005 – Defense Evasion

## Description
Adversaries may remove indicators from tools if they believe their malicious tool was detected, quarantined, or otherwise curtailed. They can modify the tool by removing the indicator and using the updated version that is no longer detected by the target's defensive systems or subsequent targets that may use similar systems.

A good example of this is when malware is detected with a file signature and quarantined by anti-virus software. An adversary who can determine that the malware was quarantined because of its file signature may modify the file to explicitly avoid that signature, and then re-use the malware.

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1027.005/
