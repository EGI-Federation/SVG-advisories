---
title: Advisory-EGI-SVG-2025-06
permalink: /Advisory-EGI-SVG-2025-06
redirect_from:
  - /Advisory-SVG-CVE-2025-31492
  
published: false
---

## Advisory-EGI-SVG-2025-06

# HIGH risk mod_auth_openidc information leak vulnerability

Date:        2025-04-24 
Updated:     2025-05-28

mod_auth_openidc information leak vulnerability

HIGH risk vulnerability in mod_auth_openidc where information may be leaked 
in mod_auth_openidc, an OpenID Certified authentication and authorization
module for the Apache 2.x HTTP server that implements the OpenID Connect 
Relying Party functionality.  [R 1], [R 2]


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-06
    
CVE ID     : CVE-2025-31492

CVSS Score : 8.2 [R 1] / 7.5 [R 3]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible,
using information in references below.

## MORE INFORMATION

This component is used in various places in EGI, including the EGI Fed 
Cloud authentication.

Keystone (OpenStack identity service) uses it.

There is also the possibility that the risk may be elevated to 'Critical' 
given a public exploit and unauthenticated access and sites will then be 
required to patch or have mitigation in place within 7 days or risk 
suspension.

Some possibilities for mitigation are given in references below.

Also see references below for more information.
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 

 https://advisories.egi.eu/Advisory-EGI-SVG-2025-06  

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-31492 


Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

   
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2025-31492> 
     
- [R 2] <https://lists.debian.org/debian-lts-announce/2025/04/msg00025.html>

- [R 3] <https://access.redhat.com/security/cve/CVE-2025-31492>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2025-31492> 
    
- [R 5] <https://ubuntu.com/security/CVE-2025-31492>
    
- [R 6]<https://github.com/OpenIDC/mod_auth_openidc/security/advisories/GHSA-59jp-rwph-878r> 
    
- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Enol Fernández
