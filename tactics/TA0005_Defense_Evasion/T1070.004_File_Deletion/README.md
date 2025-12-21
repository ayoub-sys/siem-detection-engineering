# T1070.004 – File Deletion

## Tactic
TA0005 – Defense Evasion

## Description
Adversaries may delete files left behind by the actions of their intrusion activity. Malware, tools, or other non-native files dropped or created on a system by an adversary (ex: [Ingress Tool Transfer](https://attack.mitre.org/techniques/T1105)) may leave traces to indicate to what was done within a network and how. Removal of these files can occur during an intrusion, or as part of a post-intrusion process to minimize the adversary's footprint.

There are tools available from the host operating system to perform cleanup, but adversaries may use other tools as well.(Citation: Microsoft SDelete July 2016) Examples of built-in [Command and Scripting Interpreter](https://attack.mitre.org/techniques/T1059) functions include <code>del</code> on Windows, <code>rm</code> or <code>unlink</code> on Linux and macOS, and `rm` on ESXi.

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1070.004/
