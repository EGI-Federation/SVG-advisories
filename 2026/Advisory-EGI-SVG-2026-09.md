---
title: Advisory-EGI-SVG-2026-09
permalink: /Advisory-EGI-SVG-2026-09

redirect_from:
  - /Advisory-SVG-CVE-2026-33634    
---
## Advisory-EGI-SVG-2026-09

# CRITICAL risk Trivy supply chain vulnerability

Date:        2026-03-31  
Updated:     

CRITICAL risk vulnerability concerning Trivy supply chain 

On March 19, 2026, a threat actor used compromised credentials
to publish a malicious Trivy v0.69.4 release [R 1]


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-09
    
CVE ID     : CVE-2026-33634

CVSS Score : 9.4 [R 2]
    
## AFFECTED SOFTWARE AND VERSIONS
    
The malicious version is Trivy v0.69.4 release.

While RedHat and derivatives do not support the product directly,
it can be run on those distributions. [R 3]

## ACTIONS REQUIRED/RECOMMENDED

Sites running Trivy should urgently check to ensure they are NOT running
a malicious version and take appropriate action if they are. 
 
If anyone becomes aware of any situation where this vulnerability has a
significant impact on the EGI infrastructure, then please inform EGI SVG.


## MORE INFORMATION

Trivy is a security scanner.

We (EGI SVG) are not aware how widespread the use of Trivy is in the 
EGI Infrastructure and the use of such tools is not required in EGI.
However, given the popularity of Trivy and the critical risk posed by
the malicious version, we decided an ALERT would be appropriate.
    
## STATUS OF THIS ADVISORY
                       
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2026-09  

 https://advisories.egi.eu/Advisory-SVG-CVE-2026-33634

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
------
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES
     
- [R 1] <https://www.cve.org/CVERecord?id=CVE-2026-33634>
    
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2026-33634> 

- [R 3] <https://access.redhat.com/security/cve/CVE-2026-33634>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Jakub Havrila 

