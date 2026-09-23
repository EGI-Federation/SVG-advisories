---
title: Advisory-EGI-SVG-2026-35
permalink: /Advisory-EGI-SVG-2026-35  
redirect_from:
  - /Advisory-SVG-CVE-2026-53264

---

## Advisory-EGI-SVG-2026-35

# HIGH risk Linux kernel network scheduler vulnerability

Update:     2026-08-18
* Fix available for AlmaLinux 9 [R 12]

Update:     2026-08-17
* Fixes available for RHEL [R 3]
* Fixes available for Rocky Linux [R 9] [R 10]
* Fix available for AlmaLinux 10 [R 11]

Update:     2026-07-31
* Alternative mitigation has been added below

Date:       2026-07-30


## DESCRIPTION

An important flaw in the Linux kernel's network scheduler may allow 
a local attacker to achieve privilege escalation. It is extensively
described at [R 1] [R 2], including public exploit code.

**NOTE:** exploits need unprivileged **network** namespaces to be enabled.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-35

CVE ID     : CVE-2026-53264

CVSSv3 Score: 
- Red Hat: 7 - important risk [R 3]


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to apply mitigation or update as soon as possible the Linux
kernel on hosts giving access to unprivileged users, e.g. grid worker nodes,
but also container hosts, notebook servers and CI runners.

At the time of writing, fixed kernels are available for only a few of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible. Mitigation is described below.


## MITIGATION

To prevent the published method from exploiting the vulnerability,
it is sufficient to disable unprivileged ***network*** namespaces [R 8].

Alternatively, on hosts that do not need to use the kernel modules
featuring in the example exploit, they can be disabled.

Check if either of them happens to be in use:

```
lsmod | egrep 'act_gact|cls_flower' && echo WARNING: this mitigation may not work!
```

To disable the modules:

```
modprobe -r act_gact cls_flower || echo A reboot is needed for this mitigation to work

cat >/etc/modprobe.d/mitigation-cve-2026-53264.conf << 'EOF'
blacklist act_gact
blacklist cls_flower
install act_gact /bin/false
install cls_flower /bin/false
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-35

https://advisories.egi.eu/Advisory-SVG-CVE-2026-53264 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-------

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
See [R 99] for further details, and other information on SVG.

    
## REFERENCES

- [R 1] <https://thehackernews.com/2026/07/researcher-says-ai-helped-develop-linux.html>
- [R 2] <https://starlabs.sg/blog/2026/07-when-ai-makes-0-days-feel-like-n-days/>
- [R 3] <https://access.redhat.com/security/cve/cve-2026-53264>
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-53264>
- [R 5] <https://ubuntu.com/security/CVE-2026-53264>
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 8] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>
- [R 9] <https://errata.build.resf.org/RLSA-2026:54443>
- [R 10] <https://errata.build.resf.org/RLSA-2026:54343>
- [R 11] <https://errata.almalinux.org/10/ALSA-2026-54343.html>
- [R 12] <https://errata.almalinux.org/9/ALSA-2026-54443.html>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)


