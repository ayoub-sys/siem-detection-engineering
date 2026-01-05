Adds an additional event into the event stream when a host that has been performing reconnaissance 
also has a firewall accept following the reconnaissance activity.

An IP scans / probes (recon activity)

Then the same IP gets a firewall ACCEPT

All of this happens within 5 minutes

The activity is seen by local QRadar sensors

The accept comes from a network device (FW / Router / Switch)


Rule: 
APPLY Recon Followed by Accept on events or flows which are detected by the LOCAL system

AND when all of these BB:ReconDetected: Basic Recon Rules, BB:CategoryDefinition: Firewall or ACL Accept, in order, from the same source IP to any destination IP, over 5 minutes

AND when a flow or an event matches any of the following BB:DeviceDefinition: FW / Router / Switch


* BB:ReconDetected: Basic Recon Rules: 

APPLY BB:ReconDetected: Basic Recon Rules on events or flows which are detected by the LOCAL system

AND when a flow or an event matches any of the following Host Port Scan Detected by Remote Host, Local L2L Scanner Detected,
Remote Scanner Detected, Remote Windows Server Scanner, Local L2R RPC Server Scanner, Local L2R Windows Server Scanner,
Local L2R Scanner Detected, Local L2L Suspicious Probe Events Detected, Excessive Firewall Denies from Local Host

* Rule: Host Port Scan Detected by Remote Host

Reports when more than 400 ports were scanned from a single source IP address in under 2 minutes.
APPLY Host Port Scan Detected by Remote Host on events or flows which are detected by the LOCAL system

AND NOT when a flow or an event matches any of the following BB:HostDefinition: Servers

AND when the context is Remote to Local, Remote to Remote

AND when any of these BB:CategoryDefinition: Recon Events, BB:CategoryDefinition: Suspicious Events with the same source IP more than 5 times, across more than 50 destination port within 3 minutes

AND NOT when the event or flow matches Source Port is less than 1024

AND NOT when the event or flow matches Destination Port is greater than 7000

AND NOT when the event or flow matches Source Port is any of [8080 or 8081]

* BB:CategoryDefinition: Recon Events
  
APPLY BB:CategoryDefinition: Recon Events on events or flows which are detected by the LOCAL system

AND when a flow or an event matches any of the following 
BB:CategoryDefinition: Recon Event Categories, BB:CategoryDefinition: Recon Flows




APPLY BB:CategoryDefinition: Firewall or ACL Accept on events which are detected by the LOCAL system

AND when the event category for the event is one of the following Access.Firewall Permit, 
Access.ACL Permit, Access.Access Permitted, Access.Session Opened,
Application.AAA Session Started, Application.Auth Opened, Application.Chargen Session Started,
Application.Chat Opened, Application.CUPS Session Opened, Application.CVS Session Opened, 
Application.DAP Session Started, Application.Database Opened, Application.DHCP Session Opened, 
Application.Discard Session Opened, Application.DNP3 Session Opened, Application.DNS Opened, 
Application.Echo Session Opened, Application.FileTransfer Opened, Application.Finger Session Opened, 
Application.FTP Opened, Application.GIOP Session Opened, Application.Gopher Session Opened, 
Application.Groupwise Session Opened, Application.HTTP Opened, Application.HTTPS Opened, 
Application.ICCP Session Opened, Application.Ident Session Opened, Application.IEC 104 Session Opened,
Application.IM Session Opened, Application.IPSec Session Started, Application.IRC Session Opened, 
Application.Kerberos Session Opened, Application.LDAP Session Started, Application.Lotus Notes Session Opened,
Application.LPD Session Opened, Application.Mail Opened, Application.MODBUS Session Opened,
Application.NCP Session Opened, Application.NetBIOS Session Opened, Application.NFS Session Opened,
Application.NNTP Session Opened, Application.NTP Session Opened, Application.P2P Opened, Application.RDP Opened,
Application.Remote .NET Session Opened, Application.RemoteAccess Opened, Application.REXEC Session Opened,
Application.RLOGIN Session Opened, Application.RPC Session Opened, Application.RSH Session Opened,
Application.RUSERS Session Opened, Application.SMB Session Opened, Application.SMTP Opened, 
Application.SNMP Session Opened, Application.SSH Opened, Application.SSL Session Opened,
Application.Streaming Media Session Opened, Application.Syslog Session Opened,
Application.Telnet Session Opened, Application.TFTP Session Opened, Application.TN3270 Session Opened,
Application.TOR Session Started, Application.Traceroute Session Opened, Application.VPN Opened, 
Application.Web Opened, Application.Whois Session Opened, Access.Firewall Session Opened,
Access.Database Action Allowed, Access.FTP Action Allowed, Access.Misc Application Action Allowed,
Access.Object Cached, Access.Session In Progress, Access.Session Inbound, Access.Session Outbound

