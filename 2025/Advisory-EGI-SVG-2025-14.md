---
title: Advisory-EGI-SVG-2025-14
permalink: /Advisory-EGI-SVG-2025-14

redirect_from:
  - /Advisory-SVG-CVE-2025-38052
  
---

## Advisory-EGI-SVG-2025-14

# HIGH risk linux kernel vulnerability

Date:        2025-08-20 
Updated:     2025-09-24


A HIGH risk 'Use after free' vulnerability in the linux kernel's 
management of network namespaces has been found which may allow 
leakage of sensitive data. 

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-14
    
CVE ID     : CVE-2025-38052

CVSS Score : 7.8 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible 
using references below.


## MORE INFORMATION

Red Hat has fixed various vulnerabilities in the Linux kernel [R 2] [R 3]
including 1 which the EGI SVG considers to be 'HIGH' risk in the
EGI environment.

In general, it is recommended that sites disable network namespaces as
in [R 8] unless they are explicitly needed.

This vulnerability is also relevant for cloud/kubernetes sites, where 
network namespaces are actually used and cannot be disabled.
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-14 

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-38052

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
--

    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES


- [R 1] <https://access.redhat.com/security/cve/CVE-2025-38052>

- [R 2] <https://access.redhat.com/errata/RHSA-2025:12752>

- [R 3] <https://access.redhat.com/errata/RHSA-2025:12746>
    
- [R 4] <https://ubuntu.com/security/CVE-2025-38052>

- [R 5] <https://security-tracker.debian.org/tracker/CVE-2025-38052>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 8] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Mischa Salle

