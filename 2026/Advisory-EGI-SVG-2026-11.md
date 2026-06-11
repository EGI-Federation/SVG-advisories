---
title: Advisory-EGI-SVG-2026-11
permalink: /Advisory-EGI-SVG-2026-11

redirect_from:
  - /Advisory-SVG-CVE-2026-41651
---

# ADVISORY-EGI-SVG-2026-11

## CRITICAL risk PackageKit vulnerability

Date:       2026-05-05
Updated:    2025-06-11


CRITICAL risk vulnerability concerning PackageKit which may lead to 
privilege escalation. The vulnerability allows an unprivileged local
attacker to obtain root access on an affected host. [R 1]


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-11
    
CVE ID     : CVE-2026-41651

CVSS Score : 8.8 [R 1]


## ACTIONS REQUIRED/RECOMMENDED

Sites running PackageKit on hosts giving access to unprivileged users,
e.g. grid worker nodes, must take urgent action.

If anyone becomes aware of any situation where this vulnerability has a
significant impact on the EGI infrastructure, then please inform EGI SVG.


## MORE INFORMATION

A host may be vulnerable only if it makes use of the PackageKit daemon.
Check with these commands:

systemctl status packagekit
systemctl status pkmon

It is not unusual for some of the PackageKit tools and libraries to be
installed on a host without actually being used.

    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-11 

https://advisories.egi.eu/Advisory-SVG-CVE-2026-41651

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

- [R 1] <https://github.security.telekom.com/2026/04/pack2theroot-linux-local-privilege-escalation.html>
    
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2026-41651> 
     
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2026-41651>  

- [R 4] <https://access.redhat.com/security/cve/CVE-2026-41651>

- [R 5] <https://security-tracker.debian.org/tracker/CVE-2026-41651> 
    
- [R 6] <https://ubuntu.com/security/CVE-2026-41651>

- [R 7] <https://errata.build.resf.org/>   (RockyLinux)

- [R 8] <https://errata.almalinux.org/>  (AlmaLinux)

    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Jakub Havrila

    
