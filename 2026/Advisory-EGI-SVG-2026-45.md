---
title: Advisory-EGI-SVG-2026-45
permalink: /Advisory-EGI-SVG-2026-45
 
---

## Advisory-EGI-SVG-2026-45

# HIGH risk apptainer-suid vulnerability

Date:        2026-09-23  
Updated:     2026-10-27


## DESCRIPTION

The Apptainer project has released an advisory about a local privilege
escalation to root in apptainer-suid versions >= 1.5.0 and <= 1.5.3. [R 1]

NOTE: this only affects "setuid" installations at sites.  LHC experiments
and other VOs typically run Apptainer unprivileged from CVMFS, 
depending on what a site actually supports on its worker nodes.


## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2026-45
    
CVE ID     : -

CVSS Score : 
- Apptainer  : 7.8 - HIGH


## ACTIONS REQUIRED/RECOMMENDED

Sites with apptainer-suid installed on hosts that give shell access to
unprivileged users are advised to update to version 1.5.4 and/or apply
one of the documented mitigation methods as soon as possible [R 1].

While rpms for that version are not yet available e.g. from EPEL, they can
be taken from EPEL-testing or the Apptainer repository on GitHub [R 2].


## MITIGATION

Please consult [R 1] for the mitigation methods.


## STATUS OF THIS ADVISORY
                   
_TLP:CLEAR information - Un;imited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-45

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

- [R 1] <https://github.com/apptainer/apptainer/security/advisories/GHSA-4wg8-vhjg-jq8p>
  
- [R 2] <https://github.com/apptainer/apptainer/releases/tag/v1.5.4>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec (EGI CSIRT)
 
  
