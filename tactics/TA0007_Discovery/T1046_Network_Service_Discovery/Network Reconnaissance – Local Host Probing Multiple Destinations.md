Reports when various suspicious or reconnaissance events have been detected from the same local source IP address to more than 5 destination IP address in 4 minutes. This can indicate various forms of host probing, 
such as Nmap reconnaissance,
which attempts to identify the services and operation systems of the target. 


* Rule:

APPLY Local L2L Suspicious Probe Events Detected on events or flows which are detected by the LOCAL system

AND NOT when an event matches any of the following BB:HostDefinition: Servers

AND when the event context is Local to Local, Local to Remote

AND when any of these BB:CategoryDefinition: Recon Events, BB:CategoryDefinition: Suspicious Events with the same source IP more than 20 times, across more than 5 destination IP within 4 minutes


* BB:HostDefinition: Servers

APPLY BB:HostDefinition: Servers on events or flows which are detected by the LOCAL system

AND when a flow or an event matches any of the following BB:HostDefinition: Database Servers, 
BB:HostDefinition: DHCP Servers, BB:HostDefinition: DNS Servers, BB:HostDefinition: FTP Servers,
BB:HostDefinition: LDAP Servers, BB:HostDefinition: Mail Servers, BB:HostDefinition: Network Management Servers, 
BB:HostDefinition: Proxy Servers, BB:HostDefinition: RPC Servers, BB:HostDefinition: SNMP Sender or Receiver, 
BB:HostDefinition: SSH Servers, BB:HostDefinition: Virus Definition and Other Update Servers, 
BB:HostDefinition: Web Servers, BB:HostDefinition: Windows Servers, BB:HostReference: Database Servers, 
BB:HostReference: DHCP Servers, BB:HostReference: DNS Servers, BB:HostReference: FTP Servers,
BB:HostReference: LDAP Servers, BB:HostReference: Mail Servers, BB:HostReference: Proxy Servers, 
BB:HostReference: SSH Servers, BB:HostReference: Web Servers, BB:HostReference: Windows Servers


* BB:CategoryDefinition: Recon Events

APPLY BB:CategoryDefinition: Recon Events on events or flows which are detected by the LOCAL system

AND when a flow or an event matches any of the following 
BB:CategoryDefinition: Recon Event Categories, BB:CategoryDefinition: Recon Flows


* BB:CategoryDefinition: Suspicious Events

APPLY BB:CategoryDefinition: Suspicious Events on events or flows which are detected by the LOCAL system

AND when a flow or an event matches any of the following BB:CategoryDefinition: Suspicious Flows, 
BB:CategoryDefinition: Suspicious Event Categories

 
