---
title: Advisory-EGI-SVG-2023-54
permalink: /Advisory-EGI-SVG-2023-54
redirect_from:
  - /Advisory-SVG-CVE-2023-42753

---

## Advisory-EGI-SVG-2023-42753

Date:        2024-01-30
Updated      2024-03-15

# HIGH risk array indexing vulnerability in netfilter

HIGH risk array indexing vulnerability in the netfilter subsystem of the Linux kernel  
which may allow a local user to crash the system or potentially escalate their privileges   
on the system.[R 1] [R 2] This affects RHEL7, RHEL8, RHEL9 and derivatives

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2023-54
    
CVE ID     : CVE-2023-42753

CVSS Score : 7.8 [R 1] 

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible. 
See references below for further information. 

## MORE INFORMATION

A Proof of Concept exploit has been published [R 4], but it would at most crash  
the OS and not lead to a privilege escalation. 
The vulnerability can be exploited only by a local user.  
Hence sites should update their affected Grid Worker Nodes, User Interfaces and other 
 shared user systems as the risk may be higher than suggested by the CVSS score.    
    
## STATUS OF THIS ADVISORY
                         
_TLP:CLEAR information - Unlimited distribution_ 
    
https://advisories.egi.eu/Advisory-EGI-SVG-2023-54 

https://advisories.egi.eu/Advisory-EGI-SVG-CVE-2023-42753 

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2023-42753>

- [R 2] <https://access.redhat.com/security/cve/CVE-2023-42753>
    
- [R 3] <https://www.openwall.com/lists/oss-security/2023/09/22/10>

- [R 4] <https://lists.centos.org/pipermail/centos-announce/>

- [R 5] <https://security-tracker.debian.org/tracker/CVE-2023-42753> 
    
- [R 6] <https://ubuntu.com/security/CVE-2023-42753>

- [R 7] <https://errata.build.resf.org/>   (RockyLinux)

- [R 8] <https://errata.almalinux.org/>  (AlmaLinux)
    
- [R 9] <https://www.scientificlinux.org/category/sl-errata/>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS
  
EGI SVG was alerted to this vulnerability by Barbara Krasovec


