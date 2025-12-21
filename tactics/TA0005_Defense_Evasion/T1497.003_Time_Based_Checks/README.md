# T1497.003 – Time Based Checks

## Tactic
TA0005 – Defense Evasion

## Description
Adversaries may employ various time-based methods to detect virtualization and analysis environments, particularly those that attempt to manipulate time mechanisms to simulate longer elapses of time. This may include enumerating time-based properties, such as uptime or the system clock. 

Adversaries may use calls like `GetTickCount` and `GetSystemTimeAsFileTime` to discover if they are operating within a virtual machine or sandbox, or may be able to identify a sandbox accelerating time by sampling and calculating the expected value for an environment's timestamp before and after execution of a sleep function.(Citation: ISACA Malware Tricks)

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1497.003/
