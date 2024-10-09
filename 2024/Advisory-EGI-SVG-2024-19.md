---
title: Advisory-EGI-SVG-2024-19
permalink: /Advisory-EGI-SVG-2024-19
redirect_from:
  - /Advisory-SVG-CVE-2024-36971
  
published: false
---

## Advisory-EGI-SVG-2024-19

# Flaw in Linux kernel's network route management.

Date:        2024-09-03
Updated: 

HIGH risk use-after-free vulnerability in the Linux kernel's network route
management. This flaw allows an attacker to alter the behaviour of certain 
network connections. [R 1]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-19
    
CVE ID     : CVE-2024-36971

CVSS Score : 7.8 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible 
using information in the references below.

On Android this vulnerability is said to be exploited in the wild.

Sites should be aware that if a public exploit is released which allows 
this vulnerability to be exploited in the EGI infrastructure, this 
vulnerability is likely to be elevated to 'Critical' and sites will 
then be required to patch or have mitigation in place within 7 days 
or risk suspension. 

## MITIGATION

There is no practical mitigation [R 1]

    
## STATUS OF THIS ADVISORY 
                     
_TLP:CLEAR information - Unlimited distribution_ 

 https://advisories.egi.eu/Advisory-EGI-SVG-2024-19 

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-36971 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.

    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/security/cve/CVE-2024-36971>

- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2024-36971> 
     
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2024-36971>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2024-36971> 
    
- [R 5] <https://ubuntu.com/security/CVE-2024-36971>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS 

SVG was alerted to this vulnerability by Mischa Salle 

