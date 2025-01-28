---
title: Advisory-EGI-SVG-2024-27
permalink: /Advisory-EGI-SVG-2024-27
redirect_from:
  - /Advisory-SVG-CVE-2024-49369

---

## Advisory-EGI-SVG-2024-27

# CRITICAL risk Icinga 2 Security releases

Date:        2024-11-19  
Updated:     2025-01-28


CRITICAL risk vulnerability in Icinga 2, security-fix releases available as of 2024-11-12
    

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2024-27
    
CVE ID     : CVE-2024-49369

CVSS Score : 9.8
    

## ACTIONS REQUIRED/RECOMMENDED

Sites running Icinga 2 should apply updates to affected versions immediately.

Fixed versions [R 2]:
- v2.14.3
- v2.13.10
- v2.12.11
- v2.11.12

Source code for new versions have been published on the Icinga Git repository [R 3]. 
Updated binary packages are available on packages.icinga.com and the Icinga for Windows 
repository. Updated container images are available on Docker Hub. 
Updated Helm Charts are provided in the corresponding repository.

While in this case we are not able to monitor sites for exposure to this vulnerability, 
and suspend vulnerable sites, we emphasise the importance of patching.   

## MORE INFORMATION

Icinga have published a blog detailing a vulnerability which allows an attacker to bypass 
TLS certificate validation for JSON-RPC and HTTP API connections. 
More information is available in the official blog post [R 2].

We (the EGI Software Vulnerability Group) are aware that there are (many) sites 
within EGI that are using Icinga 2.

    
## STATUS OF THIS ALERT/ADVISORY
                           
_TLP:CLEAR information - Unlimited distribution_
    
https://advisories.egi.eu/Advisory-EGI-SVG-2024-27 

https://advisories.egi.eu/Advisory-SVG-CVE-2024-49369

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG
  
-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://icinga.com/blog/2024/11/04/icinga2-security-pre-announcement/>

- [R 2] <https://icinga.com/blog/critical-icinga-2-security-releases-2-14-3/>

- [R 3] <https://github.com/Icinga/icinga2/releases>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

