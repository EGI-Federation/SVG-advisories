---
title: Advisory-EGI-SVG-2024-22
permalink: /Advisory-EGI-2024-22
redirect_from:
  - /Advisory-SVG-CVE-2024-0132
  
---

## Advisory-EGI-SVG-2024-22

# CRITICAL risk Nvidia container escape Vulnerability 

Date:        2024-10-02 
Updated:     2024-11-07

CRITICAL risk vulnerability in Nvidia products whereby it is possible to escape containers. [R 1]


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-22
    
CVE ID     : CVE-2024-0132

CVSS Score : 9.0
    
## AFFECTED SOFTWARE AND VERSIONS
    
All Nvidia Container Toolkit versions up to and including v1.16.1.
The vulnerability is fixed in v1.16.2.  [R 1]

This also affects Nvidia GPU Operator up to and including 24.6.1.
The vulnerability is fixed in v24.6.2. [R 2]


## ACTIONS REQUIRED/RECOMMENDED

Sites running Nvidia Container Toolkit or GPU Operator are required to urgently apply vendor patches using information provided by Nvidia. [R 1]
 
All resources running affected Nvidia software MUST be patched or have the software removed by 2024-10-10  00:00 UTC.

Sites failing to act and/or failing to respond to requests from the EGI CSIRT team risk site suspension. 


## MITIGATION

We are not aware of any mitigation. Sites need to patch.


## MORE INFORMATION

RedHat is not affected [R 5]

Also see references below. 
    
## STATUS OF THIS ADVISORY
                       
_TLP:CLEAR information - Unlimited distribution_ 

 
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-22 

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-0132


Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG


-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
--

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvidia.custhelp.com/app/answers/detail/a_id/5582>

- [R 2] <https://www.theregister.com/2024/09/26/critical_nvidia_bug_container_escape>

- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2024-0132> 
     
- [R 4] <https://www.cve.org/CVERecord?id=CVE-2024-0132>

- [R 5] <https://access.redhat.com/security/cve/CVE-2024-0132>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Baptiste Grenier 

