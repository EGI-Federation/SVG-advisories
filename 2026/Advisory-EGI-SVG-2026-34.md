---
title: Advisory-EGI-SVG-2026-34
permalink: /Advisory-EGI-SVG-2026-34
redirect_from:
  - /Advisory-SVG-CVE-2026-64600
  
---

## Advisory-EGI-SVG-2026-34

# XFS file system vulnerability

Update:    2026-07-25
* Fixes available for AlmaLinux 8, 9 and 10 [R 10] [R 11] [R 12]

Date:      2026-07-23


## DESCRIPTION 

CRITICAL risk vulnerability in the copy-on-write functionality of 
the XFS file system may lead to privilege escalation.
It is extensively described in [R 9].


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-34
    
CVE ID     : CVE-2026-64600

CVSSv3 Score: 
- Red Hat: 7.6 - Important [R 1]
- EGI SVG: CRITICAL 
    
    
**NOTE:**

All running resources MUST be either patched or have mitigation
in place or affected services disabled by  2026-07-31  00:00 UTC 

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension. [R 98]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites should take immediate action, either patch (fixed kernels are
available for RHEL, Rocky Linux and AlmaLinux) or apply mitigation.


## MITIGATION

Follow Red Hat’s mitigation guidance in [R 1]

As a temporary mitigation, review the world-writable directories on the affected  
XFS filesystem and remove unnecessary write permissions or move writable directories 
to a different filesystem where appropriate. 


## MORE INFORMATION


At the time of writing, no public exploit has been released but there are some working 
proof-of-concept such as [R 9].

According to the advisory, systems are potentially affected when:

- The filesystem is XFS with reflink enabled (reflink=1).
- The same XFS filesystem contains both privileged files and directories writable by unprivileged users.
- The running kernel does not yet include the vendor fix or backported patch.

You can perform some initial checks with the following commands: 

- Check whether the root XFS filesystem was created with reflink support (reflink=1). -> `xfs_info / | grep reflink=`
- Identify directories writable by unprivileged users without crossing into other mounted filesystems -> `find / -xdev -type d -perm -002 -ls 2>/dev/null`

    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-34 

  https://advisories.egi.eu/Advisory-SVG-CVE-2026-64600

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
---

    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
See [R 99] for further details, and other information on SVG.
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/security/cve/CVE-2026-64600>

- [R 2] <https://security-tracker.debian.org/tracker/CVE-2026-64600> 
    
- [R 3] <https://ubuntu.com/security/CVE-2026-64600>

- [R 4] <https://errata.build.resf.org/>   (RockyLinux)

- [R 5] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 6] <https://nvd.nist.gov/vuln/detail/CVE-2026-64600> 
     
- [R 7] <https://www.cve.org/CVERecord?id=CVE-2026-64600>

- [R 8] <https://www.openwall.com/lists/oss-security/2026/07/22/14>

- [R 9] <https://blog.qualys.com/vulnerabilities-threat-research/2026/07/22/refluxfs-a-linux-kernel-local-privilege-escalation-to-root-in-xfs-cve-2026-64600>

- [R 10] <https://errata.almalinux.org/8/ALSA-2026-39179.html>

- [R 11] <https://forums.almalinux.org/t/refluxfs-lpe-cve-2026-64600/7518/5>
  - the fix is included starting from kernel-5.14.0-687.26.1
  - the update released on 24 July is kernel-5.14.0-687.29.1
    - <https://errata.almalinux.org/9/ALSA-2026-43307.html>

- [R 12] <https://errata.almalinux.org/10/ALSA-2026-39494.html>
    
    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by CERN Computer Security Office


