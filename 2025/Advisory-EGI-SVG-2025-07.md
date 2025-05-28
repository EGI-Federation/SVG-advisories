---
title: Advisory-EGI-SVG-2025-07
permalink: /Advisory-EGI-SVG-2025-07
redirect_from:

---

## Advisory-EGI-SVG-2025-07

# perfSONAR privilege escalation Vulnerability

Date: 2025-05-28

MODERATE risk vulnerability/vulnerabilities concerning perfSONAR wherein
excessively permissive sudo rules potentially allow privilege escalation.

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2025-07
    
CVE ID     : N/A

CVSS Score : N/A

## AFFECTED SOFTWARE AND VERSIONS
    
Versions of perfSONAR < 5.2.0 are affected.

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update perfSONAR to versions >= 5.2.0 Beta 1.

If anyone becomes aware of any situation where this vulnerability has a 
significant impact on the EGI infrastructure then please inform EGI SVG.

## MITIGATION

The only suggested mitigation was to remove the particular packages that
have the vulnerability, but that would in turn cause a loss of functionality
that is deemed important for many perfSONAR instances. Given the risk level
being at most moderate, our advice is to update perfSONAR when convenient.

## MORE INFORMATION

The risk of privilege escalation due to this vulnerability is deemed 
moderate at most, since succesful exploitation requires the presence of 
additional vulnerabilities. It was therefore decided NOT to send an 
advisory to sites, but place it only on our advisories web page. 

## STATUS OF THIS ADVISORY

_TLP:CLEAR information - Unlimited distribution_
                   
https://advisories.egi.eu/Advisory-EGI-SVG-2025-07 

 
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

- [R 1] <https://www.perfsonar.net/releasenotes-2025-03-20-5-2-0b1.html>

- [R 2] <https://github.com/perfsonar/pscheduler/pull/1485>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS
    
This vulnerability was reported by Simon Fayer.
