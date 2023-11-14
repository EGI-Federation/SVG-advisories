---
title: Advisory-EGI-SVG-2023-55
permalink: /Advisory-EGI-SVG-2023-55
redirect_from:
  - /Advisory-SVG-CVE-2023-4911
---

## Advisory-EGI-SVG-2023-55

# 'ADVISORY' [TLP:WHITE] HIGH Risk glibc vulnerability 

Date: 2023-10-06
Updated 2023-11-14

HIGH risk buffer overflow vulnerability in GNU C Library's dynamic loader ld.so 
which may lead to privilege escalation. [R 1] [R 2]. This affects RHEL8, RHEL9 
and derivatives, but not RHEL7.

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2023-55
    
CVE ID     : CVE-2023-4911

CVSS Score : 7.8 [R 1] [R 2] 

## ACTIONS REQUIRED/RECOMMENDED

Where possible, sites running vulnerable versions should update as soon as
possible. See references below.  Note that updating requires a re-boot.

Sites also have the option of mitigation, see [R 2]

Sites should be aware that if a public exploit is released which allows easy root 
access in the EGI infrastructure this vulnerability is likely to be elevated to 
'Critical' and sites will then be required to patch or have mitigation in place 
within 7 days or risk suspension. 

## MORE INFORMATION

Since this does not affect RHEL7 and derivatives, scientific Linux is not affected.
    
## STATUS OF THIS ADVISORY
                        
_TLP:WHITE information - Unlimited distribution_ 

<https://advisories.egi.eu/Advisory-EGI-SVG-2023-55> 

<https://advisories.egi.eu/Advisory-EGI-SVG-CVE-2023-4911>

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2023-4911> 

- [R 2] <https://access.redhat.com/security/cve/CVE-2023-4911>

- [R 3] <https://lists.centos.org/pipermail/centos-announce/>

- [R 4] <https://security-tracker.debian.org/tracker/CVE-2023-4911> 
    
- [R 5] <https://ubuntu.com/security/CVE-2023-4911>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet and separately 
by Torsten Harenberg.
