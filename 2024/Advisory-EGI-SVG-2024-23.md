---
title: Advisory-EGI-SVG-2024-23
permalink: /Advisory-EGI-SVG-2024-23
redirect_from:
  - /Advisory-SVG-CVE-2024-47176
  - /Advisory-SVG-CVE-2024-47076
  - /Advisory-SVG-CVE-2024-47175
---

## Advisory-EGI-SVG-2024-23

# HIGH risk CUPS vulnerabilities

Date:        2024-10-04 
Updated:     2024-10-08

HIGH risk vulnerabilities concerning CUPS which may lead to remote code execution.
Note that CUPS is used for printer management.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-23
    
CVE ID     : CVE-2024-47176, CVE-2024-47076, CVE-2024-47175

CVSS Score : Up to 8.6 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Where sites ARE running CUPS, they should update urgently, using references below. 


## MITIGATION

Since this software is related to printer management, it **ought**
**not** to be installed on resources made available to EGI.
Sites may want to use this occasion to make sure of that.


## MORE INFORMATION

Some have assessed this as 'Critical' [R 11], while the EGI SVG is of
the opinion that the assessment by Red Hat is more realistic for EGI,
which then leads to a rating of high risk instead.
A good description is also in [R 12]

    
## STATUS OF THIS ADVISORY
    

_TLP:CLEAR information - Unlimited distribution_
                   
https://advisories.egi.eu/Advisory-EGI-SVG-2024-23

https://advisories.egi.eu/Advisory-SVG-CVE-47175

https://advisories.egi.eu/Advisory-SVG-CVE-47076

https://advisories.egi.eu/Advisory-SVG-CVE-47176

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.

    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2024-47175>

- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2024-47076> 
    
- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2024-47176> 
    
- [R 4] <https://access.redhat.com/security/cve/CVE-2024-47175> 
    
- [R 5] <https://access.redhat.com/security/cve/CVE-2024-47076>

- [R 6] <https://access.redhat.com/security/cve/CVE-2024-47176>

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2024-47175> 
    
- [R 8] <https://ubuntu.com/security/CVE-2024-47175>

- [R 9] <https://errata.build.resf.org/>   (RockyLinux)

- [R 10] <https://errata.almalinux.org/>  (AlmaLinux)

- [R 11] <https://thehackernews.com/2024/09/critical-linux-cups-printing-system.html>

- [R 12] <https://access.redhat.com/security/vulnerabilities/RHSB-2024-002>
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Sebastian Luna Valero 
    

