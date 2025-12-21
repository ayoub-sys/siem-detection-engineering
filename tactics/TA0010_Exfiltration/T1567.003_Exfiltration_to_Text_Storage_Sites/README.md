# T1567.003 – Exfiltration to Text Storage Sites

## Tactic
TA0010 – Exfiltration

## Description
Adversaries may exfiltrate data to text storage sites instead of their primary command and control channel. Text storage sites, such as <code>pastebin[.]com</code>, are commonly used by developers to share code and other information.  

Text storage sites are often used to host malicious code for C2 communication (e.g., [Stage Capabilities](https://attack.mitre.org/techniques/T1608)), but adversaries may also use these sites to exfiltrate collected data. Furthermore, paid features and encryption options may allow adversaries to conceal and store data more securely.(Citation: Pastebin EchoSec)

**Note:** This is distinct from [Exfiltration to Code Repository](https://attack.mitre.org/techniques/T1567/001), which highlight access to code repositories via APIs.

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1567.003/
