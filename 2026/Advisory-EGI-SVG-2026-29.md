---
title: Advisory-EGI-SVG-2026-29
permalink: /Advisory-EGI-SVG-2026-29

redirect_from:
  - /Advisory-SVG-CVE-2026-46242
---

## Advisory-EGI-SVG-2026-29

# Linux kernel vulnerability "Bad Epoll"

Date:       2026-07-07

Updated:    2026-08-18 


## DESCRIPTION

Bad Epoll (CVE-2026-46242) is a race-condition use-after-free in the
Linux kernel's epoll subsystem, which in principle may lead to privilege
escalation. It is extensively described at [R 1].


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-29

CVE ID     : CVE-2026-46242

CVSSv3 Score: 
- Red Hat: 7 - important risk [R 2]


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to update as soon as possible the Linux kernel on hosts 
giving access to unprivileged users, e.g. grid worker nodes, but also 
container hosts, notebook servers and CI runners.

At the time of writing, fixed kernels are available for only a few of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible. AlmaLinux has patches available that also
fix another vulnerability we are looking into [R 7].


## MORE INFORMATION

Given that the exploit published in [R 1] does not work on "EL" 9 kernels
and Red Hat have rated the complexity for privilege escalation high [R 2],
we do not yet advise denying access to unprivileged users, but will keep
monitoring the case for new developments.

Unfortunately, there is no mitigation besides denying access altogether.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-29

https://advisories.egi.eu/Advisory-SVG-CVE-2026-46242 

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
----

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    Others may re-use this information provided they:-
    
    1) Respect the provided TLP classification
    
    2) Credit the EGI (https://www.egi.eu/) Software Vulnerability Group [R 99]
-----------------------------

    
## REFERENCES

- [R 1] <https://github.com/J-jaeyoung/bad-epoll>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-46242>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-46242>
- [R 4] <https://ubuntu.com/security/CVE-2026-46242>
- [R 5] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 6] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 7] <https://almalinux.org/blog/2026-07-06-januscape-bad-epoll/>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)



