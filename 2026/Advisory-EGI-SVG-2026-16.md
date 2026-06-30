---
title: Advisory-EGI-SVG-2026-16
permalink: /Advisory-EGI-SVG-2026-16

redirect_from:
  - /Advisory-SVG-CVE-2026-42945
---

## Advisory-EGI-SVG-2026-16

# HIGH risk nginx vulnerability 

Date:       2026-05-14

Updated:    2026-05-21  
- Fixes for RHEL 8, 9 and 10 available since May 18-20
- Fixes for Rocky Linux 8, 9 and 10 available since May 18-21


## DESCRIPTION

HIGH risk vulnerability concerning "nginx" module "ngx_http_rewrite_module"
used by many webservices.  It is extensively described at [R 1] [R 2].


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-16
    
CVE ID     : CVE-2026-42945

CVSSv3 Score: 
- Red Hat: 8.1 - critical risk [R 2]
- EGI SVG: high risk (see below)


## ACTIONS REQUIRED/RECOMMENDED

Sites are strongly recommended to patch their nginx instances
as soon as possible.  At the time of writing, patches are only
available for very few distributions.  AlmaLinux has patches.
Please consult the references listed below for your distribution(s).
For mitigation options, see [R 1] under:

    "Temporary mitigation: rewrite your rewrites"


## MORE INFORMATION

Compared to the CVSS critical risk assessment detailed in [R 2],
EGI SVG judges the risk to be high, because of the complexity of
pulling off an actual exploit instead of a DoS (see [R 1]).
However, if an actual exploit gets published, the risk will become critical.
Therefore, please patch your instances as soon as possible!


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_  

https://advisories.egi.eu/Advisory-EGI-SVG-2026-16

https://advisories.egi.eu/Advisory-SVG-42945 

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

- [R 1] <https://almalinux.org/blog/2026-05-13-nginx-rift-cve-2026-42945/>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-42945>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-42945>
- [R 4] <https://ubuntu.com/security/notices/USN-8271-1>
- [R 5] <https://forums.rockylinux.org/>  (Rocky Linux forum)
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux errata)
- [R 7] <https://errata.almalinux.org/>  (AlmaLinux - see [R 1])

- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by the EGI CSIRT

