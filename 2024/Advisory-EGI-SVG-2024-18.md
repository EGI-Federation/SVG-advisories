---
title: Advisory-EGI-SVG-2024-18
permalink: /Advisory-EGI-SVG-2024-18
redirect_from:
  - /Advisory-SVG-CVE-2023-31315
  
published: false
---

## Advisory-EGI-SVG-2024-18

# HIGH risk SinkClose flaw in AMD EPYC processors 

Date:        2024-12-04  
Updated:     2025-01-29


HIGH risk vulnerability concerning a flaw in AMD EPYC processors which
may allow privilege escalation. [R 1] 
This may be exploited on systems where a user has access to a system 
where they can run code, such as Worker Nodes (WNs), User Interfaces (UI),
VObox, and FedCloud hosts.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-18
    
CVE ID     : CVE-2023-31315

CVSS Score : 7.5 [R 2]

## AFFECTED CPUs

Many AMD CPU models are affected, including all EPYC generations.
See [R 1] for the complete list.

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update firmware if they are running vulnerable
systems as soon as possible using references below if they have not done
so already. 

## MITIGATION

RedHat states that 'Mitigation for this issue is either not available or 
the currently available options do not meet the Red Hat Product Security 
criteria comprising ease of use and deployment, applicability to 
widespread installation base or stability.'

## MORE INFORMATION

See references below.

We apologise for having missed sending this information earlier!
    
## STATUS OF THIS ADVISORY
    
                      
_TLP:AMBER information - Limited distribution_ 

 This advisory will be made public on or after 2025-01-02  at  
 
https://advisories.egi.eu/Advisory-EGI-SVG-2024-18 

https://advisories.egi.eu/Advisory-SVG-CVE-2023-31315 

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

- [R 1] <https://www.amd.com/en/resources/product-security/bulletin/amd-sb-7014.html> 
     
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2023-31315>
 
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2023-31315>

- [R 4] <https://access.redhat.com/security/cve/CVE-2023-31315>

- [R 5] <https://security-tracker.debian.org/tracker/CVE-2023-31315> 
    
- [R 6] <https://ubuntu.com/security/CVE-2023-31315>

- [R 7] <https://errata.build.resf.org/>   (RockyLinux)

- [R 8] <https://errata.almalinux.org/>  (AlmaLinux)
    
- [R 9] <https://www.bleepingcomputer.com/news/security/new-amd-sinkclose-flaw-helps-install-nearly-undetectable-malware/>
    
- [R 10] <https://www.scmagazine.com/news/20-year-old-hardware-flaw-found-in-amd-chips>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 
    
