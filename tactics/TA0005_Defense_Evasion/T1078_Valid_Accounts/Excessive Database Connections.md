Excessive Database Connections


Notes
Rule detects an excessive number of successful database connections.

RULE:

APPLY Excessive Database Connections on events which are detected by the LOCAL system

AND when any of these BB:CategoryDefinition: Successful Database Connections with the same source IP more than 60 times, 
across exactly 1 destination IP within 1 minutes



BB define successful logins to databases: 

APPLY BB:CategoryDefinition: Successful Database Connections on events which are detected by the LOCAL system

AND when an event matches any of the following BB:DeviceDefinition: Database

AND when an event matches any of the following BB:CategoryDefinition: Authentication Success




BB: BB:DeviceDefinition: Database

APPLY BB:DeviceDefinition: Database on events which are detected by the LOCAL system

AND when the event(s) were detected by one or more of Oracle RDBMS Audit Record, Microsoft SQL Server, Application Security DbProtect, IBM DB2,
IBM Informix Audit, Oracle Audit Vault, Oracle Database Listener, Oracle Fine Grained Auditing, Sybase ASE



BB:CategoryDefinition: Authentication Success:

APPLY BB:CategoryDefinition: Authentication Success on events which are detected by the LOCAL system

AND when the event category for the event is one of the following Authentication.Admin Login Successful,
Authentication.Auth Server Login Succeeded, Authentication.Auth Server Session Opened,
Authentication.FTP Login Succeeded, Authentication.General Authentication Successful, 
Authentication.Host Login Succeeded, Authentication.Login with username/password defaults successful,
Authentication.Mail Service Login Succeeded, Authentication.Misc Login Succeeded,
Authentication.Remote Access Login Succeeded, Authentication.Samba Login Succeeded, 
Authentication.SSH Login Succeeded, Authentication.System Security Access Granted, 
Authentication.Telnet Login Succeeded, Authentication.VoIP Login Succeeded, 
Authentication.Web Service Login Succeeded, Authentication.Database Login Succeeded,
Authentication.IKE Authentication Succeeded, Authentication.RADIUS Authentication Succeeded,
Authentication.Station authentication succeeded, Authentication.TACACS Authentication Succeeded,
Authentication.User Login Success, Authentication.SFTP Login Succeeded

