QNI : Confidential Content Being Transferred to Foreign Geography

Notes
This rule detects confidential content that is being transferred to countries/regions with restricted access.

Note that these countries/regions are defined in the Building Block: "Countries/Regions with Restricted Access" therefore please ensure this is setup according to your business use case before you enable this rule.

RULE:

APPLY QNI : Confidential Content Being Transferred to Foreign Geography on flows which are detected by the LOCAL system

AND when the flow context is Local to Remote

AND when a flow matches any of the following BB:CategoryDefinition: Countries/Regions with Restricted Access

AND when any of Suspect Content Descriptions (QNI) match confidential content


BB:CategoryDefinition: Countries/Regions with Restricted Access

Apply BB:CategoryDefinition: Countries/Regions with Restricted Access on events or flows which are detected by the Local system
and when the any IP is a part of any of the following Africa, Antarctic, Asia, CentralAmerica, Europe, Oceania, SouthAmerica, misc
