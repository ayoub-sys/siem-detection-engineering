

Potential Local port scan detected

Rule:

APPLY Potential Local Port Scan Detected on events or flows which are detected by the LOCAL system

AND NOT when a flow or an event matches any of the following BB:HostDefinition: Servers

AND when the context is Local to Local

AND when any of these BB:CategoryDefinition: Recon Events, BB:CategoryDefinition: Suspicious Events with the same source IP more than 5 times, across more than 100 destination port within 3 minutes


