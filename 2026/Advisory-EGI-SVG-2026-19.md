---
title: Advisory-EGI-SVG-2026-19
permalink: /Advisory-EGI-SVG-2026-19
redirect_from:
  - /Advisory-SVG-CVE-2026-24187  
---

## Advisory-EGI-SVG-2026-19

# HIGH risk Nvidia driver vulnerabilities

Date:       2026-05-20




## DESCRIPTION

HIGH risk vulnerabilities concerning the Nvidia drivers potentially allowing
denial of service, escalation of privileges, information disclosure, data
tampering, and code execution.  See [R 1] for details.


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-19
    
CVE ID     : CVE-2026-24187 and others with lower scores

CVSSv3 Score: 
- Nvidia: 8.8 - high


## ACTIONS REQUIRED/RECOMMENDED

Urgent action is required on hosts giving access to unprivileged users
such as grid worker nodes.

Please apply updates detailed in [R 1] on affected hosts as soon as possible.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-19

https://advisories.egi.eu/Advisory-SVG-CVE-2026-24187 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------
    
See [R 99] for further details, and other information on SVG.


## REFERENCES

- [R 1] <https://nvidia.custhelp.com/app/answers/detail/a_id/5821>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by the Barbara Krasovec.
