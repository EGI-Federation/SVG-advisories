---
title: Advisory-EGI-SVG-2026-15
permalink: /Advisory-EGI-SVG-2026-15

redirect_from:
  - /Advisory-SVG-CVE-2026-46300
---

## Advisory-EGI-SVG-2026-15

# CRITICAL risk Linux kernel vulnerability 

Date:       2026-05-13

Updated:    2026-05-29 - handled via EGI-SVG-2026-17
- Rocky Linux 9 standard patches available since May 28
  - Also fixing "ssh-keysign-pwn" [EGI-SVG-2026-17]
- Rocky Linux 8 standard patches available since May 23
  - Ditto

Updated:    2026-05-21
- AlmaLinux standard kernel updates available since May 16 (!)
  - Dealing with ALL recent, serious kernel vulnerabilities!
- RHEL fixes available since May 20
- Rocky Linux patches only available via non-default security repository


**NOTE:**

All running resources MUST be either patched or have mitigation
in place or affected services disabled by 2026-05-21, 00:00 UTC.

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension.

## DESCRIPTION

CRITICAL risk vulnerability concerning the Linux kernel with yet another
very easy public exploit leading to local privilege escalation to root.
It is extensively described at [R 1] [R 2] [R 3] [R 9].


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-15
    
CVE ID     : CVE-2026-46300

CVSSv3 Score: 
- Red Hat: 7.8 [R 4]
- EGI SVG: 8.8 (see below)


## ACTIONS REQUIRED/RECOMMENDED

Urgent action is required on hosts giving access to unprivileged users,
e.g. grid worker nodes, but also container hosts, notebook servers and
CI runners.

At the time of writing, fixed kernels are only available for some of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible.

Please apply these mitigation commands on affected hosts in the meantime:


modprobe -r esp4 esp6 rxrpc
cat >/etc/modprobe.d/mitigation-dirtyfrag.conf <<'EOF'
install esp4 /bin/false
install esp6 /bin/false
install rxrpc /bin/false
blacklist esp4
blacklist esp6
blacklist rxrpc
EOF
echo 3 > /proc/sys/vm/drop_caches


They are sufficient to prevent the published exploits and
are not expected to affect vital functionality.
A reboot is not needed just to apply those mitigations.


## MORE INFORMATION

Compared to the CVSS risk assessment detailed in [R 4],
in some of our deployment scenarios, the "Scope" parameter needs
to have "Changed" as value, which causes the EGI SVG score to have
a significantly higher, more appropriate value.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-15

https://advisories.egi.eu/Advisory-SVG-CVE-2026-46300

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

- [R 1] <https://github.com/v12-security/pocs/tree/main/fragnesia>
- [R 2] <https://www.openwall.com/lists/oss-security/2026/05/13/3>
- [R 3] <https://www.openwall.com/lists/oss-security/2026/05/13/6>
- [R 4] <https://access.redhat.com/security/cve/cve-2026-46300>
- [R 5] <https://security-tracker.debian.org/tracker/CVE-2026-46300>
- [R 6] <https://ubuntu.com/blog/dirty-frag-linux-vulnerability-fixes-available>
  - Mitigation still relevant
- [R 7] <https://errata.build.resf.org/>   (Rocky Linux - see [R 10] [R 11] [R 12] [R 13])
- [R 8] <https://errata.almalinux.org/>  (AlmaLinux - see next item)
- [R 9] <https://almalinux.org/blog/2026-05-13-fragnesia-cve-2026-46300/>
- [R 10] <https://forums.rockylinux.org/t/rocky-linux-security-repository-and-dirty-frag-security-update/20435>
  - Also relevant for this case
- [R 11] <https://forums.rockylinux.org/t/fragnesia-cve-2026-46300/20463>
- [R 12] <https://errata.build.resf.org/RLSA-2026:19568>
- [R 13] <https://errata.build.resf.org/RLSA-2026:19666>

- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by the EGI CSIRT


