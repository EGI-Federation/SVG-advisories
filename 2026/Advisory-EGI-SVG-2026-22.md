---
title: Advisory-EGI-SVG-2026-22
permalink: /Advisory-EGI-SVG-2026-22
redirect_from:
  - /Advisory-SVG-CVE-2026-43001

---

## Advisory-EGI-SVG-2026-22

# OpenStack Keystone authorization bypass vulnerabilities 

Date: 2026-05-26


## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2026-22

CVE ID : CVE-2026-43001 (most serious), 
         CVE-2026-42998, CVE-2026-42999, CVE-2026-43000, CVE-2026-44394

CVSS Score : 8.5 (NVD) / 7.9 (MITRE) for CVE-2026-43001


## AFFECTED SOFTWARE AND VERSIONS

Impacted Keystone versions:
    >=14.0.0 <27.0.2, >=28.0.0 <28.0.2, >=29.0.0 <29.0.2

Several vulnerabilities have been disclosed in OpenStack Keystone that allow 
credential delegation and authorization bypass. Depending on configuration and 
enabled Keystone features, these issues could let an authenticated attacker 
perform lateral movement across projects, potentially accessing or modifying 
resources outside their intended scope.

These flaws are tracked under OSSA-2026-015 [1].

Administrators are strongly encouraged to apply the corresponding security 
updates to mitigate the risk of authorization bypass, privilege escalation, 
and unauthorized access.


## ACTIONS REQUIRED/RECOMMENDED

See the links provided for details, upgrade Keystone to a patched version.

## STATUS OF THIS ADVISORY
    
_TLP:CLEAR information - Unlimited distribution_
                   
https://advisories.egi.eu/Advisory-EGI-SVG-2026-22  

https://advisories.egi.eu/Advisory-SVG-CVE-2026-43001  

## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------

See [R 99] for further details, and other information on SVG.
    

## REFERENCES

[1] https://security.openstack.org/ossa/OSSA-2026-015.html

[2] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42998

[3] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-42999

[4] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-43000

[5] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-43001

[6] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-44394

[7] https://launchpad.net/bugs/2148398

[8] https://launchpad.net/bugs/2148477

[9] https://launchpad.net/bugs/2149775

[10] https://launchpad.net/bugs/2149789

[11] https://launchpad.net/bugs/2150089

[12] https://launchpad.net/bugs/2150379


[R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>



## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec



