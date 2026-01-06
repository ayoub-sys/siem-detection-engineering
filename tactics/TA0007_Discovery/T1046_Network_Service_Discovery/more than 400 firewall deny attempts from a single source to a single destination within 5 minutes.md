Reports excessive firewall denies from a single host. 
Detects more than 400 firewall deny attempts from a single source to a single destination within 5 minutes. 

RULE:

APPLY Excessive Firewall Denies from Single Source on events which are detected by the LOCAL system

AND NOT when an event matches any of the following BB:HostDefinition: Servers

AND when any of these BB:CategoryDefinition: Firewall or ACL Denies with the same source IP more than 400 times, across exactly 1 destination IP within 5 minutes
