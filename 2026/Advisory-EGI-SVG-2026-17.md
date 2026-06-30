---
title: Advisory-EGI-SVG-2026-17
permalink: /Advisory-EGI-SVG-2026-17

redirect_from:
  - /Advisory-SVG-CVE-2026-46333
---

## Advisory-EGI-SVG-2026-17

# CRITICAL risk Linux kernel vulnerability

Date:       2026-05-15

Updated:    2026-05-29
- Rocky Linux 9 standard patches available since May 28
  - Also fixing Fragnesia [EGI-SVG-2026-15] 
- Rocky Linux 8 standard patches available since May 23
  - Ditto 

Updated:    2026-05-21
- RHEL fixes available since May 20

Updated:    2026-05-18
- AlmaLinux standard kernel updates available since May 16 (!) 
  - Dealing with ALL recent, serious kernel vulnerabilities! 
- Debian fixes available (not yet for all cases) 

Updated:    2026-05-15
- Description and actions updated, CVE added 
- AlmaLinux patches available since May 15 


**NOTE:**

All running resources MUST be either patched or have mitigation 
in place or affected services disabled by 2026-05-23, 00:00 UTC. 

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension.  See [R 98].


## DESCRIPTION

CRITICAL risk vulnerability concerning the Linux kernel allowing a local 
unprivileged user to read confidential files that should have been 
inaccessible.

A public Proof-of-Concept (PoC) is available that allows host private 
SSH keys and /etc/shadow to be read by anyone. It is extensively 
described at [R 1] [R 2] [R 3] [R 4].


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-17
    
CVE ID     : CVE-2026-46333

CVSSv3 Score: 
- Red Hat: 7.8 - important
- EGI SVG: 8.5 - critical (scope "Changed" considered more appropriate)


## ACTIONS REQUIRED/RECOMMENDED

Urgent action is required on hosts giving access to unprivileged users
such as grid worker nodes.

Please apply mitigation commands from [R 3] on affected hosts as soon as
possible!

At the time of writing, patched kernels are only available for very few
relevant distributions.  AlmaLinux has patches available: see [R 4].


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-17

https://advisories.egi.eu/Advisory-SVG-CVE-2026-46333

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------
    
See [R 99] for further details, and other information on SVG.


## REFERENCES

- [R 1] <https://github.com/0xdeadbeefnetwork/ssh-keysign-pwn>
- [R 2] <https://www.openwall.com/lists/oss-security/2026/05/15/3>
  - and rest of that mail thread
- [R 3] <https://gitlab.cern.ch/ComputerSecurity/mitigations/ssh-keysign/>
- [R 4] <https://almalinux.org/blog/2026-05-15-ssh-keysign-pwn-cve-2026-46333/>
- [R 5] <https://access.redhat.com/security/cve/cve-2026-46333>
- [R 6] <https://forums.rockylinux.org/t/ssh-keysign-pwn-read-root-owned-files-as-unprivileged-user/20481>
- [R 7] <https://security-tracker.debian.org/tracker/CVE-2026-46333>
- [R 8] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 9] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 10] <https://ubuntu.com/security/CVE-2026-46333>

- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by the EGI CSIRT among others.

