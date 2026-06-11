---
title: Advisory-EGI-SVG-2026-12
permalink: /Advisory-EGI-SVG-2026-12

redirect_from:
  - /Advisory-SVG-CVE-2026-31431
---
## Advisory-EGI-SVG-2026-12

## CRITICAL risk Linux kernel vulnerability 

Date:       2026-04-30
Updated:    2026-05-04

- AlmaLinux kernel package updates are available since May 1. 
- Red Hat have published further mitigation options at [R9].

Updated:    2026-05-06
- Red Hat kernel package updates are available since May 5. 
- Rocky Linux kernel package updates are available since May 6. 

**NOTE:**

All running resources MUST be either patched or have mitigation  
in place or affected services disabled by 2026-05-13, 00:00 UTC. 

Sites failing to act or respond to requests from the EGI CSIRT team 
risk site suspension.

## DESCRIPTION

CRITICAL risk vulnerability concerning the Linux kernel with very 
easy public exploit leading to local privilege escalation to root. 
It is extensively described at [R 1].


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-12
    
CVE ID     : CVE-2026-31431

CVSSv3.x Score:
- Red Hat:  7.8 [R 4]
- EGI SVG:  8.8 (see below)


## ACTIONS REQUIRED/RECOMMENDED

Urgent action is required on hosts giving access to unprivileged users, 
e.g. grid worker nodes, but also container hosts, notebook servers and 
CI runners.

At this time, patched kernels look available for all relevant distributions. 
Please check the references listed at the bottom of this advisory for your 
distribution(s).

There are several mitigation options, some of which are documented here 
and/or in references listed below.  In particular, this strategy has been 
found to work on RHEL and derivatives: 

1. add
    initcall_blacklist=algif_aead_init 
   to the kernel commandline, for example via GRUB_CMDLINE_LINUX 
   in /etc/default/grub 
2. /usr/sbin/grub2-mkconfig -o /boot/grub2/grub.cfg 
3. reboot the machine

A second mitigation option is to install a BPF filter, as exemplified in  
this repository provided by the CERN Computer Security Team:

https://gitlab.cern.ch/ComputerSecurity/mitigations/cve-2026-31431 


## MORE INFORMATION

Compared to the CVSS risk assessment detailed in [R 4], 
in our deployment scenarios, the "Scope" parameter needs to 
have "Changed" as value, which causes the EGI SVG score to have 
a significantly higher, more appropriate value. 


## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-12 

https://advisories.egi.eu/Advisory-SVG-CVE-2026-31431

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
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] https://copy.fail/ 
- [R 2] https://nvd.nist.gov/vuln/detail/CVE-2026-31431 
- [R 3] https://www.cve.org/CVERecord?id=CVE-2026-31431 
- [R 4] https://access.redhat.com/security/cve/cve-2026-31431 
- [R 5] https://security-tracker.debian.org/tracker/CVE-2026-31431 
- [R 6] https://ubuntu.com/security/CVE-2026-31431 
- [R 7] https://errata.build.resf.org/   (Rocky Linux)
- [R 8] https://errata.almalinux.org/   (AlmaLinux)
- [R 9] https://access.redhat.com/security/cve/cve-2026-31431#cve-details-mitigation 

- [R 98]  https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities 

- [R 99] https://confluence.egi.eu/display/EGIBG/SVG+Advisories

  ## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec




