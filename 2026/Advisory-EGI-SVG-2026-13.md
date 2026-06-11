---
title: Advisory-EGI-SVG-2026-13
permalink: /Advisory-EGI-SVG-2026-13

redirect_from:
  - /Advisory-SVG-CVE-2026-29080
  - /Advisory-SVG-CVE-2026-29090
---

## Advisory-EGI-SVG-2026-13

## CRITICAL risk Rucio vulnerabilities

Date:        2026-05-07 
Updated:     

CRITICAL risk SQL injection vulnerabilities in Rucio, 
which affect metadata configurations.

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-13
    
CVE ID     : CVE-2026-29080, CVE-2026-29090 

CVSS Score : 9.4/9.0 [R 3] [R 4]
    
## AFFECTED SOFTWARE AND VERSIONS
    
These vulnerabilities affect:
- All Oracle-based Rucio deployments using the default metadata plugin
  configuration (json_meta), since Rucio server version 1.27.0
  (GHSA-vjr5-c9qv-hgm3, CVE-2026-29080)
- Rucio deployments that have explicitly configured the postgres_meta
  metadata plugin, since Rucio server version 1.30.0 
  (GHSA-6j7p-qjhg-9947, CVE-2026-29090).
  
*NOT affected*: PostgreSQL/MySQL deployments using the default json_meta plugin

Fixed versions:

35 LTS -> 35.8.5
38 LTS -> 38.5.5
39 -> 39.4.2
40 -> 40.1.1


## ACTIONS REQUIRED/RECOMMENDED

Sites running Rucio are required to urgently update, using information
in references below. 

All running resources MUST be either patched or have mitigation
in place or software removed by 2026-05-15  00:00 UTC 

Sites failing to act or to respond to requests from the EGI CSIRT team 
risk site suspension. 


## STATUS OF THIS ADVISORY
                   
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-13  

https://advisories.egi.eu/Advisory-SVG-CVE-2026-29080

https://advisories.egi.eu/Advisory-SVG-CVE-2026-29090

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


- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2026-29080> 
    
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2026-29090> 
     
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2026-29080>

- [R 4] <https://www.cve.org/CVERecord?id=CVE-2026-29090>

- [R 5] <https://github.com/rucio/rucio/security/advisories/GHSA-vjr5-c9qv-hgm3>
 
- [R 6] <https://github.com/rucio/rucio/security/advisories/GHSA-6j7p-qjhg-9947>


    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Dr. Martin Barisits 
