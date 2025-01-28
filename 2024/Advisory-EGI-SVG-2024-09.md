---
title: Advisory-EGI-SVG-2024-09
permalink: /Advisory-EGI-SVG-2024-09
redirect_from:
  - /Advisory-SVG-CVE-2024-2201
  
published: false
---

## Advisory-EGI-SVG-2024-09

# HIGH risk Intel Native Branch History Vulnerability

Date:        2024-04-17 
Updated:     2024-12-10

A flaw was found in some Intel CPUs where mitigations for the Spectre 
V2/BHI vulnerability were incomplete. This issue may allow an attacker 
to read arbitrary memory, compromising system integrity and exposing 
sensitive information.  [R 1] [R 2]


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-09
    
CVE ID     : CVE-2024-2201

CVSS Score : 4.7 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites running Intel hardware are recommended to look at the announced 
information and take appropriate action.

**Updated 2024-12-10**

After checking this older issue it was found that patches are available
which address this vulnerability for RH8 and RH9 in August 2024 and 
October 2024 respectively.  [R 1]

See references below for further information.

## MORE INFORMATION

Given the way the Grid/HTC computing works within EGI, the EGI SVG
considers the risk from this vulnerability higher than the CVSS score. 

    
## STATUS OF THIS ADVISORY
    
_TLP:CLEAR information - Unlimited distribution_ 
                   
  https://advisories.egi.eu/Advisory-EGI-SVG-2024-09

  https://advisories.egi.eu/Advisory-SVG-CVE-2024-2201 


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

- [R 1] <https://access.redhat.com/security/cve/CVE-2024-2201>

- [R 2] <https://www.openwall.com/lists/oss-security/2024/04/09/15>

- [R 3] <https://www.intel.com/content/www/us/en/developer/topic-technology/software-security-guidance/overview.html>

- [R 4] <https://www.intel.com/content/www/us/en/developer/articles/technical/software-security-guidance/advisory-guidance/branch-history-injection.html>

- [R 5] <https://kb.cert.org/vuls/id/155143>

- [R 6] <https://security-tracker.debian.org/tracker/CVE-2024-2201> 
    
- [R 7] <https://ubuntu.com/security/CVE-2024-2201>

- [R 8] <https://errata.build.resf.org/>   (RockyLinux)

- [R 9] <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Eygene Ryabinkin
