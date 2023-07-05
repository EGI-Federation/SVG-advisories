---
title: Test-New-Template
permalink: / Test-New-Template
---

##  'ADVISORY' [TLP:AMBER] HIGH risk Linux kernel vulnerability [EGI-SVG-2023-33]

(for testing the new template when put in advisories.egi.eu only) 


Date: 2023-05-17
Updated:

A HIGH risk Use-after-free flaw was found in the Linux kernel’s TLS protocol.

## AFFECTED SOFTWARE AND VERSIONS

EGI SVG ID : EGI-SVG-2023-33
    
CVE ID     : CVE-2023-0461

CVSS Score : 7.8 [R 1]
    


## ACTIONS REQUIRED/RECOMMENDED
    
Affected sites are recommended to update relevant components as soon as possible.

Sites should update the relevant components using the RedHat or other vendor updates, see references below.

## MORE INFORMATION

A use-after-free flaw was found in the Linux kernel’s TLS protocol functionality in how a user installs a tls context (struct tls_context) on a connected TCP socket. This flaw allows a local user to crash or potentially escalate their privileges on the system. [R 1] . For RHEL this only affects RHEL8 and RHEL9 nad their derivatives, 7 and its derivatives are not affected.

The vulnerability can be exploited only by a local user. Hence sites should update their affected Grid Worker Nodes, User Interfaces and other shared user systems as the risk may be higher than suggested by the CVSS score.

Note that Scientific Linux is based on RHEL7 therefore is not affected.



## STATUS OF THIS ADVISORY
                        
** AMBER information - Limited distribution 

 This advisory will be made public on or after 2023-06-14  at  
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2023-33  

 https://advisories.egi.eu/Advisory-EGI-SVG-CVE-2023-0461 

Minor updates may be made without re-distribution to the sites.


## CONTEXT AND INFORMATION ON SVG

See [R 98] for information on how to report vulnerabilities, context and re-use of this information. 

See [R 99] for the EGI SVG software vulnerability handling procedure. 

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
    report-vulnerability at egi.eu (see [R 98] for further details)
    
    
## REFERENCES

[R 1] https://access.redhat.com/security/cve/CVE-2023-0461

[R 2] https://lists.centos.org/pipermail/centos-announce/

[R 3] https://security-tracker.debian.org/tracker/CVE-2023-0461

[R 4] https://ubuntu.com/security/CVE-2023-0461

[R 5] RockyLinux https://errata.build.resf.org/

[R 6] AlmaLinux https://errata.almalinux.org/

[R 98] <info on SVG> (temp link) https://confluence.egi.eu/display/EGISVG/SVG+Advisories

[R 99] https://documents.egi.eu/public/ShowDocument?docid=3867


  
## CREDITS

SVG was alerted to this vulnerability by Mischa Salle 
