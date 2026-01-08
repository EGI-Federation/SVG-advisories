---
title: Advisory-EGI-SVG-2025-17
permalink: /Advisory-EGI-SVG-2025-17
redirect_from:
  - /Advisory-SVG-CVE-2025-40300
---

## Advisory-EGI-SVG-2025-17

# CRITICAL risk VMSCAPE virtualization escape vulnerability

Date:        2025-09-17  
Updated:     2025-11-25, 2026-01-08

CRITICAL risk vulnerability (VMScape) that can be used to attack Linux 
userspace hypervisor software affecting e.g. cloud platforms. [R 1]

**UPDATE 2025-11-25 - Patches are now available for most distributions**

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-17
    
CVE ID     : CVE-2025-40300

CVSS Score : 6.5
    

## ACTIONS REQUIRED/RECOMMENDED

**UPDATE 2025-11-25** 

Sites running running untrusted VMs (e.g. cloud platforms) should update
as soon as possible when patches are available for their distribution,
if they have not done so already. Most distributions have the patches now.

See references below.

## MORE INFORMATION

While RedHat considers this issue to be of 'MODERATE' severity [R 2] due to
it being a local privilege escalation, the EGI SVG considers such a problem
whereby a user can escape a virtual appliance in combination with a public
exploit to be a 'CRITICAL' vulnerability.

A single compromised VM is probably sufficient to launch an attack on a 
hypervisor and then move on to other parts of the underlying infrastructure.


## STATUS OF THIS NOTIFICATION
                       
_TLP:CLEAR information - Unlimited distribution_ 

 This advisory will be made public on or after 24th December 2025 at:- 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-17 

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-40300

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

- [R 1] <https://comsec.ethz.ch/research/microarch/vmscape-exposing-and-exploiting-incomplete-branch-predictor-isolation-in-cloud-environments/>

- [R 2] <https://access.redhat.com/security/cve/CVE-2025-40300>

- [R 3] <https://github.com/comsec-group/vmscape>

- [R 4] <https://nvd.nist.gov/vuln/detail/CVE-2025-40300> 
     
- [R 5] <https://www.cve.org/CVERecord?id=CVE-2025-40300>

- [R 6] <https://security-tracker.debian.org/tracker/CVE-2025-40300> 
    
- [R 7] <https://ubuntu.com/security/CVE-2025-40300>

- [R 8] <https://errata.build.resf.org/>   (RockyLinux)

- [R 9] <https://errata.almalinux.org/>  (AlmaLinux)
      

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS


SVG was alerted to this vulnerability by Vincent Legoll
