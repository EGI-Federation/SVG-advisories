---
title: Advisory-EGI-SVG-2025-26
permalink: /Advisory-EGI-SVG-2025-26
redirect_from:
  - /Advisory-SVG-CVE-2025-55182  
---

## Advisory-EGI-SVG-2025-26

# CRITICAL risk React Server Components Vulnerability 

Date:        2025-12-10  
Updated:     2026-01-13

CRITICAL risk vulnerability concerning React Server Components 
allowing unauthenticated remote code execution.  

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-26
    
CVE ID     : CVE-2025-55182

CVSS Score : 10.0 [R 1]
    
## AFFECTED SOFTWARE AND VERSIONS
    
See [R 2]
    
## ACTIONS REQUIRED/RECOMMENDED

Sites running web services depending on React Server Components  
should check [R 2] and have any vulnerable version updated urgently. 
 
If anyone becomes aware of any situation where this vulnerability is 
exposed in the EGI infrastructure, then please inform EGI SVG. 
    

## MORE INFORMATION

An unauthenticated remote attacker could:

- Execute arbitrary code on the server

- Access or manipulate data processed by server-side React functions  

- Compromise the hosting environment 

- Potentially pivot deeper into infrastructure
 
Because this vulnerability requires no authentication and may be  
reachable through public endpoints, it is considered Critical.

The EGI SVG is currently not aware of potentially affected services  
providing functionality to the EGI ecosystem.

If EGI SVG becomes aware of any relevant exposure, we will send an  
update to this alert and require affected sites to patch within 7 days.
    
    
## STATUS OF THIS ADVISORY   
                        
_TLP:CLEAR information - Unimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2025-26 

https://advisories.egi.eu/Advisory-SVG-CVE-2025-55182 
                        
Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
---
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

 
- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2025-55182> 
     
- [R 2] <https://react.dev/blog/2025/12/03/critical-security-vulnerability-in-react-server-components>

    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by OSG
