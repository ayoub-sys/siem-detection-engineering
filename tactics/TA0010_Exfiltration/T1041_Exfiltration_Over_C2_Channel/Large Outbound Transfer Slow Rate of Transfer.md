Detects a single host that is sending more data out of the network than received.  This rule detects over 2 MB of data transferred over a 2 hour period.  This is fairly slow and could indicated stealthy data leakage.

RUle:

APPLY Large Outbound Transfer Slow Rate of Transfer on flows which are detected by the LOCAL system

AND when the source bytes is greater than 20000

AND when at least 100 flows are seen with the same Source IP, Destination Port, Destination IP in 120 minutes

AND when the flow context is Local to Remote

AND when the flow bias is any of the following mostly outbound
