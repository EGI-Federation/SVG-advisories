---
title: Advisory-EGI-SVG-2025-15
permalink: /Advisory-EGI-SVG-2025-15
redirect_from:
  - /Advisory-SVG-CVE-2025-6020
  - /Advisory-SVG-CVE-2025-8941

---

published: false
---

## Advisory-EGI-SVG-2025-15

# HIGH risk pam_namespace vulnerabilities

Date:        2025-09-03 
Updated:     2025-10-08

HIGH risk vulnerabilities concerning pam_namespace which may
allow privilege escalation.

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-15
    
CVE ID     : CVE-2025-6020, CVE-2025-8941 

CVSS Score : 7.8 [R 1], [R 2]


## ACTIONS REQUIRED/RECOMMENDED

Sites using pam_namespace are recommended to urgently apply 
vendor updates using the references below as soon as patches 
are available for the distrubution they run.
    
Sites should be aware that if a public exploit is released 
which allows easy root access in the EGI infrastructure, 
these vulnerabilities are likely to be elevated to 'CRITICAL' 
risk and sites will then be required to patch or have 
mitigation in place within 7 days or risk suspension.


## MORE INFORMATION

Note that CVE-2025-8941 is due to a potentially RedHat-specific, 
incomplete fix for CVE-2025-6020.

    
## STATUS OF THIS ADVISORY
                            
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-15  

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-6020

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-8941

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

- [R 1] <https://access.redhat.com/security/cve/CVE-2025-6020>
    
- [R 2] <https://access.redhat.com/security/cve/CVE-2025-8941> 
    
- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2025-6020> 

- [R 4] <https://nvd.nist.gov/vuln/detail/CVE-2025-8941>
     
- [R 5] <https://www.cve.org/CVERecord?id=CVE-2025-6020>

- [R 6] <https://www.cve.org/CVERecord?id=CVE-2025-8941>

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2025-6020> 

- [R 8] <https://security-tracker.debian.org/tracker/CVE-2025-8941> 
    
- [R 9] <https://ubuntu.com/security/CVE-2025-6020>

- [R 10] <https://ubuntu.com/security/CVE-2025-8941>

- [R 11] <https://errata.build.resf.org/>   (RockyLinux)

- [R 12] <https://errata.almalinux.org/>  (AlmaLinux)
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Mischa Salle.
        
