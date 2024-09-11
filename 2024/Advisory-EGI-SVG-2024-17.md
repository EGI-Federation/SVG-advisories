---
title: Advisory-EGI-SVG-2024-17
permalink: /Advisory-EGI-SVG-2024-17
redirect_from:
  - /Advisory-SVG-CVE-2024-41110
  
published: false
---

## Advisory-EGI-SVG-2024-17

# Docker Authorization Vulnerability 

Date:        2024-07-29 
Updated:     2024-09-11

CRITICAL risk vulnerability concerning Docker that could allow an attacker
to bypass authorization plugins (AuthZ) under specific circumstances.
[R 1], [R 2]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-17
    
CVE ID     : CVE-2024-41110

CVSS Score : 10 [R 3]   

## ACTIONS REQUIRED/RECOMMENDED

Sites running Docker should check  whether they are running a 
vulnerable version, and if they are update urgently, see [R 1]

If anyone becomes aware of any situation or configuration where this
vulnerability can be exploited in the EGI infrastructure or otherwise has a
significant impact on the EGI infrastructure then please inform  EGI SVG.

## MORE INFORMATION

More information is available at [R 1] and [R 2]

In [R 2] it is stated that Users of Docker Engine who rely on 
authorization plugins to make access control decisions are vulnerable.

At present it is not clear whether this is exploitable in any
of the configurations used in the EGI infrastructure, but since the
CVSS score is 10 we are treating it as 'Critical'
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 

 https://advisories.egi.eu/Advisory-EGI-SVG-2024-17  

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-41110 

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

- [R 1] <https://thehackernews.com/2024/07/critical-docker-engine-flaw-allows.html>

- [R 2] <https://www.docker.com/blog/docker-security-advisory-docker-engine-authz-plugin/>
    
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2024-41110>
    
- [R 4] <https://nvd.nist.gov/vuln/detail/CVE-2024-41110> 
  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by David Crooks and Thomas Birkett

