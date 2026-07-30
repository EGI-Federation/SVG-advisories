---
title: Advisory-EGI-SVG-2026-27
permalink: /Advisory-EGI-SVG-2026-27
redirect_from:
  - /Advisory-SVG-CVE-2026-43503

---
## Advisory-EGI-SVG-2026-27

# Linux kernel DirtyClone vulnerability 

Date:       2026-06-26


**NOTE:**

All running resources MUST be either patched or have mitigation 
in place or affected services disabled by 2026-07-04, 00:00 UTC. 

Sites failing to act or respond to requests from the EGI CSIRT team 
risk site suspension. [R 98]


## DESCRIPTION

CRITICAL risk Linux kernel vulnerability "DirtyClone" 
allowing local privilege escalation to root [R 1].


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-27
    
CVE ID     : CVE-2026-43503

CVSSv3 Score: 
- Red Hat: 7 [R 2]
- EGI SVG: critical


## ACTIONS REQUIRED/RECOMMENDED

Urgent action is required on hosts giving access to unprivileged users, 
e.g. grid worker nodes, but also container hosts, notebook servers and 
CI runners.

At the time of writing, fixed kernels are only available for some of the 
relevant distributions. Please check the references listed at the bottom 
of this advisory for your distribution(s), update and reboot affected 
systems as soon as feasible.

Please apply these mitigation commands on affected hosts in the meantime: 

```
modprobe -r esp4 esp6 rxrpc
cat >/etc/modprobe.d/mitigation-dirtyclone.conf <<'EOF'
install esp4 /bin/false
install esp6 /bin/false
install rxrpc /bin/false
blacklist esp4
blacklist esp6
blacklist rxrpc
EOF
echo 3 > /proc/sys/vm/drop_caches
```

They are sufficient to prevent potential exploits and 
are not expected to affect vital functionality.

A reboot is not needed just to apply those mitigations.

If such a module is reported as being in use: 
- if the usage is legitimate, other mitigation would have to be found, 
  e.g. making the service unavailable to unprivileged users or 
  disabling unprivileged namespaces (see below); 
- if the usage is not legitimate, the service may be compromised, 
  which would then need to be handled as a security incident.
   
Alternatively, unprivileged **network** namespaces can be disabled:
please see [R 7] for details.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_  

https://advisories.egi.eu/Advisory-EGI-SVG-2026-27

https://advisories.egi.eu/Advisory-SVG-CVE-2026-43503

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------


## REFERENCES

- [R 1] <https://research.jfrog.com/post/dissecting-and-exploiting-linux-lpe-variant-dirtyclone-cve-2026-43503/>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-43503>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-43503>
- [R 4] <https://ubuntu.com/security/CVE-2026-43503>
- [R 5] <https://errata.build.resf.org/>  (Rocky Linux)
- [R 6] <https://errata.almalinux.org/>  (AlmaLinux)
- [R 7] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>

- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)



