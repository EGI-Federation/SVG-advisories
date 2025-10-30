---
title: Advisory-EGI-SVG-2025-16
permalink: /Advisory-EGI-SVG-2025-16
redirect_from:
  - /Advisory-SVG-CVE-2025-38352
  
---
## Advisory-EGI-SVG-2025-16

# CRITICAL risk Linux Kernel Vulnerability 

Date:        2025-09-11
Updated:     2025-09-18, 2025-10-30

CRITICAL risk vulnerability concerning Linux kernel allowing 
local privilege escalation for which there is a known exploit.

**UPDATE** Patches are now available for Rocky Linux and AlmaLinux.

Revising date by which sites must patch to 7 days from now.


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-16
    
CVE ID     : CVE-2025-38352

CVSS Score : 7.8 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are required to urgently apply vendor kernel updates.

All running resources MUST be either patched or have mitigation
in place or software removed by 2025-09-26  00:00 UTC

Sites failing to act and/or failing to respond to requests from 
the EGI CSIRT team risk site suspension. 


## MORE INFORMATION

Although RedHat set this as 'Important' we have assessed as 'CRITICAL'
as it allows local privilege escalation AND an exploit is known to be
available [R 9], which we consider 'CRITICAL' in our environment.

The RedHat patches [R 2] [R 11] also fixes other vulnerabilities which 
we consider less than critical.
    
## STATUS OF THIS ADVISORY
                         
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-16  
 
 https://advisories.egi.eu/Advisory-SVG-CVE-2025-38352
 
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

- [R 1] <https://access.redhat.com/security/cve/CVE-2025-38352>
    
- [R 2] <https://access.redhat.com/errata/RHSA-2025:15471>   
     
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2025-38352>

- [R 4] <https://nvd.nist.gov/vuln/detail/CVE-2025-38352> 

- [R 5] <https://security-tracker.debian.org/tracker/CVE-2025-38352> 
    
- [R 6] <https://ubuntu.com/security/CVE-2025-38352>

- [R 7] <https://errata.build.resf.org/>   (RockyLinux)

- [R 8] <https://errata.almalinux.org/>  (AlmaLinux)
    
- [R 9] <https://www.cisa.gov/news-events/alerts/2025/09/04/cisa-adds-three-known-exploited-vulnerabilities-catalog>
    
- [R 10] <https://source.android.com/docs/security/bulletin/2025-09-01>    

- [R 11] <https://access.redhat.com/errata/RHSA-2025:15661>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS


SVG was alerted to this vulnerability by Mischa Salle 
