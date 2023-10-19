---
title: Advisory-EGI-SVG-2023-52
permalink: /Advisory-EGI-SVG-2023-52
redirect_from:
  - /Advisory-SVG-CVE-2023-3610
  - /Advisory-SVG-CVE-2023-4147
  - /Advisory-SVG-CVE-2023-31248
  - /Advisory-SVG-CVE-2023-3390
  - /Advisory-SVG-CVE-2023-4004
  - /Advisory-SVG-CVE-2023-21102
  - /Advisory-SVG-CVE-2023-1637
  - /Advisory-SVG-CVE-2023-35001
  - /Advisory-SVG-CVE-2023-3776
  - /Advisory-SVG-CVE-2023-20593
---
## Advisory-EGI-SVG-2023-52

# HIGH risk Multiple linux Kernel Vulnerabilities 
Red Hat has produced a new release of RHEL9, fixing  
Multiple HIGH risk vulnerabilities. [R 1] 
Some also affect RHEL8, some RHEL7.  
A further release [R 17] of RHEL8 fixes most of the vulnerabilities 
affecting RHEL8. 
Those affecting RHEL7 (with 1 exception) are NOT yet fixed. 

## CVE IDS, CVSS SCORES, AND AFFECTED SOFTWARE VERSIONS

EGI SVG ID : EGI-SVG-2023-52 

CVE's only affecting RHEL9:- 
 
CVE ID/CVSS Score     : CVE-2023-3610/7.8 [R 2]  
CVE ID/CVSS Score     : CVE-2023-4147/7.8 [R 3]  
CVE ID/CVSS Score     : CVE-2023-31248/7.8 [R 4]  

CVE's affecting RHEL9 and RHEL8:- 

CVE ID/CVSS Score     : CVE-2023-3390/7.8 [R 5]  
CVE ID/CVSS Score     : CVE-2023-4004/7.8 [R 6]  
CVE ID/CVSS Score     : CVE-2023-21102/7.8 [R 7]  
CVE ID/CVSS Score     : CVE-2023-1637/5.5 [R 8]  

CVE's affecting RHEL9, RHEL8 and RHEL7:- 

CVE ID/CVSS Score     : CVE-2023-35001/7.8 [R 9]  
CVE ID/CVSS Score     : CVE-2023-3776/7.0 [R 10]  
CVE ID/CVSS Score     : CVE-2023-20593/6.5 [R 11]  
    
## ACTIONS REQUIRED/RECOMMENDED 

Sites running RHEL9 and derivatives are recommended to update relevant  
components as soon as possible, when a patched version is available  
see references below.  

Sites running RHEL8 are also recommended to update relevant components,  
as most of the vulnerabilities affecting RHEL8 have also been fixed. 
    
Sites running RHEL7 are recommended to carry out mitigation,  
unless this disables functionality required, again see references below. 

Sites running various linux derivatives should see references below. 

## MORE INFORMATION

For CVE-2023-20593 (Zenbleed) [R 11] we have already sent and 'ALERT'  
and placed this on our public advisories.  
There is also a RHEL7 patch relating to this. 

## STATUS OF THIS ADVISORY
                
_TLP:WHITE information - Unlimited distribution_  

 <https://advisories.egi.eu/Advisory-EGI-SVG-2023-52> 

Minor updates may be made without re-distribution to the sites. 

## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to 
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at 
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG) 
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/errata/RHSA-2023:5069> 

- [R 2] <https://access.redhat.com/security/cve/CVE-2023-3610>
     
- [R 3] <https://access.redhat.com/security/cve/CVE-2023-4147>

- [R 4] <https://access.redhat.com/security/cve/CVE-2023-31248>

- [R 5] <https://access.redhat.com/security/cve/CVE-2023-3390>

- [R 6] <https://access.redhat.com/security/cve/CVE-2023-4004>

- [R 7] <https://access.redhat.com/security/cve/CVE-2023-21102> 
    
- [R 8] <https://access.redhat.com/security/cve/CVE-2023-1637>

- [R 9] <https://access.redhat.com/security/cve/CVE-2023-35001>

- [R 10] <https://access.redhat.com/security/cve/CVE-2023-3776>

- [R 11] <https://access.redhat.com/security/cve/CVE-2023-20593> 

- [R 12] <https://advisories.egi.eu/Advisory-SVG-CVE-2023-20593>

- [R 13] <https://www.scientificlinux.org/category/sl-errata/>

- [R 14] <https://lists.centos.org/pipermail/centos-announce/>

- [R 15] <https://security-tracker.debian.org/tracker/CVE-2023-3610> 
 (and similar references)
 
- [R 16] <https://ubuntu.com/security/CVE-2023-3610> 
 (and similar references)
 
- [R 17] <https://access.redhat.com/errata/RHSA-2023:5244>

- [R 18] <https://errata.build.resf.org/>   (RockyLinux)

- [R 19] <https://errata.almalinux.org/> (AlmaLinux)

- [R 20] <https://advisories.egi.eu/Advisory-SVG-CVE-2023-20593>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to these vulnerabilities by Mischa Salle


