---
title: Advisory-EGI-SVG-2026-38
permalink: /Advisory-EGI-SVG-2026-38
redirect_from:
  - /Advisory-SVG-CVE-2026-64561
---

## Advisory-EGI-SVG-2026-38

# Linux kernel "Zapscape" vulnerability 

Date:       2026-08-07

**NOTE:**

Exploits of this vulnerability require **root** access on the guest VM.
Therefore, this mainly concerns hypervisors and virtual machines in
cloud services that give users **root** access in their virtual machines.


## DESCRIPTION

High risk Linux kernel vulnerability "Zapscape" allowing KVM guests
to crash or compromise their host. It is described in detail at [R 1].


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-38
    
CVE ID     : CVE-2026-64561

CVSSv3 Score: 
- Red Hat: 7 - important


## ACTIONS REQUIRED/RECOMMENDED

Urgent action may be required on hypervisors and virtual machines in
cloud services that give users root access in their virtual machines.

At the time of writing, fixed kernels are available for most of the
relevant distributions. Please check the references listed at the bottom
of this advisory for your distribution(s), update and reboot affected
systems as soon as feasible. Fixes are available for RHEL and derivatives.
Please apply mitigation where needed in the meantime.


## MITIGATION

The mitigation described here is essentially the same as for the recent
"Januscape" vulnerability (exploitable by *any* user in an affected VM).

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

To protect an affected VM that does not need nested virtualization,
these commands can also be run instead:

```
modprobe -r kvm_amd kvm_intel || echo A reboot will be needed

cat >/etc/modprobe.d/mitigation-zapscape.conf <<'EOF'
install kvm_amd /bin/false
install kvm_intel /bin/false
blacklist kvm_amd
blacklist kvm_intel
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-38

https://advisories.egi.eu/Advisory-SVG-CVE-2026-64561 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
----
    
## REFERENCES

- [R 1] <https://github.com/V4bel/Zapscape>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-64561>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-64561>
- [R 4] <https://ubuntu.com/security/CVE-2026-64561> (may not exist yet)
- [R 5] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 6] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)

