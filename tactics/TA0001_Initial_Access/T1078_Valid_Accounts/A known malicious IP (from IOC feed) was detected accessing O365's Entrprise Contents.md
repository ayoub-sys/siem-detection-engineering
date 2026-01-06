

RULE:


APPLY A known malicious IP (from IOC feed) was detected accessing 0365's Entreprise Contents on events which are detected by the LOCAL system

AND when the event(s) were detected by one or more of Microsoft Office 365

AND when any of Source IP, ClientIP (custom), Destination IP are contained in any of KnownMaliciousIP - IP

KnownMaliciousIP - IP: a reference set

