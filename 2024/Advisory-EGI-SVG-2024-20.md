---
title: Advisory-EGI-SVG-2024-20
permalink: /Advisory-EGI-SVG-2024-20

published: false
---

## Advisory-EGI-SVG-2024-20


# 'INFORMATION' SLUBStick Attack Scenario  [EGI-SVG-2024-20]

Date:        2024-09-10


A cross-cache attack Scenario called SLUBStick has been identified 
which may make it easier to exploit certain vulnerabilities including 
Linux Kernel Vulnerabilities [R 1]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-20
    
CVE ID     : N/A

CVSS Score : N/A
    

## ACTIONS REQUIRED/RECOMMENDED

No specific action is required at present.

However, as a result of this it is likely to be easier to exploit many
vulnerabilities, so sites are reminded to install updates (especially 
kernel ones) promptly after they become available. 

If anyone becomes aware of any situation where this attack scenario has
a significant impact on the EGI infrastructure then please inform EGI SVG.


## MORE INFORMATION

In [R 2] it states "SLUBStick is not a security vulnerability in itself, 
it is a technique that makes exploitation of other vulnerabilities easier.
Hence SLUBStick is not assigned a CVE number and mitigation happens 
through fixing other vulnerabilities that could be potentially exploited 
by this technique."

And see other references below.
    
## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_
                   
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-20

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES


- [R 1] <https://linuxsecurity.com/news/security-vulnerabilities/anatomy-of-slubstick-linux-vulnerability> 
     
- [R 2] <https://www.suse.com/support/kb/doc/?id=000021529>

- [R 3] <https://www.usenix.org/conference/usenixsecurity24/presentation/maar-slubstick>

- [R 4] <https://www-bleepingcomputer-com.cdn.ampproject.org/c/s/www.bleepingcomputer.com/news/security/linux-kernel-impacted-by-new-slubstick-cross-cache-attack/amp/> 
    
- [R 5] <https://thehackernews.com/2024/08/new-linux-kernel-exploit-technique.html>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this by Barbara Krasovec.
