---
title: Advisory-EGI-SVG-2026-05
permalink: /Advisory-EGI-SVG-2026-05
redirect_from:
  - /Advisory-SVG-CVE-2025-55182

---


## Advisory-EGI-SVG-2026-05

#  CRITICAL risk RUCIO vulnerability

Date:        2026-02-17
Updated:     2026-03-25

CRITICAL risk vulnerability concerning RUCIO WebUI container images 
due to the downstream dependencies on React and Next.js. 

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-05
    
CVE ID     : CVE-2025-55182

CVSS Score : 10 [R 1]
    
## AFFECTED SOFTWARE AND VERSIONS
    
Rucio containing WebUI 38.2.0 and 38.2.1  
This is fixed in version 38.3.0 and later.

## ACTIONS REQUIRED/RECOMMENDED
 
Sites running RUCIO services are required to urgently update
to Rucio WebUI 38.3.0 or higher [R 3]

All running resources MUST be either patched or have mitigation
in place or software removed by 2026-02-23  00:00 UTC 

Sites failing to act and/or failing to respond to requests from 
the EGI CSIRT team risk site suspension. 
   

## MORE INFORMATION

This critical vulnerability affecting Rucio WebUI 38.2.0 and 38.2.1
container images is due to the downstream dependencies on React and 
Next.js which are impacted by CVE-2025-55182, commonly referred to 
as "React2Shell" [R 4].

Sites running Rucio services may have already been informed of this.

    
## STATUS OF THIS ADVISORY    
                        
_TLP:CLEAR information - Unlimited distribution_ 
    
    https://advisories.egi.eu/Advisory-EGI-SVG-2026-05  

    https://advisories.egi.eu/Advisory-SVG-CVE-2025-55182

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

- [R 1]  <https://nvd.nist.gov/vuln/detail/CVE-2025-55182> 
         
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2025-55182>
    
- [R 3] <https://github.com/rucio/containers/releases/tag/webui-38.3.0>     

- [R 4] <https://react2shell.com/>  
    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Stefan Lueders 

