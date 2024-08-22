---
title: Advisory-EGI-SVG-2024-14
permalink: /Advisory-EGI-SVG-2024-14
redirect_from:
  - /Advisory-SVG-CVE-2024-6409
  
published: false
---

## Advisory-EGI-SVG-2024-14

# 'HIGH' Risk *ANOTHER* OpenSSH vulnerability

Date:        2024-07-11 
Updated:     2024-08-22

*ANOTHER* OpenSSH vulnerability 
    
HIGH risk OpenSSH vulnerability due to a signal handler race condition 
with the possibility of Remote Code Execution. 
This affects RedHat 9 and derivatives.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-14
    
CVE ID     : CVE-2024-6409

CVSS Score : 7.0 [R 1]
    
## ACTIONS REQUIRED/RECOMMENDED

Sites running vulnerable versions are recommended to update relevant 
components as soon as possible using information in the references below.

## MORE INFORMATION

We are aware that this advisory is being sent only a couple of days after
another advisory on OpenSSH (CVE-2024-6387), but it is another vulnerablity which we
were not aware of when sending the previous advisory. Sites should be aware that they may require further action beyond those taken to resolve the previous vulnerability.

Some software providers rate as 'Moderate' others as 'High' risk or 'Important'.
EGI SVG has assessed this as 'HIGH risk in our environment. 

At the time of writing, as far as we are aware no exploit has been 
published but this could change.
    
## STATUS OF THIS ADVISORY
                       
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-14 

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-6409



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
    
- [R 1] <https://access.redhat.com/security/cve/CVE-2024-6409>
    
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2024-6409>

- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2024-6409> 

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2024-6409> 
    
- [R 5] <https://ubuntu.com/security/CVE-2024-6409>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7]  <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

EGI SVG was alerted to this vulnerability by both Sebastian Luna Valero and Jan Astalos.
