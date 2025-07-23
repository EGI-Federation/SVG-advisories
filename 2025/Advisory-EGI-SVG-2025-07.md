---
title: Advisory-EGI-SVG-2025-07
permalink: /Advisory-EGI-SVG-2025-07
redirect_from:
  - /Advisory-SVG-CVECVE-2025-21756
  
published: false
---

## Advisory-EGI-SVG-2025-07

# CRITICAL risk Linux Kernel Vulnerability

Date:        2025-05-28
Updated:     2025-07-23

RedHat has released Kernel updates to fix several kernel vulnerabilities, 
one of which (CVE-2025-21756) the EGI SVG considers 'CRITICAL'  for 
the EGI infrastructure. [R 1]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2025-07
    
CVE ID     : CVE-2025-21756

CVSS Score : 7.8 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

All affected sites are required to react urgently, using references below.
 
All running resources MUST be patched or mitigated by 2025-06-06  00:00 UTC 

Sites failing to act and/or respond to requests from the EGI CSIRT team 
risk site suspension. 


## MORE INFORMATION

For the EGI infrastructure, CVE-2025-21756 is considered 'CRITICAL'
even though the CVSS score fits more with 'HIGH' risk, as explained next.

Although it is only exploitable locally, that mitigation is insufficient
for Grid Worker Nodes and shared User Interfaces. In practice this means 
it may be widely exploitable in our infrastructure.

Furthermore, although the vulnerability is particularly associated with
the use of VMware, the corresponding driver is also usable with other
VM systems and has been found to be readily available even on hosts that 
do not have any VM usage set up. Please refer to the mitigation below.

A public exploit is available [R 6], [R 7]


## MITIGATION

Sufficient mitigation is to disable the affected driver, as detailed in [R 1].
## STATUS OF THIS ADVISORY
                            
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2025-07

https://advisories.egi.eu/Advisory-SVG-CVE-2025-21756

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

- [R 1] <https://access.redhat.com/security/cve/CVE-2025-21756>

- [R 2] <https://security-tracker.debian.org/tracker/CVE-2025-21756> 
    
- [R 3] <https://ubuntu.com/security/CVE-2025-21756>

- [R 4] <https://errata.build.resf.org/>   (RockyLinux)

- [R 5] <https://errata.almalinux.org/>  (AlmaLinux)
    
- [R 6] <https://github.com/hoefler02/CVE-2025-21756>
    
- [R 7] <https://hoefler.dev/articles/vsock.html> 


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>
