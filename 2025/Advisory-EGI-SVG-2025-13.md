---
title: Advisory-EGI-SVG-2025-13
permalink: /Advisory-EGI-SVG-2025-13
redirect_from:
  - /Advisory-SVG-CVE-2025-6000
 
---
## Advisory-EGI-SVG-2025-13

# Vulnerabilities concerning Hashicorp Vault and Openbao

Date:        2025-08-13
Updated:     2025-09-24

CRITICAL risk vulnerabilities concerning Hashicorp Vault and Openbao  [R 1]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2025-13
    
CVE ID     : CVE-2025-6000

CVSS Score : 9.1 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites using Hashicorp Vault or Openbao should urgently check the references
below, see whether their installation is vulnerable, and take appropriate 
action.

If anyone becomes aware of any situation where this vulnerability has a 
significant impact on the EGI infrastructure, then please inform EGI SVG.


## MORE INFORMATION

The EGI SVG is aware of 1 EGI service using the Hashicorp Vault, but in a
non-vulnerable configuration. We are currently not aware of any instances in
the EGI infrastructure using either Hashicorp Vault or Openbao in a vulnerable
manner.

This vulnerability is considered 'CRITICAL' if it is used in a way which
makes a site vulnerable. 
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unimited distribution_ 

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
---

 https://advisories.egi.eu/Advisory-EGI-SVG-2025-13 

  https://advisories.egi.eu/Advisory-SVG-CVE-2025-6000

Minor updates may be made without re-distribution to the sites.


Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2025-6000> 
     
- [R 2] <https://cyata.ai/blog/cracking-the-vault-how-we-found-zero-day-flaws-in-authentication-identity-and-authorization-in-hashicorp-vault/>

- [R 3] <https://github.com/openbao/openbao/releases/tag/v2.3.2>

- [R 4] <https://github.com/openbao/openbao/security/advisories>
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS


SVG was alerted to this vulnerability by Dave Dykstra 
