---
title: Advisory-EGI-SVG-2026-33
permalink: /Advisory-EGI-SVG-2026-33
redirect_from:
  - /Advisory-SVG-CVE-2026-46215

---

## Advisory-EGI-SVG-2026-33

# Linux kernel DRM vulnerability

Update:     2026-07-24 
* Fixes available for AlmaLinux 9 and 10 [R 9] [R 10] 

Update:     2026-07-23 
* Fixes available for Rocky Linux 9 and 10 [R 7] [R 8] 

Date:       2026-07-23 


## DESCRIPTION

An important flaw in the Linux kernel's Direct Rendering Manager (DRM)  
subsystem allows a local attacker to achieve arbitrary code execution  
or privilege escalation. It is extensively described at [R 1]. 


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-33

CVE ID     : CVE-2026-46215

CVSSv3 Score: 
- Red Hat: 7.8 - important risk [R 2]


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to update as soon as possible the Linux kernel on hosts 
giving access to unprivileged users, e.g. grid worker nodes, but also 
container hosts, notebook servers and CI runners.

At the time of writing, fixed kernels are available for only a few of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible. Fixes are available for RHEL [R 2].


## MORE INFORMATION

Given that the exploit published in [R 1] does not seem to work on "EL" 9,
we do not yet advise denying access to unprivileged users, but will keep
monitoring the case for new developments. Also see the mitigation below.


## MITIGATION

On hosts that do not need a GPU driver or on which it can temporarily
be made unavailable as a mitigation, the "drm" module can be disabled:

```
modprobe -r drm || echo A reboot is needed for the mitigation to work

cat >/etc/modprobe.d/mitigation-cve-2026-46215.conf <<'EOF'
install drm /bin/false
blacklist drm
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-33

https://advisories.egi.eu/Advisory-SVG-CVE-2026-46215

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

- [R 1] <https://github.com/0xCyberstan/CVE-2026-46215-POC>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-46215>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-46215>
- [R 4] <https://ubuntu.com/security/CVE-2026-46215>
- [R 5] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 6] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 7] <https://errata.build.resf.org/RLSA-2026:43307>
- [R 8] <https://errata.build.resf.org/RLSA-2026:42919>
- [R 9] <https://errata.almalinux.org/9/ALSA-2026-43307.html>
- [R 10] <https://errata.almalinux.org/10/ALSA-2026-42919.html>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)

