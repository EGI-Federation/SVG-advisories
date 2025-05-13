---
title: Advisory-EGI-SVG-2025-05
permalink: /Advisory-EGI-SVG-2025-05
redirect_from:
  - /Advisory-SVG-CVE-2025-30093

---

## Advisory-EGI-SVG-2025-05

# HT Condor Security Release

Date:        2025-04-02
Updated:     2025-05-13
      
A security vulnerability was found in the HTCondor Software Suite (HTCSS)
where a user who has an IDToken with restricted authorization could perform 
some operations that should be denied by those restrictions. [R 1]
A security release has been made which fixes this. 
    
## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-05
    
CVE ID     : CVE-2025-30093

CVSS Score : Not Available at time of writing
    
HT-Condor ID : 2025-0001

## AFFECTED SOFTWARE AND VERSIONS

The vulnerability is fixed in HTCondor Security Release: 23.0.22,  
23.10.22, 24.0.6, and 24.6.0.
Earlier versions are likely to be vulnerable.
    
## ACTIONS REQUIRED/RECOMMENDED

Sites running HTCondor are recommended to update relevant components 
as soon as possible using information in [R 1].

Alternatively, mitigation is available, also documented in [R 1].


## MORE INFORMATION

See [R 1]  

   
## STATUS OF THIS ADVISORY
                       
_TLP:CLEAR information - Unlimited distribution_ 
    
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-05  
    
 https://advisories.egi.eu/Advisory-SVG-CVE-2025-30093  

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG
  
-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
----
  
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES


- [R 1] <https://htcondor.org/security/vulnerabilities/HTCONDOR-2025-0001>
    
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2025-30093>
    
- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2025-30093>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by the HTCondor team

