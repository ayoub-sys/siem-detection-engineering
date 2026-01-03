Reports a DoS attack against a local target that is known to exist and the target port is open. 

Rule:
APPLY Service DoS Attack Detected on events which are detected by the LOCAL system 
AND when an event matches any of the following BB:HostDefinition: Host with Port Open 
AND when the event category for the event is one of the following DOS.Database DoS, DOS.DNS Service DoS, 
DOS.FTP DoS, DOS.Mail Service DoS, DOS.Telnet DoS, DOS.Unix DOS, DOS.Web Service DoS, DOS.Windows DoS

BB:HostDefinition: Host with Port Open 

Apply BB:HostDefinition: Host with Port Open on events or flows which are detected by the Local system
and when the local destination host destination port is open either actively or passively seen
