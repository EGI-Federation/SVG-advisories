---
title: Advisory-EGI-SVG-2025-25
permalink: /Advisory-EGI-SVG-2025-25

---
## Advisory-EGI-SVG-2025-25

# HTCondor Vulnerability

Date:        2025-12-03  
Updated:     2026-01-13
      
A security vulnerability was found in the HTCondor Software Suite (HTCSS)
where an authorized user can submit a specially-crafted job that will run 
as any other non-root user after the Access Point (AP) is upgraded to a 
vulnerable version. [R 1]
    
## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-25
    
CVE ID     : Not available at time of writing

CVSS Score : Not Available at time of writing
    
HT-Condor ID : 2025-0002

## AFFECTED SOFTWARE AND VERSIONS

The vulnerability is fixed as of these HTCondor versions: 
24.12.14, 25.0.3, 25.3.1.
    
## ACTIONS REQUIRED/RECOMMENDED

Sites running HTCondor are recommended to update relevant components 
using information in [R 1].


## MORE INFORMATION

See [R 1]  

   
## STATUS OF THIS ADVISORY
                       
_TLP:CLEAR information - Unlimited distribution_ 
    
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-05  
    
Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG
  
-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
--
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES


- [R 1] <https://htcondor.org/security/vulnerabilities/HTCONDOR-2025-0002>
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by the HTCondor team
