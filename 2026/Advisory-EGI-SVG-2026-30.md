---
title: Advisory-EGI-SVG-2026-30
permalink: /Advisory-EGI-SVG-2026-30
redirect_from:
  - /Advisory-SVG-CVE-2026-53359 
---

## Advisory-EGI-SVG-2026-30

# Linux kernel "Januscape" vulnerability 

Date:       2026-07-07


**NOTE:**

All running resources MUST be either patched or have mitigation
in place or affected services disabled by 2026-07-15, 00:00 UTC.

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension. [R 98]


## DESCRIPTION

CRITICAL risk Linux kernel vulnerability "Januscape" allowing KVM guests
to crash or compromise their host, as well as local privilege escalation
in the guest VM to root [R 1].


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-30
    
CVE ID     : CVE-2026-53359

CVSSv3 Score: 
- Red Hat: 7 - important [R 2]
- EGI SVG: critical


## ACTIONS REQUIRED/RECOMMENDED

Urgent action is required on hosts giving access to unprivileged users,
e.g. grid worker nodes, but also container hosts, notebook servers and
CI runners.

At the time of writing, fixed kernels are only available for some of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible.  AlmaLinux has patches available that also
fix another important vulnerability [R 7].

To protect an affected host in the meantime, all its guest VMs have to be
stopped to allow these mitigation commands to be applied on the host:

```
modprobe -r kvm_amd kvm_intel
echo "options kvm_amd nested=0" > /etc/modprobe.d/kvm_amd.conf
echo "options kvm_intel nested=0" > /etc/modprobe.d/kvm_intel.conf
```

Then, reload the module corresponding to the CPU flavor of the host:

```
modprobe kvm_amd
```

Or:

```
modprobe kvm_intel
```

Then the stopped VMs can be safely restarted.

To protect an affected VM that needs to make use of nested virtualization
(e.g. for a CI system), consider that VM as being the host and follow the
same procedure.  Otherwise the aforementioned commands are sufficient and
it should not be necessary to reboot the VM.

To protect an affected VM that does not need nested virtualization (e.g.
a grid worker node), these commands can also be run instead:

```
modprobe -r kvm_amd kvm_intel
cat >/etc/modprobe.d/mitigation-januscape.conf <<'EOF'
install kvm_amd /bin/false
install kvm_intel /bin/false
blacklist kvm_amd
blacklist kvm_intel
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------

https://advisories.egi.eu/Advisory-EGI-SVG-2026-30

https://advisories.egi.eu/Advisory-SVG-CVE-2026-53359

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
  

    
## REFERENCES

- [R 1] <https://github.com/V4bel/Januscape>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-53359>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-53359>
- [R 4] <https://ubuntu.com/security/CVE-2026-53359>
- [R 5] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 6] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 7] <https://almalinux.org/ja/blog/2026-07-06-januscape-bad-epoll/>

- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec (EGI CSIRT)
