---
title: Advisory-EGI-SVG-2024-21
permalink: /Advisory-EGI-SVG-2024-21
redirect_from:
  - /Advisory-SVG-CVE-2024-45409
  
published: false
---

## Advisory-EGI-SVG-2024-21

# CRITICAL risk SAML Authentication bypass flaw

Date:        2024-09-20
Updated:     2024-09-26

CRITICAL Risk vulnerability in the omniauth_saml plugin (via the ruby-saml library), 
which is used by e.g. GitLab, allowing potential Authentication bypass.

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-21
    
CVE ID     : CVE-2024-45409

CVSS Score : 10 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Any GitLab services running in the wider EGI infrastructure should urgently 
update using references below.

If anyone becomes aware of any additional situation where this vulnerability 
may have an impact on the EGI infrastructure, then please inform EGI SVG.


## MORE INFORMATION

The Ruby SAML library is used for implementing the client side of a SAML authorization. 
Ruby-SAML in <= 12.2 and 1.13.0 <= 1.16.0 does not properly verify the signature of 
the SAML Response. An unauthenticated attacker with access to any signed SAML response 
(by the IdP) can thus forge a SAML Response/Assertion with arbitrary contents. 
This would allow the attacker to log in as arbitrary user within the vulnerable system. 
This vulnerability is fixed in ruby-saml 1.17.0 and 1.12.3 [R 1], 
omniauth_saml versions 2.2.1, 2.1.2 and 1.10.5 [R3] and 
GitLab versions 17.3.3, 17.2.7, 17.1.8, 17.0.8, 16.11.10 [R2].

Also see references below. 
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-21 

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-45409 


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvd.nist.gov/vuln/detail/CVE-2024-45409> 
     
- [R 2] <https://about.gitlab.com/releases/2024/09/17/patch-release-gitlab-17-3-3-released/>

- [R 3] <https://github.com/omniauth/omniauth-saml/security/advisories/GHSA-cvp8-5r8g-fhvq>

- [R 4] <https://thehackernews.com/2024/09/gitlab-patches-critical-saml.html?_m=3n%2e009a%2e3465%2eta0ao095we%2e2h7f>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by David Crooks. 

