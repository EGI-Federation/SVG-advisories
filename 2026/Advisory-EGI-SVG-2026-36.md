---
title: Advisory-EGI-SVG-2026-36
permalink: /Advisory-EGI-SVG-2026-36

redirect_from:
  - /Advisory-SVG-CVE-2026-64531 
---

## Advisory-EGI-SVG-2026-36

# CRITICAL risk Linux Open vSwitch vulnerability

Update:     2026-08-13
* Fixes available for RHEL [R 3] and Rocky Linux [R 9] [R 10]
* Fixes available for AlmaLinux [R 11] [R 12]

Date:       2026-07-30


**NOTE:** All running resources MUST be either patched or have mitigation
in place or affected services disabled by 2026-08-07 00:00 UTC.

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension. [R 98]


## DESCRIPTION

An important flaw in the Linux kernel's Open vSwitch datapath may allow 
a local attacker to achieve privilege escalation. It is extensively
described at [R 1] [R 2], including public exploit code.

**NOTE:** exploits need unprivileged **network** namespaces to be enabled.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-36

CVE ID     : CVE-2026-64531

CVSSv3 Score: 
- Red Hat: 7.8 - important risk [R 2]
- EGI SVG: critical risk


## ACTIONS REQUIRED/RECOMMENDED

Sites are required to apply mitigation or update as soon as possible
the Linux kernel on hosts giving access to unprivileged users, e.g. 
grid worker nodes, container hosts, notebook servers and CI runners.

At the time of writing, fixed kernels are available for only a few of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible. Mitigation is described below.


## MITIGATION

To prevent the published method from exploiting the vulnerability,
it is sufficient to disable unprivileged ***network*** namespaces [R 8].

Alternatively, prevent any Open vSwitch functionality from being used:

```
modprobe -r openvswitch || echo A reboot is needed for this mitigation to work

cat >/etc/modprobe.d/mitigation-cve-2026-64531.conf <<'EOF'
blacklist openvswitch
install openvswitch /bin/false
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-36

https://advisories.egi.eu/Advisory-SVG-CVE-2026-64531

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
----

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
See [R 99] for further details, and other information on SVG.

    
## REFERENCES

- [R 1] <https://www.openwall.com/lists/oss-security/2026/07/28/8>
- [R 2] <https://github.com/manizada/OVSwrap>
- [R 3] <https://access.redhat.com/security/cve/cve-2026-64531>
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-64531>
- [R 5] <https://ubuntu.com/security/CVE-2026-64531>
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 8] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>
- [R 9] <https://errata.build.resf.org/RLSA-2026:53329>
- [R 10] <https://errata.build.resf.org/RLSA-2026:53330>
- [R 11] <https://errata.almalinux.org/9/ALSA-2026-53329.html>
- [R 12] <https://errata.almalinux.org/10/ALSA-2026-53330.html>

- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Pau Cutrina Vilalta (CERN Computer Security)



