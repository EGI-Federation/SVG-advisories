---
title: Advisory-EGI-SVG-2026-48
permalink: /Advisory-EGI-SVG-2026-48
redirect_from:
  - /Advisory-SVG-CVE-2026-74580
---

## Advisory-EGI-SVG-2026-48

# HIGH risk Linux kernel "vghost" vulnerability

Date:       2026-10-15  
Updated:    2026-11-17

## DESCRIPTION

A flaw in the "vhost" Linux kernel module may allow a local attacker to  
achieve privilege escalation [R 1] [R 2]. A PoC exploit has been published, 
which might serve as a basis for actual privilege escalation code. 


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-48

CVE ID     : CVE-2026-74580

CVSSv3 Score: 
- Red Hat: 8.7 - important [R 3]


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to update as soon as possible the Linux kernel on hosts  
giving access to unprivileged users, e.g. grid worker nodes, container hosts,  
notebook servers and CI runners. Mitigation is documented below. 

An extra reason for sites to **update** the kernel to the latest version  
is that **many** other vulnerabilities have been fixed in recent weeks,  
for some of which exploits may also still be published. 

At the time of writing, fixed kernels are available since August.  
Please check the references listed at the bottom of this advisory for your  
distribution(s), update and reboot affected systems as soon as feasible.


## MITIGATION

The vulnerability can be mitigated as follows, but mind that this may  
seriously degrade I/O performance in certain deployments [R 3]:

```
modprobe -r vhost_net vhost_vsock vhost || \
    echo A reboot is needed for this mitigation to work

# the next one is mentioned in [R 3] but was not found on our test hosts
modprobe -r vhost_scsi

cat >/etc/modprobe.d/mitigation-CVE-2026-74580.conf <<'EOF'
blacklist vhost
install vhost /bin/false
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-48 

https://Advisory-SVG-CVE-2026-74580

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

- [R 1] <https://www.openwall.com/lists/oss-security/2026/10/14/2>
- [R 2] <https://matrix.tencent.com/en/2026/10/12/vghost-cve-2026-74580>
- [R 3] <https://access.redhat.com/security/cve/cve-2026-74580>
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-74580>
- [R 5] <https://ubuntu.com/security/CVE-2026-74580>
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by the CERN Computer Security Team

