---
title: Advisory-EGI-SVG-2026-02
permalink: /Advisory-EGI-SVG-2026-02
redirect_from:
  - /Advisory-SVG-CVE-2025-68285

---
## Advisory-EGI-SVG-2026-02

# HIGH risk Ceph client Vulnerability in Linux kernel 

Date:        2026-01-21 
Updated:     2026-02-25

A HIGH risk use-after-free vulnerability was found in the Ceph client 
session initialization in the Linux kernel. This may lead to privilege
escalation.  


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-02
    
CVE ID     : CVE-2025-68285

CVSS Score : 7.0 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible 
using information in the references below.    

Sites should be aware that if a public exploit is released which allows 
easy root access in the EGI infrastructure this vulnerability is likely 
to be elevated to 'Critical' and sites will then be required to patch or 
have mitigation in place within 7 days or risk suspension. 


## MORE INFORMATION

This vulnerability is difficult to expoit because of the complexity  
of the attack.  However, the use-after-free vulnerability might lead to 
privilege escalation, which elevates the risk. RedHat's initial 
assessment of 'IMPORTANT' severity, usually implies at least HIGH risk 
for EGI sites, although it appears to have been downgraded to 'Moderate'
    
## STATUS OF THIS ADVISORY
                            
_TLP:CLEAR information - Unlimited distribution_  
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2026-02  

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-68285

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

- [R 1] <https://access.redhat.com/security/cve/CVE-2025-68285> 
     
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2025-68285>

- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2025-68285>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2025-68285> 
    
- [R 5] <https://ubuntu.com/security/CVE-2025-68285>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
     

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Mischa Salle 

    
