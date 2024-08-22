---
title: Advisory-EGI-SVG-2024-13
permalink: /Advisory-EGI-SVG-2024-13
redirect_from:
  - /Advisory-SVG-CVE-2024-6387
  
---

## Advisory-EGI-SVG-2024-13

# HIGH risk OpenSSH vulnerability

Date:        2024-07-11
Updated:     2024-08-22

HIGH risk vulnerability in OpenSSH with the possibility of Unauthenticated
Remote Code Execution due to a race condition in signal handling [R 1]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-13
    
CVE ID     : CVE-2024-6387

CVSS Score : 8.1 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components or apply mitigation 
as soon as possible using information in the references below.


## MORE INFORMATION

For RedHat and derivatives, this only affects RHEL9 and derivatives [R 1]

At present, as far as we know, a working exploit has only been produced 
for 32-bit systems, therefore the impact on EGI is likely to be limited.
For this reason we have not elevated to 'Critical' risk but this could 
change. This does, of course, mean anyone running 32-bit systems should
take action urgently, while it is recommended that 64-bit systems also
be patched soon, because a 64-bit exploit may appear at some point.
       
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 
       
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-13 

 https://advisories.egi.eu/Advisory-SVG-2024-6387

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

- [R 1] <https://access.redhat.com/security/cve/CVE-2024-6387>

- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2024-6387> 

- [R 3] <http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2024-6387>
     
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2024-6387> 
    
- [R 5] <https://ubuntu.com/security/CVE-2024-6387>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by the EGI CSIRT team.


