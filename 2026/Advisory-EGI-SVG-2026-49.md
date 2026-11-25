---
title: Advisory-EGI-SVG-2026-49
permalink: /Advisory-EGI-SVG-2026-49
redirect_from:
  - /Advisory-SVG-CVE-2026-99999 

---
## Advisory-EGI-SVG-2026-49

# HIGH risk Linux kernel "pwnescape" vulnerability 

Date:       2026-10-23
Updated:    2026-11-25

## DESCRIPTION

A flaw in the Linux kernel's IPv4 subsystem may allow a local attacker or
a guest VM to run arbitrary code on the host, disclose sensitive information
from the host's memory, or crash the host. A VM escape has been demonstrated
by security researchers, but no exploit code has been published so far.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-49

CVE ID     : CVE-2026-99999

CVSSv3 Score: 
- Red Hat: 8.8 - important [R 3]


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to update as soon as possible the Linux kernel on hosts
giving access to unprivileged users directly or through guest VMs, e.g. 
grid worker nodes, container hosts, notebook servers and CI runners.

An extra reason for sites to **update** the kernel to the latest version
is that **many** other vulnerabilities have been fixed in recent weeks
and recent days, for some of which exploits may also still be published. 

At the time of writing, fixed kernels for this vulnerability are available
for many of the relevant distributions. A patched kernel is available for
AL 8 [R 8] and fixes are available for all our EL 9 and 10 variants.
Please check the references listed at the bottom of this advisory for your
distribution(s), update and reboot affected systems as soon as feasible.


## MITIGATION

At the time of writing, reasonable mitigation is not yet available.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-49

https://advisories.egi.eu/Advisory-SVG-CVE-2026-99999 

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
    
See [R 99] for further details, and other information on SVG.

    
## REFERENCES

- [R 1] <https://www.openwall.com/lists/oss-security/2026/10/15/5>
- [R 2] <https://pwn.ai/blog/pwnescape>
- [R 3] <https://access.redhat.com/security/cve/cve-2026-99999>
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-99999>
- [R 5] <https://ubuntu.com/security/CVE-2026-99999>
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 8] <https://almalinux.org/blog/2026-10-16-pwnescape-cve-2026-99999/>
- [R 9] <https://errata.almalinux.org/9/ALSA-2026-86033.html>
- [R 10] <https://errata.almalinux.org/10/ALSA-2026-85321.html>
- [R 11] <https://errata.build.resf.org/RLSA-2026:86033>
- [R 12] <https://errata.build.resf.org/RLSA-2026:85321>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec (EGI CSIRT)


