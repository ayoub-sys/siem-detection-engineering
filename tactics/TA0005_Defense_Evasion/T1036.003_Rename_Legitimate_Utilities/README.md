# T1036.003 – Rename Legitimate Utilities

## Tactic
TA0005 – Defense Evasion

## Description
Adversaries may rename legitimate / system utilities to try to evade security mechanisms concerning the usage of those utilities. Security monitoring and control mechanisms may be in place for legitimate utilities adversaries are capable of abusing, including both built-in binaries and tools such as PSExec, AutoHotKey, and IronPython.(Citation: LOLBAS Main Site)(Citation: Huntress Python Malware 2025)(Citation: The DFIR Report AutoHotKey 2023)(Citation: Splunk Detect Renamed PSExec) It may be possible to bypass those security mechanisms by renaming the utility prior to utilization (ex: rename <code>rundll32.exe</code>).(Citation: Elastic Masquerade Ball) An alternative case occurs when a legitimate utility is copied or moved to a different directory and renamed to avoid detections based on these utilities executing from non-standard paths.(Citation: F-Secure CozyDuke)

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1036.003/
