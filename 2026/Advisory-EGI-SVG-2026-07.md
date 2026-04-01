---
title: Advisory-EGI-SVG-2026-07
permalink: /Advisory-EGI-SVG-2026-07

redirect_from:
  - /Advisory-SVG-CVE-2026-24708
---


## Advisory-EGI-SVG-2026-07

# HIGH risk OpenStack Nova vulnerability

HIGH risk vulnerability concerning OpenStack Nova image conversion which 
is likely to affect cloud sites [R 1]

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-07
    
CVE ID     : CVE-2026-24708

CVSS Score : 8.2 [R 2]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites running Openstack Nova are recommended to update relevant components 
as soon as possible when fixes are available for the software they deploy
using information in the references below.


## MORE INFORMATION

Although this advisory is primarily for EGI Federated Cloud sites, 
we are sending to all EGI sites as a precaution. 

It is unclear how easy this is to exploit beyond DoS, but since it has
been assessed as a CVSS score of 8.2 and there are the possibilities of
widespread damage and privilege escalation, we have assessed as 'HIGH' risk.
We do not think we have sufficient reason to reduce the risk below what
others have assessed as our equivalent to HIGH. 

## STATUS OF THIS ADVISORY
                            
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2026-07 

 https://advisories.egi.eu/Advisory-SVG-CVE-2026-24708

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
---
   
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES
    
- [R 1] <https://security.openstack.org/ossa/OSSA-2026-002.html>   

- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2026-24708> 
     
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2026-24708>

- [R 4] <https://access.redhat.com/security/cve/CVE-2026-24708>

- [R 5] <https://security-tracker.debian.org/tracker/CVE-2026-24708> 
    
- [R 6] <https://ubuntu.com/security/CVE-2026-24708>

- [R 7] <https://errata.build.resf.org/>   (RockyLinux)

- [R 8] <https://errata.almalinux.org/>  (AlmaLinux)
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Enol Fernández
