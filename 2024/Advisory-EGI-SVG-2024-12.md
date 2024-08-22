---
title: Advisory-EGI-SVG-2024-12
permalink: /Advisory-EGI-SVG-2024-12
redirect_from:
  - /Advisory-SVG-CVE-2024-32498
      
published: false
---

## Advisory-EGI-SVG-2024-12

# HIGH risk OpenStack arbitrary file access vulnerability

Date:        2024-07-09
Updated:     2024-08-22

OpenStack arbitrary file access vulnerability

A HIGH risk vulnerability concerning OpenStack has been found where 
it is possible to return a copy of the contents of a file from the 
server resulting in unauthorized access to potentially sensitive data. 
[R 1]


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-12
    
CVE ID     : CVE-2024-32498

CVSS Score : 8.8 [R 5]
    
## AFFECTED SOFTWARE AND VERSIONS
    
- Cinder: <22.1.3, >=23.0.0 <23.1.1, ==24.0.0
- Glance: <26.0.1, ==27.0.0, >=28.0.0 <28.0.2
- Nova: <27.3.1, >=28.0.0 <28.1.1, >=29.0.0 <29.0.3
 
## ACTIONS REQUIRED/RECOMMENDED

Sites running OpenStack should check which version(s) they are running, 
and if running a vulnerable version update as soon as possible using
the references below.

## MORE INFORMATION

This vulnerability is in QCOW2 image processing for Cinder, Glance and Nova. 
By supplying a specially created QCOW2 image which references a specific 
data file path, an authenticated user may convince systems to return a copy 
of that files contents from the server resulting in unauthorized access to 
potentially sensitive data. All Cinder deployments are affected; only 
Glance deployments with image conversion enabled are affected; all Nova 
deployments are affected. [R 1]
    
## STATUS OF THIS ADVISORY   
                      
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2024-12 

https://advisories.egi.eu/Advisory-SVG-CVE-32498 


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

- [R 1] <https://security.openstack.org/ossa/OSSA-2024-001.html>

- [R 2] <https://launchpad.net/bugs/2059809>
    
- [R 3] <http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2024-32498>

- [R 4] <https://nvd.nist.gov/vuln/detail/CVE-2024-32498> 

- [R 5] <https://access.redhat.com/security/cve/CVE-2024-32498>

- [R 6] <https://lists.centos.org/pipermail/centos-announce/>

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2024-32498> 
    
- [R 8] <https://ubuntu.com/security/CVE-2024-32498>

- [R 9] <https://errata.build.resf.org/>   (RockyLinux)

- [R 10]  <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

EGI SVG was alerted to this vulnerability due to subscription to 
the OpenStack lists, Baptiste Grenier, and additionally by 
Sebastian Luna-Valero.
