---
title: Advisory-EGI-SVG-2024-24
permalink: /Advisory-EGI-SVG-2024-24
redirect_from:
  - /Advisory-SVG-CVE-2023-49141
  - /Advisory-SVG-CVE-2023-42667
   
---

## Advisory-EGI-SVG-2024-24

# 'ADVISORY' Multiple Intel Processor Vulnerabilities [EGI-SVG-2024-24]

Date:        2024-10-29 
Updated: 

Multiple vulnerabilities were found in some Intel processors, potentially 
allowing privilege escalation, information disclosure and/or a denial of 
service via local access. 

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-24
    
CVE ID     : CVE-2023-23583, CVE-2023-42667, CVE-2023-49141

CVSS Score : Up to 8.8 [R 3] / [R 6] 
     

## ACTIONS REQUIRED/RECOMMENDED

Sites running Intel hardware should look at the announced information 
and take appropriate action using the references below.

Among others, RedHat and derivatives have provided microcode fixes for 
RHEL 9 [R 1] and RHEL 8 [R 2]. Likewise for the different Debian versions [R 9].

If anyone becomes aware of any situation where such a vulnerability has a 
significant impact on the EGI infrastructure, then please inform EGI SVG.
 

## MORE INFORMATION

EGI SVG has already sent an 'Alert' related to one of these vulnerabilities, 
but at the time there were not yet updates available:

   https://advisories.egi.eu/Advisory-EGI-SVG-2023-58

See references below for further information.

More vulnerabilities, but with lower CVSS score, are fixed by the same update.

## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_

                    
   https://advisories.egi.eu/Advisory-EGI-SVG-2024-24 

   https://advisories.egi.eu/Advisory-SVG-CVE-2023-49141
   
   https://advisories.egi.eu/Advisory-SVG-CVE-2023-42667
      

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
    
- [R 1]  <https://access.redhat.com/errata/RHEA-2024:7620>
    
- [R 2]  <https://access.redhat.com/errata/RHEA-2024:8159>
 
- [R 3]  <https://nvd.nist.gov/vuln/detail/CVE-2023-23583>
    
- [R 4]  <https://nvd.nist.gov/vuln/detail/CVE-2023-42667>
    
- [R 5]  <https://nvd.nist.gov/vuln/detail/CVE-2023-49141>

- [R 6]  <https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-00950.html>

- [R 7]  <https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-01038.html>
     
- [R 8]  <https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-01046.html>

- [R 9]  <https://security-tracker.debian.org/tracker/source-package/intel-microcode>
     

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to these vulnerabilities by Mischa Salle and Barbara
Krasovec.
