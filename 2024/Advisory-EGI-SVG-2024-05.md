---
title: Advisory-EGI-SVG-2024-05
permalink: /Advisory-EGI-SVG-2024-05
redirect_from:
  - /Advisory-SVG-CVE-2023-4623
  - /Advisory-SVG-CVE-2023-4921
  - /Advisory-SVG-CVE-2023-6817
  
---

## Advisory-EGI-SVG-2024-05

# HIGH risk Linux Kernel Vulnerabilities 

Date:        2024-03-06  
Updated:     2024-04-10

Red Hat has released a new kernel for RHEL8, fixing 
Multiple vulnerabilities. [R 1] 
Some of these also affect RHEL9 [R 2] and RHEL7


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-05

CVE ID/CVSS Score     : CVE-2023-4623/7.8 
Affecting RHEL7, RHEL8, and RHEL9

CVE ID/CVSS Score     : CVE-2023-4921/7.8 
Affecting RHEL7 and RHEL8 

CVE ID/CVSS Score     : CVE-2023-6817/7.8 
Affecting RHEL8 and RHEL9


## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon 
as possible, when patches for the versions of Linux they deploy 
are available according to the references below. 
 

## MORE INFORMATION
    
There are a large number of CVE's patched in these RedHat 
releases, we have identified the 3 listed above as 'HIGH' 
risk according to our criteria.  We have not investigated all 
the CVE's in detail, and there is the possibility that others 
may also be 'HIGH' but of course sites will be protected 
against them if they patch.

## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_  

 https://advisories.egi.eu/Advisory-EGI-SVG-2024-05 

 https://advisories.egi.eu/Advisory-SVG-CVE-2023-4623
 
 https://advisories.egi.eu/Advisory-SVG-CVE-2023-4921 
 
 https://advisories.egi.eu/Advisory-SVG-CVE-2023-6817 

 (For CVE-2023-6817 also see https://advisories.egi.eu/Advisory-EGI-SVG-2024-06 )

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

- [R 1] <https://access.redhat.com/errata/RHSA-2024:0897> 

- [R 2] <https://access.redhat.com/errata/RHSA-2024:0461>
     
- [R 3] <https://access.redhat.com/security/cve/CVE-2023-4623>

- [R 4] <https://access.redhat.com/security/cve/CVE-2023-4921>

- [R 5] <https://access.redhat.com/security/cve/CVE-2023-6817>

- [R 6] <https://lists.centos.org/pipermail/centos-announce/>

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2023-4623> 
    
- [R 8] <https://ubuntu.com/security/CVE-2023-4623>

- [R 9] <https://errata.build.resf.org/>   (RockyLinux)

- [R 10]  <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

EGI SVG was alerted to these vulnerabilites by Mischa Salle


