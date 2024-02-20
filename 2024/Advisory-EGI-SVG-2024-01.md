---
title: Advisory-EGI-SVG-2024-01
permalink: /Advisory-EGI-SVG-2024-01
redirect_from:
  - /Advisory-SVG-CVE-2023-4206
  - /Advisory-SVG-CVE-2023-4207
  - /Advisory-SVG-CVE-2023-4208
---

## Advisory-EGI-SVG-2024-01

# HIGH risk Linux Privilege Escalation Vulnerabilities

Use-after-free flaws was found in net/sched/cls_fw.c in classifiers 
(cls_fw, cls_u32, and cls_route) in the Linux Kernel. 
This flaw allows a local attacker to perform a local privilege escalation
due to incorrect handling of the existing filter, leading to a kernel
information leak issue. [R 1]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-01
    
CVE ID     : CVE-2023-4206, CVE-2023-4207, CVE-2023-4208 

CVSS Score : 7.8 [R 1]
    
## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible,
see references below, where patches are available.

## MITIGATION

Potential mitigation is to prevent the module cls_u32 from being loaded by 
blacklisting the module to prevent it from loading automatically [R 1]

## MORE INFORMATION

All relevant Linux versions appear to be affected, and most are patched
    
## STATUS OF THIS ADVISORY
                            
_TLP:CLEAR information - Unlimited distribution_ 

 https://advisories.egi.eu/Advisory-EGI-SVG-2024-01 

 https://advisories.egi.eu/Advisory-SVG-CVE-2023-4206  
 https://advisories.egi.eu/Advisory-SVG-CVE-2023-4207  
 https://advisories.egi.eu/Advisory-SVG-CVE-2023-4208

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] https://access.redhat.com/security/cve/CVE-2023-4206
 
- [R 2] https://access.redhat.com/security/cve/CVE-2023-4207

- [R 3] https://access.redhat.com/security/cve/CVE-2023-4208

- [R 4] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-4206
     
- [R 5] https://www.cve.org/CVERecord?id=CVE-2023-4206

- [R 6] https://www.scientificlinux.org/category/sl-errata/

- [R 7] https://lists.centos.org/pipermail/centos-announce/

- [R 8] https://security-tracker.debian.org/tracker/CVE-2023-4206
    
- [R 9] https://ubuntu.com/security/CVE-2023-4206

- [R 10] https://errata.build.resf.org/   (RockyLinux)

- [R 11] https://errata.almalinux.org/  (AlmaLinux)


- [R 99] https://confluence.egi.eu/display/EGIBG/SVG+Advisories

