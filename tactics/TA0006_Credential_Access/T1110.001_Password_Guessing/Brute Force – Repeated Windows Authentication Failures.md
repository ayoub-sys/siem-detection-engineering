

Reports when a source IP address causes an authentication failure event at least 7 times to a single destination within 5 minutes. 

Rule:

APPLY Repeat Windows Login Failures on events which are detected by the LOCAL system 
AND  when the event(s) were detected by one or more of Microsoft Windows Security Event Log 
AND when BB:CategoryDefinition: Authentication Failures match at least 7 times with the same Source IP, Destination IP, Event Name in 5 minutes

* BB:CategoryDefinition: Authentication Failures

Apply BB:CategoryDefinition: Authentication Failures on events which are detected by the Local system
and when the event category for the event is one of the following Authentication.Admin Login Failure,
Authentication.Auth Server Login Failed, Authentication.FTP Login Failed,
Authentication.General Authentication Failed, Authentication.Host Login Failed,
Authentication.Login with username/password defaults failed, Authentication.Mail Service Login Failed,
Authentication.Misc Login Failed, Authentication.Password Change Failed, Authentication.Privilege Escalation Failed,
Authentication.Remote Access Login Failed, Authentication.Samba Login Failed, Authentication.SSH Login Failed,
Authentication.Telnet Login Failed, Authentication.VoIP Login Failed, Authentication.Web Service Login Failed,
Authentication.Database Login Failed, Authentication.IKE Authentication Failed, Authentication.RADIUS Authentication Failed,
Authentication.TACACS Authentication Failed, Authentication.User Login Failure, Authentication.Station authentication failed
