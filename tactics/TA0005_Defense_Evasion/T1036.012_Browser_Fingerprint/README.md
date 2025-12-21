# T1036.012 – Browser Fingerprint

## Tactic
TA0005 – Defense Evasion

## Description
Adversaries may attempt to blend in with legitimate traffic by spoofing browser and system attributes like operating system, system language, platform, user-agent string, resolution, time zone, etc.  The HTTP User-Agent request header is a string that lets servers and network peers identify the application, operating system, vendor, and/or version of the requesting user agent.(Citation: Mozilla User Agent)

Adversaries may gather this information through [System Information Discovery](https://attack.mitre.org/techniques/T1082) or by users navigating to adversary-controlled websites, and then use that information to craft their web traffic to evade defenses.(Citation: Gummy Browsers: Targeted Browser Spoofing against State-of-the-Art Fingerprinting Techniques)

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1036.012/
