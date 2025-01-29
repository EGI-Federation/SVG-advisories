---
title: Advisory-EGI-SVG-2024-28
permalink: /Advisory-EGI-SVG-2024-28
redirect_from:
  - /Advisory-SVG-CVE-2024-10963
  
published: false
---

## Advisory-EGI-SVG-2024-28

# HIGH risk PAM host name spoofing vulnerability

Date:        2024-12-12 
Updated: 

PAM host name spoofing vulnerability

HIGH risk vulnerability concerning PAM. A flaw was found in pam_access, 
where certain rules in its configuration file are mistakenly treated as hostnames. 
This vulnerability allows attackers to trick the system by pretending to be a trusted 
hostname, gaining unauthorized access. [R 3]


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-28
    
CVE ID     : CVE-2024-10963

CVSS Score : 7.4 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible 
using information in the references below.
    

## MITIGATION

RedHat suggests some Mitigation in [R 3]

## MORE INFORMATION

The EGI SVG is unsure how widely this can be exploited in EGI, but we think it may be exploitable in some configurations. We have assessed as 'HIGH' due to the serious impact if it is exploitable.
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unimited distribution_ 

 https://advisories.egi.eu/Advisory-EGI-SVG-2024-28 

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-10963


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

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2024-10963> 
     
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2024-10963>

- [R 3] <https://access.redhat.com/security/cve/CVE-2024-10963>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2024-10963> 
    
- [R 5] <https://ubuntu.com/security/CVE-2024-10963>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Mischa Salle 
