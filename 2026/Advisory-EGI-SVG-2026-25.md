---
title: Advisory-EGI-SVG-2026-25
permalink: /Advisory-EGI-SVG-2026-25

redirect_from:
  - /Advisory-SVG-CVE-2026-46331
  
---

## Advisory-EGI-SVG-2026-25

# Kernel traffic control vulnerability 

Date:       2026-06-23

Update:     2026-06-26
- risk elevated from HIGH to CRITICAL because of public exploit [R 10]
  

**NOTE:**

All running resources MUST be either patched or have mitigation  
in place or affected services disabled by 2026-07-04, 00:00 UTC.

Sites failing to act or respond to requests from the EGI CSIRT team  
risk site suspension. [R 98]


## DESCRIPTION

CRITICAL risk vulnerability concerning kernel traffic control module "act_pedit"  
which can lead to arbitrary code execution in kernel context or a system crash.


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-25
    
CVE ID     : CVE-2026-46331

CVSSv3 Score: 
- Red Hat: 7.8 - high risk [R 2]
- EGI SVG: critical


## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update and reboot services that allow shell 
access by unprivileged users, such as grid worker nodes, or at least 
apply a mitigation as described below. Fixed kernels are available 
for several distributions already: please check the references below. 


## MITIGATION

Please apply these mitigation commands on affected hosts while they 
cannot yet be rebooted with fixed kernels:

```
modprobe -r act_pedit
cat > /etc/modprobe.d/blacklist-act-pedit.conf <<'EOF'
install act_pedit /bin/false
blacklist act_pedit
EOF
```

If the `modprobe` command reports the module being in use, 
the host would need to be rebooted as well.

Alternatively, unprivileged **network** namespaces can be disabled: 
please see [R 9] for details.


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-25

https://advisories.egi.eu/Advisory-SVG-CVE-2026-46331

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/security/vulnerabilities/RHSB-2026-008>
- [R 2] <https://access.redhat.com/security/cve/cve-2026-46331>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2026-46331>
- [R 4] <https://ubuntu.com/security/CVE-2026-46331>
- [R 5] <https://errata.build.resf.org/RLSA-2026:27288>  (fix for RL 10)
- [R 6] <https://errata.build.resf.org/>  (Rocky Linux errata)
- [R 7] <https://errata.almalinux.org/8/ALSA-2026-27353.html>  (fix for AL 8)
- [R 8] <https://errata.almalinux.org/>  (AlmaLinux errata)
- [R 9] <https://csirt.egi.eu/2022/10/19/linux-namespaces-and-containers/>
- [R 10] <https://thehackernews.com/2026/06/new-linux-pedit-cow-exploit-enables.html>
- [R 11] <https://errata.almalinux.org/9/ALSA-2026-27789.html>  (fix for AL 9)
- [R 12] <https://errata.rockylinux.org/RLSA-2026:27789>  (fix for RL 9)
- [R 13] <https://errata.rockylinux.org/RLSA-2026:27353>  (fix for RL 8)

- [R 98] https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+'CRITICAL'+vulnerabilities
- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Laurent Caillat-Vallet (EGI CSIRT)



---
