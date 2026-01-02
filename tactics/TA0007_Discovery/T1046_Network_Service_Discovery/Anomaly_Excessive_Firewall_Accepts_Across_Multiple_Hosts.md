1- Reports excessive Firewall Accepts across multiple hosts.  
More than 100 events were detected across at least 100 unique destination IP addresses in 5 minutes. 

2- Rule:

APPLY Anomaly: Excessive Firewall Accepts Across Multiple Hosts on events which are detected by the LOCAL system

AND NOT when an event matches any of the following BB:HostDefinition: Servers (Excludes known servers)

AND when any of these BB:CategoryDefinition: Firewall or ACL Accept, BB:DeviceDefinition: FW / Router / Switch with the same source IP more than 100 times, across more than 100 destination IP within 5 minutes

* BB:CategoryDefinition: Firewall or ACL Accept

APPLY BB:CategoryDefinition: Firewall or ACL Accept on events which are detected by the LOCAL system

AND when the event category for the event is one of the following Access.Firewall Permit,
Access.ACL Permit, Access.Access Permitted, Access.Session Opened, Application.AAA Session Started,
Application.Auth Opened, Application.Chargen Session Started, Application.Chat Opened,
Application.CUPS Session Opened, Application.CVS Session Opened, Application.DAP Session Started,
Application.Database Opened, Application.DHCP Session Opened, Application.Discard Session Opened,
Application.DNP3 Session Opened, Application.DNS Opened, Application.Echo Session Opened,
Application.FileTransfer Opened, Application.Finger Session Opened, Application.FTP Opened,
Application.GIOP Session Opened, Application.Gopher Session Opened, Application.Groupwise Session Opened,
Application.HTTP Opened, Application.HTTPS Opened, Application.ICCP Session Opened,
Application.Ident Session Opened, Application.IEC 104 Session Opened, Application.IM Session Opened,
Application.IPSec Session Started, Application.IRC Session Opened, Application.Kerberos Session Opened,
Application.LDAP Session Started, Application.Lotus Notes Session Opened, Application.LPD Session Opened,
Application.Mail Opened, Application.MODBUS Session Opened, Application.NCP Session Opened,
Application.NetBIOS Session Opened, Application.NFS Session Opened, Application.NNTP Session Opened,
Application.NTP Session Opened, Application.P2P Opened, Application.RDP Opened,
Application.Remote .NET Session Opened, Application.RemoteAccess Opened,
Application.REXEC Session Opened, Application.RLOGIN Session Opened,
Application.RPC Session Opened, Application.RSH Session Opened, 
Application.RUSERS Session Opened, Application.SMB Session Opened, Application.SMTP Opened,
Application.SNMP Session Opened, Application.SSH Opened, Application.SSL Session Opened,
Application.Streaming Media Session Opened, Application.Syslog Session Opened, Application.Telnet Session Opened, 
Application.TFTP Session Opened, Application.TN3270 Session Opened, Application.TOR Session Started, 
Application.Traceroute Session Opened, Application.VPN Opened, Application.Web Opened, Application.Whois Session Opened,
Access.Firewall Session Opened, Access.Database Action Allowed, Access.FTP Action Allowed, 
Access.Misc Application Action Allowed, Access.Object Cached, Access.Session In Progress,
Access.Session Inbound, Access.Session Outbound


* BB:DeviceDefinition: FW / Router / Switch 

Apply BB:DeviceDefinition: FW / Router / Switch on events which are detected by the Local system
and when the event(s) were detected by one or more of Cisco Adaptive Security Appliance (ASA), 
Configurable Firewall Filter, Cisco PIX Firewall, Juniper Networks Firewall and VPN, 
Juniper Junos OS Platform, Juniper DX Application Acceleration Platform, 
Juniper M Series Multiservice Edge Routing, Juniper MX Series Ethernet Services Router, 
Juniper T Series Core Platform, Linux iptables Firewall, Extreme Matrix E1 Switch, 
Extreme Matrix K/N/S Series Switch, Fortinet FortiGate Security Gateway, Cisco IOS,
Forcepoint Sidewinder, Extreme Networks ExtremeWare Operating System (OS),
Cisco CatOS for Catalyst Switches, Cisco 12000 Series Routers, Cisco 6500 Series Switches, 
Cisco 7600 Series Routers, Symantec Gateway Security (SGS) Appliance, SonicWALL SonicOS,
Check Point, Nortel Multiprotocol Router, Cisco Firewall Services Module (FWSM), 
CyberGuard TSP Firewall/VPN, Cisco Carrier Routing System, Cisco Integrated Services Router,
TippingPoint X Series Appliances, F5 Networks BIG-IP LTM, 3Com 8800 Series Switch,
Starent Networks Home Agent (HA), Foundry Fastiron, Imperva SecureSphere, Motorola SymbolAP,
Extreme HiPath, IBM Resource Access Control Facility (RACF), Redback ASE, Juniper SRX Series Services Gateway,
Brocade FabricOS, Cisco Aironet, Cisco Nexus, DCN DCS/DCRS Series, Extreme 800-Series Switch, Extreme A2-Series,
Extreme A4-Series, Extreme B2-Series, Extreme B3-Series, Extreme B5-Series, Extreme C2-Series, Extreme C3-Series,
Extreme C5-Series, Extreme D2-Series, Extreme G3-Series, Extreme I3-Series, Extreme Stackable and Standalone Switches,
Extreme XSR Security Routers, ESET Remote Administrator, H3C Comware Platform, H3C IP Security Devices, H3C Routers,
H3C Switches, HP ProCurve, Huawei AR Series Router, Huawei S Series Switch, Juniper EX-Series Ethernet Switch,
Juniper Networks Network and Security Manager, Juniper Security Binary Log Collector, Microsoft ISA,
Nortel Ethernet Routing Switch 2500/4500/5500, Nortel Ethernet Routing Switch 8300/8600, Nortel Secure Router,
Nortel Switched Firewall 5100, Nortel Switched Firewall 6000, Palo Alto PA Series, Sophos Web Security Appliance,
Venustech Venusense Firewall, Venustech Venusense Security Platform, Venustech Venusense Unified Threat Management, 
WatchGuard Fireware OS, Sophos Astaro Security Gateway, Trend Micro Deep Discovery Inspector


