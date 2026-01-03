Detects when a single host on the internet sends a large number of packets (greater than 60000pps) to a single local destination at least 3 times over a small period of time. 
The packet rate in this rule can be adjusted as needed to reflect the network. 

Rule:

APPLY Remote Flood (TCP) on flows which are detected by the LOCAL system
AND when the flow bias is any of the following inbound 
AND when the IP protocol is one of the following TCP 
AND when at least 3 flows are seen with the same Source IP, Destination IP in 5 minutes
AND when the source packets is greater than 60000
