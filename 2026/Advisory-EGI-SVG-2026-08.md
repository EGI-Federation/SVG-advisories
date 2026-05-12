---
title: Advisory-EGI-SVG-2026-08
permalink: /Advisory-EGI-SVG-2026-08

redirect_from:
  - /Advisory-SVG-CVE-2026-3288
  
---

## Advisory-EGI-SVG-2026-08

# 'HIGH' risk ingress-nginx vulnerability  [EGI-SVG-2026-08]

Date:        2026-03-11 
Updated:     2026-05-12

HIGH risk vulnerability concerning ingress-nginx which may lead to
arbitrary code execution in the context of the ingress-nginx controller
and to disclosure of secrets accessible to the controller. [R 1]
This may affect any Kubernetes cluster where authorised users can create
ingress resources, potentially making secrets accessible that are not theirs.


## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2026-08
    
CVE ID     : CVE-2026-3288

CVSS Score : 8.8 [R 1] [R 2]
    
## AFFECTED SOFTWARE AND VERSIONS
    
- ingress-nginx: < 1.13.8
- ingress-nginx: < 1.14.4
- ingress-nginx: < 1.15.0


## ACTIONS REQUIRED/RECOMMENDED

Sites should update according to [R 3] below.
    
If it is difficult to do this immediately, sites should carry out the mitigation below. 

If anyone becomes aware of any situation (other than in the FedCloud) 
where this vulnerability may have a significant impact on the EGI 
infrastructure, then please inform EGI SVG.

## MITIGATION 
                         
This vulnerability can be mitigated by using admission control to 
block the use of the rewrite-target annotation.

## MORE INFORMATION

We are sending this advisory to all sites, not just Cloud sites,
as we deem it advisable for any site using ingress-nginx to update.

We also note that in certain deployments users are already privileged
and hence have already access to all secrets. 
    
## STATUS OF THIS ADVISORY 
                        
_TLP:CLEAR information - Unimited distribution_ 
                         
 https://advisories.egi.eu/Advisory-EGI-SVG-2026-08 

 https://advisories.egi.eu/Advisory-SVG-CVE-2026-3288 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://www.cve.org/CVERecord?id=CVE-2026-3288> 
     
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2026-3288>

- [R 3] <https://kubernetes.github.io/ingress-nginx/deploy/upgrade/>

- [R 4] <https://github.com/kubernetes/kubernetes/issues/137560>
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 
