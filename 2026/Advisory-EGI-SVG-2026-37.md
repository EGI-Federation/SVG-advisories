
---
title: Advisory-EGI-SVG-2026-37
permalink: /Advisory-EGI-SVG-2026-37
redirect_from:
  - /Advisory-SVG-CVE-2026-64564
  
---

## Advisory-EGI-SVG-2026-37

# Linux kernel SCTPhantom vulnerability

Date:       2026-08-07

**NOTE:** on RHEL and derivatives, the affected functionality is 
**disabled** by **default**, but please **check!** Details are below.


## DESCRIPTION

An important flaw in the Linux kernel's SCTP functionality may allow 
a local attacker to achieve privilege escalation. It is extensively
described at [R 1] [R 2].


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-37

CVE ID     : CVE-2026-64564

CVSSv3 Score: 
- Red Hat: N/A
- EGI SVG: high risk


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to apply mitigation or update as soon as possible
the Linux kernel on hosts giving access to unprivileged users, e.g. 
grid worker nodes, container hosts, notebook servers and CI runners.

At the time of writing, fixed kernels are available for very few of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible. Mitigation is described below.


## MITIGATION

On RHEL and derivatives, the affected kernel module "sctp" is provided
by the "kernel-modules-extra" rpm which is **not** installed by default.

To check if the module present, irrespective of how it got installed:

```
ls -l /lib/modules/*/kernel/net/sctp/sctp*
```

If it is installed via the rpm, the module is **blacklisted** by default:

```
# grep sctp /etc/modprobe.d/sctp-blacklist.conf 
blacklist sctp
```

To check if it is loaded:

```
lsmod | grep sctp
```

To prevent it from being loaded at all:

```
cat >/etc/modprobe.d/mitigation-cve-2026-64564.conf <<'EOF'
blacklist sctp
install sctp /bin/false
EOF
```

On concerned hosts, our advice is to make sure the affected module cannot
be used by unprivileged users, by blacklisting or ensuring it is absent.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_  

https://advisories.egi.eu/Advisory-EGI-SVG-2026-37

https://advisories.egi.eu/Advisory-SVG-CVE-2026-64564

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
------

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
See [R 99] for further details, and other information on SVG.

    
## REFERENCES

- [R 1] <https://www.openwall.com/lists/oss-security/2026/08/06/3>
- [R 2] <https://matrix.tencent.com/en/2026/08/06/sctphantom-CVE-2026-64564>
- [R 3] <https://access.redhat.com/security/cve/cve-2026-64564> 
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-64564>
- [R 5] <https://ubuntu.com/security/CVE-2026-64564> 
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)


