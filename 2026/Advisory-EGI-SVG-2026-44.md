---
title: Advisory-EGI-SVG-2026-44
permalink: /Advisory-EGI-SVG-2026-44

redirect_from:
  - /Advisory-SVG-CVE-2026-80844
  - /Advisory-SVG-CVE-2026-81000
  - /Advisory-SVG-CVE-2026-68121
  - /Advisory-SVG-CVE-2026-74469
  - /Advisory-SVG-CVE-2026-68143
    
---

## Advisory-EGI-SVG-2026-44

# HIGH risk Linux kernel vulnerabilities

Date:       2026-09-18


## DESCRIPTION

Flaws in several Linux kernel network modules may allow a local attacker to 
achieve privilege escalation. Most are extensively described at [R 1] [R 2], 
including public exploit code.

**NOTE:** the LPE exploits need unprivileged **network** namespaces to be enabled.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-44

CVE ID     : CVE-2026-80844, CVE-2026-81000, CVE-2026-68121, CVE-2026-74469,
             CVE-2026-68143

CVSSv3 Score: 
- Red Hat: moderate up to important risk [R 3]
- EGI SVG: high risk


## ACTIONS REQUIRED/RECOMMENDED

Sites are advised to apply mitigation **and** update as soon as possible 
the Linux kernel on hosts giving access to unprivileged users, e.g.  
grid worker nodes, container hosts, notebook servers and CI runners. 

An extra reason for sites to **update** the kernel to the latest version 
is that **many** other vulnerabilities have been fixed in recent weeks, 
for some of which exploits may still be published. 

At the time of writing, fixed kernels for the given vulnerabilities are  
available for only a few of the relevant distributions. 
Please check the references listed at the bottom of this advisory for your 
distribution(s), update and reboot affected systems as soon as feasible. 
Mitigation is described below.


## MITIGATION

To prevent most of the published exploit methods from working, 
it is sufficient to disable unprivileged ***network*** namespaces [R 8]: 

```
echo "user.max_net_namespaces = 0"  > /etc/sysctl.d/92-max_net_namespaces.conf 
sysctl -p /etc/sysctl.d/92-max_net_namespaces.conf
```

Sites are **strongly** advised to apply that mitigation on worker nodes etc. 
To our knowledge, on worker nodes etc, there is **no** need to adjust the 
configuration of certain `systemd` modules that refer to network namespaces. 
Some of our sites have been running like that for years without issues. 

The vulnerabilities covered by this advisory can also be prevented by 
making the related modules unavailable, presuming they are not needed:

```
modprobe -r ah6 || echo A reboot is needed for this mitigation to work

cat >/etc/modprobe.d/mitigation-CVE-2026-80844.conf <<'EOF'
blacklist ah6
install ah6 /bin/false
EOF

modprobe -r pppoe || echo A reboot is needed for this mitigation to work

cat >/etc/modprobe.d/mitigation-CVE-2026-68121.conf <<'EOF'
blacklist pppoe
install pppoe /bin/false
EOF

modprobe -r sctp sctp_diag || echo A reboot is needed for this mitigation to work

cat >/etc/modprobe.d/mitigation-CVE-2026-74469.conf <<'EOF'
blacklist sctp
blacklist sctp_diag
install sctp /bin/false
install sctp_diag /bin/false
EOF

modprobe -r slip || echo A reboot is needed for this mitigation to work

cat >/etc/modprobe.d/mitigation-CVE-2026-68143.conf <<'EOF'
blacklist slip
install slip /bin/false
EOF
```

Instead of blacklisting `tun`, which e.g. would break Podman functionality,
we suggest blacklisting OpenVSwitch (OVS):

```
modprobe -r openvswitch || echo A reboot is needed for this mitigation to work

cat >/etc/modprobe.d/mitigation-CVE-2026-81000.conf <<'EOF'
blacklist openvswitch
install openvswitch /bin/false
EOF
```


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-44

https://advisories.egi.eu/Advisory-SVG-CVE-2026-80844
 
https://advisories.egi.eu/Advisory-SVG-CVE-2026-81000

https://advisories.egi.eu/Advisory-SVG-CVE-2026-68121

https://advisories.egi.eu/Advisory-SVG-CVE-2026-74469

https://advisories.egi.eu/Advisory-SVG-CVE-2026-68143


Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    Others may re-use this information provided they:-
    
    1) Respect the provided TLP classification
    
    2) Credit the EGI (https://www.egi.eu/) Software Vulnerability Group
-----------------------------

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
See [R 99] for further details, and other information on SVG.

    
## REFERENCES

- [R 1] <https://www.openwall.com/lists/oss-security/2026/09/18/3>
- [R 2] <https://heyitsas.im/posts/lpe-quartet/>
- [R 3] <https://access.redhat.com/security/cve/cve-2026-80844>, 
        <https://access.redhat.com/security/cve/cve-2026-81000>, 
        <https://access.redhat.com/security/cve/cve-2026-68121>, 
        <https://access.redhat.com/security/cve/cve-2026-74469>, 
        <https://access.redhat.com/security/cve/cve-2026-68143> 
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-80844> etc.
- [R 5] <https://ubuntu.com/security/CVE-2026-80844> etc.
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 7] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 8] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec (EGI CSIRT)

