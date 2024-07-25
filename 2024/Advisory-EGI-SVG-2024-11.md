---
title: Advisory-EGI-SVG-2024-11
permalink: /Advisory-EGI-SVG-2024-11
redirect_from:
  - /Advisory-SVG-CVE-2024-3727

---

## Advisory-EGI-SVG-2024-11

# Apptainer github/containers/image Vulnerability 

Date:        2024-06-03  
Updated:     2024-07-25

A flaw was found in the github.com/containers/image library. 
This flaw allows attackers to trigger unexpected authenticated registry 
accesses on behalf of a victim user, causing resource exhaustion, 
local path traversal, and other attacks.  [R 1] 

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-11
    
CVE ID     : CVE-2024-3727

CVSS Score : 8.3 [R 2]
    
## AFFECTED SOFTWARE AND VERSIONS
    
This is fixed for version 1.3.2 [R 3]

## ACTIONS REQUIRED/RECOMMENDED

Sites deploying Apptainer are advised to update as soon as possible.

The EGI SVG does not know whether the vulnerability could actually be 
abused in the EGI environment and, if so, how bad such abuse could be.

However, as there likely are sites which deploy their own versions, 
which would then even be setuid root typically, we are sending this 
alert to advise affected sites to update their local installations ASAP. 

If anyone becomes aware of any situation where this vulnerability has a 
significant impact on the EGI infrastructure, then please inform EGI SVG.


## MORE INFORMATION

Given that we cannot rule out serious potential abuse in the EGI environment, 
initially this alert was 'AMBER'.
    
## STATUS OF THIS ADVISORY
    
_TLP:CLEAR information - Unlimited distribution_
                   
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-11 

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-3727 

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

- [R 1] <https://bugzilla.redhat.com/show_bug.cgi?id=2274767>

- [R 2] <https://access.redhat.com/security/cve/CVE-2024-3727>
    
- [R 3] <https://github.com/apptainer/apptainer/releases/tag/v1.3.2>

- [R 4] <https://nvd.nist.gov/vuln/detail/CVE-2024-3727>

- [R 5] <https://www.cve.org/CVERecord?id=CVE-2024-3727>

- [R 6] <https://lists.centos.org/pipermail/centos-announce/>

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2024-3727>
   
- [R 8] <https://ubuntu.com/security/CVE-2024-3727>

- [R 9] <https://errata.build.resf.org/>   (RockyLinux)

- [R 10]  <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99]  <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec

