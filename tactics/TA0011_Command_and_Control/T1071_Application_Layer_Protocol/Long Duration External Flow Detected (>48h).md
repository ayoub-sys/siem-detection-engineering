Detects a flow communicating to the Internet with a sustained duration of more than 48 hours. 
This is not typical behavior for most applications.
Investigate the host for potential malware infections.

Rule:

APPLY Remote: Long Duration Flow Detected on flows which are detected by the LOCAL system

AND NOT when the flow context is Local to Local

AND when the flow duration is greater than 48 hours
