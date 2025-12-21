# T1070.002 – Clear Linux or Mac System Logs

## Tactic
TA0005 – Defense Evasion

## Description
Adversaries may clear system logs to hide evidence of an intrusion. macOS and Linux both keep track of system or user-initiated actions via system logs. The majority of native system logging is stored under the <code>/var/log/</code> directory. Subfolders in this directory categorize logs by their related functions, such as:(Citation: Linux Logs)

* <code>/var/log/messages:</code>: General and system-related messages
* <code>/var/log/secure</code> or <code>/var/log/auth.log</code>: Authentication logs
* <code>/var/log/utmp</code> or <code>/var/log/wtmp</code>: Login records
* <code>/var/log/kern.log</code>: Kernel logs
* <code>/var/log/cron.log</code>: Crond logs
* <code>/var/log/maillog</code>: Mail server logs
* <code>/var/log/httpd/</code>: Web server access and error logs

## Data Sources
N/A

## Detection Ideas
- TODO

## False Positives
- TODO

## Response Actions
- TODO

## References
- https://attack.mitre.org/techniques/T1070.002/
