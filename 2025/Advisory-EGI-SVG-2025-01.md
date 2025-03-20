---
title: Advisory-EGI-SVG-2025-01
permalink: /Advisory-EGI-SVG-2025-01
redirect_from:
  - /Advisory-SVG-CVE-2024-12084
  - /Advisory-SVG-CVE-2024-12085
  - /Advisory-SVG-CVE-2024-12086
  - /Advisory-SVG-CVE-2024-12087
  - /Advisory-SVG-CVE-2024-12088
  - /Advisory-SVG-CVE-2024-12747
  
---

## Advisory-EGI-SVG-2025-01

# Up to CRITICAL Vulnerabilities in rsync
Date: 2025-01-16
Updated: 2025-01-16

<include title without id in the body of txt of e-mail>

6 new vulnerabilities concerning rsync, of which the highest risk rating
is CRITICAL (*not* for RHEL 8/9), have been patched in the latest
release of rsync.


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-01
    
CVE ID     : CVE-2024-12084, CVE-2024-12085, CVE-2024-12086, CVE-2024-12087, CVE-2024-12088, CVE-2024-12747

CVSS Score : Up to 9.8 [R 1]/[R 2]
    
## AFFECTED SOFTWARE AND VERSIONS

Affected versions:
   - CVE-2024-12084 (Critical):
	 upstream >= 3.2.7 and < 3.4.0
	 RHEL 8/9 is *not* affected by this one, but for example Debian is
   - CVE-2024-12085, CVE-2024-12086, CVE-2024-12087, CVE-2024-12088, CVE-2024-12747:
	 upstream: < 3.4.0
	 RHEL 8: < 3.1.3-20
	 RHEL 9: < 3.2.3-20
    
## ACTIONS REQUIRED/RECOMMENDED
 
Sites running vulnerable versions of rsync are required to urgently upgrade.

All running resources MUST be either patched or have mitigation
in place or software removed by 2025-01-24  00:00 UTC.

Sites failing to act and/or failing to respond to requests from the EGI CSIRT team risk site suspension. 

## COMPONENT INSTALLATION INFORMATION

Sites should update the relevant components using the RedHat or other vendor sources.

See references below for further information.


## MORE INFORMATION

A list of CVE IDs and CVSS scores:
 - CVE-2024-12084: 9.8
 - CVE-2024-12085: 7.5
 - CVE-2024-12086: 6.1
 - CVE-2024-12087: 6.5
 - CVE-2024-12088: 6.5
 - CVE-2024-12747: 5.6

For a full list of vulnerabilities with their descriptions, affected versions and mitigations, please see [R 1].
    
[R 3] Contains a handy table to determine if your platform and version is affected. We recommend reffering to this page to determine if you are affected.

## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_

https://advisories.egi.eu/Advisory-EGI-SVG-2025-01
    
https://advisories.egi.eu/Advisory-SVG-CVE-2024-12084
  
Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://www.openwall.com/lists/oss-security/2025/01/14/3>

- [R 2] <https://lists.samba.org/archive/rsync-announce/2025/000120.html>

- [R 3] <https://kb.cert.org/vuls/id/952657>

- [R 4] <https://security-tracker.debian.org/tracker/source-package/rsync>
    
- [R 5] <https://ubuntu.com/security/CVE-2024-12084>

- [R 6] <https://errata.build.resf.org/>   (RockyLinux)

- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
    
       
Red Hat advisories: 
    
- [R 8] <https://access.redhat.com/errata/RHSA-2025:0325> (RHEL8)
    
- [R 9] <https://access.redhat.com/errata/RHSA-2025:0324> (RHEL9)

  
Links to notes concerning the critical CVE:
    
- [R 10] <https://www.cve.org/CVERecord?id=CVE-2024-12084>
    
- [R 11] <https://access.redhat.com/security/cve/CVE-2024-12084>
    
- [R 12] <https://nvd.nist.gov/vuln/detail/CVE-2024-12084>
    
Other:

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krašovec.
