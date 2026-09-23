---
title: Advisory-EGI-SVG-2026-40
permalink: /Advisory-EGI-SVG-2026-40
redirect_from:
  - /Advisory-SVG-CVE-2026-17523  

---

## Advisory-EGI-SVG-2026-40

# HIGH risk Linux kernel CAN BCM vulnerability

Date:       2026-08-19

**NOTE:** RHEL 9, 10 and their derivatives are **NOT** affected.

## DESCRIPTION

An important flaw in the Linux kernel's CAN BCM module allows an unprivileged 
local user to execute arbitrary code within the kernel, which leads to a 
local privilege escalation (LPE). [R 1]


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-40

CVE ID     : CVE-2026-17523

CVSSv3 Score: 
- Red Hat: 7.8 - important risk [R 1]


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to update as soon as possible the Linux kernel on hosts 
giving access to unprivileged users, e.g. grid worker nodes, but also 
container hosts, notebook servers and CI runners.

At the time of writing, fixed kernels are available for most of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible.


## MITIGATION

On concerned hosts that do not need it, the "can_bcm" (sic) module can be
disabled as follows (mind its correct name):

```
modprobe -r can_bcm || echo A reboot is needed for the mitigation to work

cat >/etc/modprobe.d/mitigation-cve-2026-17523.conf <<'EOF'
install can_bcm /bin/false
blacklist can_bcm
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-40

https://advisories.egi.eu/Advisory-SVG-CVE-2026-17523  

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

- [R 1] <https://access.redhat.com/security/cve/cve-2026-17523>
- [R 2] <https://security-tracker.debian.org/tracker/CVE-2026-17523>
- [R 3] <https://ubuntu.com/security/CVE-2026-17523>
- [R 4] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 5] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 6] <https://errata.build.resf.org/RLSA-2026:55764>
- [R 7] <https://errata.almalinux.org/8/ALSA-2026-55764.html>
  - Mind: the fix is present as of kernel-4.18.0-553.156
  - For x86_64, the repositories were not updated initially,
    due to a problem in the AlmaLinux build system that has been fixed

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)

