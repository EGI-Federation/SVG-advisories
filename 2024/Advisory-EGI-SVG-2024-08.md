---
title: Advisory-EGI-SVG-2024-08
permalink: /Advisory-EGI-SVG-2024-08
redirect_from:
  - /Advisory-SVG-CVE-2024-1086
  
published: false
---

## Advisory-EGI-SVG-2024-1086

# CRITICAL risk Netfilter vulnerability

Date:        2024-04-12   
Updated:     2024-05-24

CRITICAL risk vulnerability in the Netfilter subsystem in the Linux kernel

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-08
    
CVE ID     : CVE-2024-1086

CVSS Score : 7.8 [R 1] [R 2]    

## ACTIONS REQUIRED/RECOMMENDED

Sites should update relevant components as soon as possible, when 
patches for the versions of Linux they deploy are available according 
to the references below.

Sites running distributions where a patched version is not available yet 
are strongly recommended to carry out mitigation, unless this disables 
functionality required.

## MITIGATION

EGI SVG and EGI CSIRT recommend disabling network namespaces where
they are not needed, see [R 6], although we are increasingly becoming
aware of situations where this disables functionality required.

See also [R 2], [R 9] for mitigation in this case, which involves 
disabling the nf_tables module.

## MORE INFORMATION

Although RedHat considers this vulnerability as 'Important' rather
than 'Critical' the EGI SVG has rated as 'Critical' due to the way
the EGI Grid Services function.

**UPDATE 2024-05-24**

This is now fixed for all RedHat derivatives.
    
## STATUS OF THIS ADVISORY 
                  
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-08 

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-1086

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    Others may re-use this information provided they:-
    
    1) Respect the provided TLP classification
    
    2) Credit the EGI (https://www.egi.eu/) Software Vulnerability Group
-----------------------------

    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES


- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2024-1086> 

- [R 2] <https://access.redhat.com/security/cve/CVE-2024-1086>
     
- [R 3] <https://lists.centos.org/pipermail/centos-announce/>
    
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2024-1086> 
    
- [R 5] <https://ubuntu.com/security/CVE-2024-1086>

- [R 6] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>

- [R 7] <https://errata.build.resf.org/>   (RockyLinux)

- [R 8] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 9] <https://access.redhat.com/solutions/41278>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec.
