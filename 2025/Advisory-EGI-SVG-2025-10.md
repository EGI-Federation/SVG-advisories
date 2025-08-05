---
title: Advisory-EGI-SVG-2025-10
permalink: /Advisory-EGI-SVG-2025-10
redirect_from:
  - /Advisory-SVG-CVE-2025-32462
  - /Advisory-SVG-CVE-2025-32463

---

## Advisory-EGI-SVG-2025-10

# Sudo vulnerabilities

Date:        2025-07-02
Updated:     2025-08-05

HIGH risk privilege escalation vulnerabilities found in sudo

## IDs AND CVSS SCORE 

EGI SVG ID: EGI-SVG-2025-10
    
CVE ID: CVE-2025-32462, CVE-2025-32463

CVSS Score: 7.8 [R 4] (N.B. 9.3 for Ubuntu)

HIGH risk privilege escalation vulnerabilities concerning sudo, CVE-2025-32462 and CVE-2025-32463.

## AFFECTED SOFTWARE AND VERSIONS
    
CVE-2025-32462:
- Affects sudo versions 1.8.8 to 1.9.17 inclusive. [R 11]
- RHEL is affected, with fixes available. [R 3]
- Debian is affected, with fixes available. [R 5]
- Ubuntu is also affected, with fixes available. [R 7]
    
CVE-2025-32463:
- Affects sudo versions 1.9.14 to 1.9.17 inclusive. [R 12]
- RHEL is not affected unless non-standard sudo configuration is in effect. [R 4]
- Debian: Only the unstable (trixie) release is affected, in which case the
  risk is CRITICAL, and sudo must be upgraded immediately. [R 6]
- Ubuntu: 24.04 (noble) and later are affected and the risk is CRITICAL.
  Packages must be upgraded immediately. [R 8]

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible using information in the references below.

Sites should be aware that if a public exploit is released which allows easy root access in the EGI infrastructure this vulnerability is likely to be elevated to 'Critical' and sites will then be required to patch or have mitigation in place within 7 days or risk suspension.

## MITIGATION

Mitigations for CVE-2025-32462 can be found on the Red Hat CVE page. [R 3]
    
## STATUS OF THIS ADVISORY
                     
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2025-10

https://advisories.egi.eu/Advisory-SVG-CVE-2025-32462
    
https://advisories.egi.eu/Advisory-SVG-CVE-2025-32463

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
----

Vulnerabilities relevant for EGI can be reported at
                report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2025-32462>
     
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2025-32463>

- [R 3] <https://access.redhat.com/security/cve/cve-2025-32462>

- [R 4] <https://access.redhat.com/security/cve/cve-2025-32463>
    
- [R 5] <https://security-tracker.debian.org/tracker/CVE-2025-32462>
    
- [R 6] <https://security-tracker.debian.org/tracker/CVE-2025-32463>

- [R 7] <https://ubuntu.com/security/CVE-2025-32462>

- [R 8] <https://ubuntu.com/security/CVE-2025-32463>

- [R 9] <https://www.stratascale.com/vulnerability-alert-CVE-2025-32462-sudo-host>
    
- [R 10] <https://www.stratascale.com/vulnerability-alert-CVE-2025-32463-sudo-chroot>
    
- [R 11] <https://www.sudo.ws/security/advisories/host_any/>
    
- [R 12] <https://www.sudo.ws/security/advisories/chroot_bug/>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Pau Cutrina Vilalta

