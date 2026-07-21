---
title: Advisory-EGI-SVG-2026-23
permalink: /Advisory-EGI-SVG-2026-23
redirect_from:
  - /Advisory-SVG-CVE-2026-23111  
---
## Advisory-EGI-SVG-2026-23

# CRITICAL risk Linux vulnerability via nf_tables

Updated:     2026-07-21
Date:        2026-06-10  

CRITICAL risk vulnerability concerning the Linux kernel's nf_tables 
component which can be used to achieve privilege escalation. Public 
exploits have been published.

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-23
    
CVE ID     : CVE-2026-23111

CVSS 3.X Scores :
- Red Hat  : 7.8 - important [R 3]
- EGI SVG  : critical
    

## ACTIONS REQUIRED/RECOMMENDED

Urgent action may be needed on hosts that allow shell or container access by 
unprivileged users and have NOT been rebooted with a recently released kernel, 
but are instead relying on mitigation against previous vulnerabilities 
(e.g. EGI-SVG-2026-{12,14,15,17,21}).  Such hosts should either be rebooted 
with a recent kernel or need to have further mitigation applied, see below. 

In general, we advise sites to update and reboot affected hosts as soon as 
practically feasible, instead of just relying on mitigation for a long time. 

All affected resources MUST be either patched or have mitigation 
in place or be made inaccessible by 2026-06-18  00:00 UTC.


## MITIGATION

To prevent exploitation of the given vulnerability, it is sufficient to 
disable unprivileged **network** namespaces: please see [R 8] for details.


## STATUS OF THIS ADVISORY
                     
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-23 

https://advisories.egi.eu/Advisory-SVG-CVE-2026-23111  

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
----

See [R 99]
   
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2026-23111> 
     
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2026-23111>

- [R 3] <https://access.redhat.com/security/cve/CVE-2026-23111>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-23111> 
    
- [R 5] <https://ubuntu.com/security/CVE-2026-23111>

- [R 6] <https://errata.build.resf.org/>  (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
    
- [R 8] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>

    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Sven Gabriel 


