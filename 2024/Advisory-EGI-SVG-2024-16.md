---
title: Advisory-EGI-SVG-2024-16
permalink: /Advisory-EGI-SVG-2024-16
redirect_from:
  - /Advisory-SVG-CVE-2024-5564 
  
published: false
---

## Advisory-EGI-SVG-2024-16

# HIGH risk vulnerability in libndp

Date:         2024-07-23
Updated:      2024-08-22

HIGH risk vulnerability concerning libndp.  This flaw allows a local 
malicious user to cause a buffer overflow in NetworkManager, triggered 
by sending a malformed IPv6 router advertisement packet. [R 1]


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-16
    
CVE ID     : CVE-2024-5564

CVSS Score : 8.1 [R 1]
     

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible 
using information in the references below.

Sites should be aware that if a public exploit is released which allows 
easy root access in the EGI infrastructure this vulnerability is likely 
to be elevated to 'Critical' and sites will then be required to patch 
within 7 days or risk suspension.

## MITIGATION

No mitigation has been identified for this vulnerability [R 1]

## MORE INFORMATION

Red Hat rates this as an Important severity, as a local attacker may gain 
enough information to jeopardize the environment's confidentiality, 
integrity and availability.
    
## STATUS OF THIS ADVISORY
                        
_TLP:WHITE information - Unlimited distribution_ 

 https://advisories.egi.eu/Advisory-EGI-SVG-2024-16 

 https://advisories.egi.eu/Advisory-SVG-5564 


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
----------------------------
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/security/cve/CVE-2024-5564>
      
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2024-5564> 
     
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2024-5564>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2024-5564> 
    
- [R 5] <https://ubuntu.com/security/CVE-2024-5564>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7]  <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Mischa Salle


