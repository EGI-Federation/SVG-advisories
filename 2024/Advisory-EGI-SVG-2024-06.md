---
title: Advisory-EGI-SVG-2024-06
permalink: /Advisory-EGI-SVG-2024-06
redirect_from:
  - /Advisory-SVG-CVE-2024-0193
  - /Advisory-SVG-CVE-2023-0646
---

## Advisory-EGI-SVG-2024-06

# HIGH risk Linux Kernel (RHEL9) Vulnerabilities

Date:        2024-03-20   
Updated:     2024-04-19

HIGH risk Linux Kernel (RHEL9) Vulnerabilities

Red Hat has released a new kernel for RHEL9, fixing
Multiple vulnerabilities. [R 1] 

## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2024-06

CVE ID/CVSS Score : CVE-2023-6817/7.8 

CVE ID/CVSS Score : CVE-2024-0193/7.8

CVE ID/CVSS Score : CVE-2023-0646/7.0

(Plus others with CVSS score 7.8 which RedHat considers Moderate)


## ACTIONS REQUIRED/RECOMMENDED

Sites running RHEL9 and derivatives are recommended to update as soon 
as possible, according to the references below.

## MITIGATION

Sites are reminded that kernel vulnerabilities are often mitigated by 
disabling network namespaces as documented in [R 11]


## MORE INFORMATION

EGI-SVG-2024-05 already mentioned CVE-2023-6817 as this was fixed for 
RHEL8 

There are a large number of CVE’s patched in this RHEL9 
release, we have identified the 3 listed above as ‘HIGH’
risk according to our criteria. We have not investigated all
the CVE’s in detail, and there is the possibility that others
may also be ‘HIGH’ but of course sites will be protected
against them if they patch.

    
## STATUS OF THIS ADVISORY
                         
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2024-06 

https://advisories.egi.eu/Advisory-SVG-CVE-2024-0193

https://advisories.egi.eu/Advisory-SVG-CVE-2023-0646

(For CVE-2023-6817 also see https://advisories.egi.eu/Advisory-EGI-SVG-2024-05)

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

- [R 1] <https://access.redhat.com/errata/RHSA-2024:1248> 

- [R 2] <https://access.redhat.com/security/cve/CVE-2023-6817>
     
- [R 3] <https://access.redhat.com/security/cve/CVE-2024-0193>

- [R 4] <https://access.redhat.com/security/cve/CVE-2024-0646>

- [R 5] <https://www.scientificlinux.org/category/sl-errata/>

- [R 6] <https://lists.centos.org/pipermail/centos-announce/>

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2023-6817> 
    
- [R 8] <https://ubuntu.com/security/CVE-2023-6817>

- [R 9] <https://errata.build.resf.org/>   (RockyLinux)

- [R 10] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 11] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this RHEL9 release by Mischa Salle


