---
title: Advisory-EGI-SVG-2024-07
permalink: /Advisory-EGI-SVG-2024-07
redirect_from:
  - /Advisory-SVG-CVE-2024-3094
  
published: false
---

## Advisory-EGI-SVG-2024-07

# CRITICAL risk Vulnerability in xz data compression tools

Date:        2024-04-03
A CRITICAL risk vulnerability has been found in recent versions of xz data
compression tools. [R 1] 

Only a few Linux distributions use the versions affected, which does not
include RHEL and its derivatives like RockyLinux and AlmaLinux. 
Hence most EGI sites will not be affected. 
We are sending this alert as a precautionary measure because of the 
severity of this vulnerability.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-07
    
CVE ID     : CVE-2024-3094

CVSS Score : 10.0 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites should check that they DO NOT have a vulnerable version of xz tools
installed. The vulnerable versions are 5.6.0 and 5.6.1.

If anyone becomes aware of any situation where this vulnerability has an 
impact on the EGI infrastructure then please inform EGI SVG.

## MORE INFORMATION

While the vulnerable versions are NOT included in most RedHat versions or 
their derivatives [R 2], they were included in Fedora 40 and 41 which are 
upstream versions of RHEL releases.

Other affected distributions include OpenSUSE Tumbleweed [R 6], 
Gentoo [R 7] and Debian sid (unstable) [R 8].

Also see references below.
   
## STATUS OF THIS ADVISORY
    
_TLP:CLEAR information - Unlimited distribution_
                   
https://advisories.egi.eu/Advisory-EGI-SVG-2024-07 

https://advisories.egi.eu/Advisory-SVG-CVE-2024-3094 

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

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2024-3094>

- [R 2] <https://access.redhat.com/security/cve/CVE-2024-3094>

- [R 3] <https://www.redhat.com/en/blog/urgent-security-alert-fedora-41-and-rawhide-users>

- [R 4] <https://www.openwall.com/lists/oss-security/2024/03/29/4>

- [R 5] <https://github.com/amlweems/xzbot?tab=readme-ov-file#backdoor-format>
    
- [R 6] <https://news.opensuse.org/2024/03/29/xz-backdoor/>

- [R 7] <https://security.gentoo.org/glsa/202403-04>

- [R 8] <https://security-tracker.debian.org/tracker/CVE-2024-3094>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by David Crooks.


