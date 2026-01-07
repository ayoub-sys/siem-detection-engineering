
Reports multiple log in failures to a single host, followed by a successful log in to the host. 

RULE:

APPLY Login Failures Followed By Success from the same Source IP on events which are detected by the LOCAL system

AND when BB:CategoryDefinition: Authentication Success match at least 1 times in 5 minutes after any of Multiple Login Failures from the Same Source match with the same Source IP


BB:CategoryDefinition: Authentication Succes: 

APPLY BB:CategoryDefinition: Authentication Success on events which are detected by the LOCAL system

AND when the event category for the event is one of the following Authentication.Admin Login Successful,
Authentication.Auth Server Login Succeeded, Authentication.Auth Server Session Opened, Authentication.FTP Login Succeeded, 
Authentication.General Authentication Successful, Authentication.Host Login Succeeded, 
Authentication.Login with username/password defaults successful, Authentication.Mail Service Login Succeeded,
Authentication.Misc Login Succeeded, Authentication.Remote Access Login Succeeded, 
Authentication.Samba Login Succeeded, Authentication.SSH Login Succeeded, 
Authentication.System Security Access Granted, Authentication.Telnet Login Succeeded,
Authentication.VoIP Login Succeeded, Authentication.Web Service Login Succeeded, 
Authentication.Database Login Succeeded, Authentication.IKE Authentication Succeeded,
Authentication.RADIUS Authentication Succeeded, Authentication.Station authentication succeeded, 
Authentication.TACACS Authentication Succeeded, Authentication.User Login Success, Authentication.SFTP Login Succeeded


RULE: Multiple Login Failures from the Same Source 

AND when an event matches any of the following BB:CategoryDefinition: Authentication Failures

AND when at least 10 events are seen with the same Source IP and different Username in 5 minutes
APPLY Multiple Login Failures from the Same Source on events which are detected by the LOCAL system

AND when an event matches any of the following BB:CategoryDefinition: Authentication Failures

AND when at least 10 events are seen with the same Source IP and different Username in 5 minutes



BB:CategoryDefinition: Authentication Failures

APPLY BB:CategoryDefinition: Authentication Failures on events which are detected by the LOCAL system

AND when the event category for the event is one of the following Authentication.Admin Login Failure,
Authentication.Auth Server Login Failed, Authentication.FTP Login Failed,
Authentication.General Authentication Failed, Authentication.Host Login Failed,
Authentication.Login with username/password defaults failed,
Authentication.Mail Service Login Failed, Authentication.Misc Login Failed,
Authentication.Password Change Failed, Authentication.Privilege Escalation Failed,
Authentication.Remote Access Login Failed, Authentication.Samba Login Failed,
Authentication.SSH Login Failed, Authentication.Telnet Login Failed,
Authentication.VoIP Login Failed, Authentication.Web Service Login Failed,
Authentication.Database Login Failed, Authentication.IKE Authentication Failed,
Authentication.RADIUS Authentication Failed, Authentication.TACACS Authentication Failed,
Authentication.User Login Failure, Authentication.Station authentication failed
