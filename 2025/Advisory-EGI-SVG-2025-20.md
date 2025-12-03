---
title: Advisory-EGI-SVG-2025-20
permalink: /Advisory-EGI-SVG-2025-20
redirect_from:
  - /Advisory-CVE-2025-7493
  
---
## Advisory-EGI-SVG-2025-20

# CRITICAL risk FreeIPA host to domain privilege escalation

Date:        2025-10-01
Updated:     2025-12-03


CRITICAL risk vulnerability concerning FreeIPA which allows host to domain
privilege escalation [R 1]


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-20
    
CVE ID     : CVE-2025-7493

CVSS Score : 9.1 [R 1]


## ACTIONS REQUIRED/RECOMMENDED

Sites running FreeIPA must patch urgently when patches are
available for the distribution they run.
    
We (EGI SVG) are aware of 1 site in the EGI infrastructure which
is using FreeIPA but do not know how widespread the usage is.
    
If anyone becomes aware of any situation where this vulnerability has a
significant impact on the EGI infrastructure, then please inform EGI SVG.


## MITIGATION

No mitigation is available, other than updating the software [R 3]


## MORE INFORMATION

Details of this vulnerability are at [R 8]    
    
    
## STATUS OF THIS ADVISORY
                           
_TLP:CLEAR information - Unlimited distribution_ 

    https://advisories.egi.eu/Advisory-EGI-SVG-2025-20
  
    https://advisories.egi.eu/Advisory-SVG-CVE-2025-7493

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


- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2025-7493> 
     
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2025-7493>

- [R 3] <https://access.redhat.com/security/cve/CVE-2025-7493>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2025-7493> 
    
- [R 5] <https://ubuntu.com/security/CVE-2025-7493>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
    
- [R 8] <https://www.freeipa.org/release-notes/4-12-5.html> 


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovek
    
