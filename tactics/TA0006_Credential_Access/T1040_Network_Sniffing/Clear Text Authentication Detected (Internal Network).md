Detects flows to or from the Internet where the application type uses clear text passwords. 
This may include applications such as Telnet, FTP, etc.

RULE:

APPLY Local: Clear Text Application Usage on flows which are detected by the LOCAL system

AND when the flow context is Local to Local

AND when a flow matches any of the following BB:Policy Violation: Compliance Policy Violation: Clear Text Application Usage

AND when a flow matches all of the following BB:CategoryDefinition: Successful Communication



BB: Policy Violation: Compliance Policy Violation: Clear Text Application Usage

APPLY BB:Policy Violation: Compliance Policy Violation: Clear Text Application Usage on flows which are detected by the LOCAL system

AND when the flow matches Application is any of [RemoteAccess.Telnet or RemoteAccess.Telnet-Port or Mail.POP or Mail.POP-port or DataTransfer.FTP]

AND NOT when the flow bias is inbound, outbound


BB: BB:CategoryDefinition: Successful Communication

APPLY BB:CategoryDefinition: Successful Communication on flows which are detected by the LOCAL system

AND when the source byte/packet ratio is greater than than 80 bytes/packet

AND when the destination byte/packet ratio is greater than than 80 bytes/packet



