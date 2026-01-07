

Reports authentication failures on the same destination IP address more than ten times,
from more than 10 source IP addresses within 10 minutes. 



RULE:

APPLY Multiple Login Failures to the Same Destination on events which are detected by the LOCAL system

AND when an event matches any of the following BB:CategoryDefinition: Authentication Failures

AND when at least 10 events are seen with the same Destination IP and different Source IP, Username in 5 minutes


BB:CategoryDefinition: Authentication Failures: 

APPLY BB:CategoryDefinition: Authentication Failures on events which are detected by the LOCAL system

AND when the event category for the event is one of the following Authentication.Admin Login Failure,
Authentication.Auth Server Login Failed, Authentication.FTP Login Failed, Authentication.General Authentication Failed,
Authentication.Host Login Failed, Authentication.Login with username/password defaults failed, 
Authentication.Mail Service Login Failed, Authentication.Misc Login Failed,
Authentication.Password Change Failed, Authentication.Privilege Escalation Failed,
Authentication.Remote Access Login Failed, Authentication.Samba Login Failed,
Authentication.SSH Login Failed, Authentication.Telnet Login Failed, Authentication.VoIP Login Failed,
Authentication.Web Service Login Failed, Authentication.Database Login Failed,
Authentication.IKE Authentication Failed, Authentication.RADIUS Authentication Failed,
Authentication.TACACS Authentication Failed,
Authentication.User Login Failure, Authentication.Station authentication failed

