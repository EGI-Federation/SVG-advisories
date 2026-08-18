---
title: Advisory-EGI-SVG-2026-31
permalink: /Advisory-EGI-SVG-2026-31
redirect_from:
  - /Advisory-SVG-CVE-2026-43499  

---
## Advisory-EGI-SVG-2026-31

# Linux kernel vulnerability "GhostLock"

Updated:    2026-07-14 (#2)
* Fix available for Rocky Linux 9 [R 9]
* Fix available for RHEL 8 [R 2]

Updated:    2026-07-14 (#1)
* AlmaLinux fixes available from the standard repositories
  * Please ensure you get a sufficiently recent version! - see [R 7] [R 8]
* Fixes available for RHEL 9 and 10 [R 2]

Updated:    2026-07-09
* AlmaLinux patches available [R 7]

Date:       2026-07-08


## DESCRIPTION

GhostLock (CVE-2026-43499) is a use-after-free vulnerability in the
Linux kernel's rtmutex subsystem, which can be abused for privilege
escalation. It is extensively described at [R 1].
A public PoC has proven to work, there's a public root exploit for at least android.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-31

CVE ID     : CVE-2026-43499

CVSSv3 Score: 
- Red Hat: 7.8 - important risk [R 2]
- EGI SVG: critical


## ACTIONS REQUIRED/RECOMMENDED

Sites are required to update as soon as possible the Linux kernel on hosts 
giving access to unprivileged users, e.g. grid worker nodes, but also 
container hosts, notebook servers and CI runners.

At the time of writing, fixed kernels are available for only some of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible.

In the meantime sites might want to deny unprivileged users access to
affected resources. To our knowledge there is no other mitigation.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-31

https://advisories.egi.eu/Advisory-SVG-CVE-2026-43499  

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

- [R 1] <https://nebusec.ai/research/ionstack-part-2/>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-43499>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-43499>
- [R 4] <https://ubuntu.com/security/CVE-2026-43499>
- [R 5] <https://errata.build.resf.org/>  (Rocky Linux - see [R 9])
- [R 6] <https://errata.almalinux.org/>  (AlmaLinux - see [R 7] [R 8])
- [R 7] <https://almalinux.org/blog/2026-07-09-ghostlock/>
- [R 8] <https://errata.almalinux.org/9/ALSA-2026-38491.html>
- [R 9] <https://errata.build.resf.org/RLSA-2026:38491>
   
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)

