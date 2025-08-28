---
title: Advisory-EGI-SVG-2025-12
permalink: /Advisory-EGI-SVG-2025-12

redirect_from:
  - /Advisory-SVG-CVE-2025-49794 
  - /Advisory-SVG-CVE-2025-49796
---

## Advisory-EGI-SVG-2025-12

# HIGH risk vulnerabilities in libxml2 

Date:        2025-07-23 
Updated:     2025-08-28

HIGH risk vulnerabilities concerning libxml2 which is a dependency of 
several packages in the EGI UMD.  [R 1], [R 2], [R 3] 


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2025-12
    
CVE ID     : CVE-2025-49794, CVE-2025-49796

CVSS Score : 9.1 [R 1, R 2]

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible 
and restart potentially affected services, using information below.

Sites should be aware that if a public exploit is released which allows 
easy root access or other serious exploitation in the EGI infrastructure, 
this vulnerability could be elevated to 'CRITICAL' risk and sites will then be 
required to patch or have mitigation in place within 7 days or risk suspension. 

If anyone becomes aware of any situation where this vulnerability has a 
significant impact on the EGI infrastructure then please inform EGI SVG.

## MORE INFORMATION

Various items of software in the different Linux distributions, incl RHEL &
EPEL, Debian etc. but also the EGI UMD [R 3] have libxml2 as a direct
dependency. For the UMD components this includes:--

- davix-libs
- eos-xrootd
- gridsite-devel
- gridsite-libs
- nagios-plugins-onedata
- nordugrid-arc-*
- xrootd-libs

However, we do not know if any of those packages make use of libxml2 in
a way that would make the vulnerabilities exploitable. As a consequence,
although the NVD [R 4] and CVE [R 5] say 'CRITICAL' risk, we are currently
assessing this as 'HIGH' risk.

On the other hand, as we neither know which of the given packages are in
fact exploitable, nor the severity of any potential exploit, we do advise
that libxml2 be updated on any host that has it installed and that
services depending on any of the packages listed above are restarted.

    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-12 

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-49794 
 
 https://advisories.egi.eu/Advisory-SVG-CVE-2025-49796 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
--
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/security/cve/CVE-2025-49794>
    
- [R 2] <https://access.redhat.com/security/cve/CVE-2025-49796>

- [R 3] <https://repository.egi.eu/> 

- [R 4] <https://nvd.nist.gov/vuln/detail/CVE-2025-49794> 
     
- [R 5] <https://www.cve.org/CVERecord?id=CVE-2025-49794>

- [R 6] <https://security-tracker.debian.org/tracker/CVE-2025-49794> 

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2025-49796> 

- [R 8] <https://errata.build.resf.org/>   (RockyLinux)

- [R 9] <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Mischa Salle
    
    
