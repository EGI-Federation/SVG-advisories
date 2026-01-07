---
title: Advisory-EGI-SVG-2025-24
permalink: /Advisory-EGI-SVG-2025-24
redirect_from:
  - /Advisory-SVG-CVE-2025-65073
  
------

## Advisory-EGI-SVG-2025-24

# CRITICAL risk OpenStack Vulnerability

Date:        2025-11-25
Updated:     2026-01-07

CRITICAL risk vulnerability concerning OpenStack where Unauthenticated 
access to EC2/S3 token endpoints can grant Keystone authorization [R 1]

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-24
    
CVE ID     : CVE-2025-65073

CVSS Score : 7.5 [R 2]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites running OpenStack to provide EGI Federated Cloud services are 
required to urgently update to a new version using the reference [R 1] 
or via their usual means.

All running resources MUST be either patched or have mitigation
in place or software removed by 2025-11-28  00:00 UTC 

Sites failing to act and/or respond to requests from the EGI CSIRT team 
risk site suspension. 

## MORE INFORMATION

Note that this is only being sent to the EGI Federated Cloud sites.
    
## STATUS OF THIS ADVISORY
                   
_TLP:CLEAR information - Unlimited distribution_ 
    
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-24 

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-65073

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

- [R 1] <https://security.openstack.org/ossa/OSSA-2025-002.html>
     
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2025-65073>

- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2025-65073>
 
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Sebastian Luna-Valero
    
