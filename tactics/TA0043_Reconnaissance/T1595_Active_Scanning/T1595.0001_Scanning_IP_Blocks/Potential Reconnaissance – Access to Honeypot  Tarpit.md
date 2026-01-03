Potential Reconnaissance – Access to Honeypot / Tarpit

This rule triggers when an event involves a source or destination defined as a honeypot or tarpit address. 

Rule: Potential Honeypot Access 

APPLY Potential Honeypot Access on events which are detected by the LOCAL system
AND when an event matches any of the following BB:NetworkDefinition: Honeypot like Addresses

BB: NetworkDefinition: Honeypot like Addresses

Apply BB:NetworkDefinition: Honeypot like Addresseson events or flows which are detected by the Local system
 and when the destination IP is a part of any of the following Bogon


