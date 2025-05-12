---
title: Advisory-EGI-SVG-2025-04
permalink: /Advisory-EGI-SVG-2025-04
redirect_from:
  - /Advisory-SVG-CVE-2024-1974
---

# Advisory-EGI-SVG-2025-04

## CRITICAL risk Kubernetes Ingress NGINX Controller vulnerabilities

Date:        2025-03-26
Updated:     2025-05-12

CRITICAL risk vulnerabilities concerning Kubernetes Ingress NGINX 
Controller enabling remote code execution [R 1]

## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2025-04

CVE ID : CVE-2025-1974 [R 1], CVE-2025-1097 [R 2], CVE-2025-24513 [R 3], CVE-2025-24514 [R 4]

CVSS Score : Up to 9.8 [R 1] 

## ACTIONS REQUIRED/RECOMMENDED

Sites running Kubernetes are required to urgently install the new version  
using information in the references below.

All running resources MUST be either patched or have mitigation
in place or software removed by 2025-04-03  00:00 UTC 

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension. 

## MORE INFORMATION
    
CVE-2025-24513: This vulnerability involves improper input validation,
leading to directory traversal within the container. It can result in
denial-of-service (DoS) or limited disclosure of secret objects
    
CVE-2025-24514: Exploits the auth-url Ingress annotation to inject
configuration into NGINX, enabling arbitrary code execution and
disclosure of secrets
    
CVE-2025-1097: The auth-tls-match-cn Ingress annotation can be used to
inject configuration into NGINX, leading to arbitrary code execution and
secret disclosure
    
CVE-2025-1974: The most severe, allowing unauthenticated attackers to
execute arbitrary code in the context of the ingress-nginx controller,
potentially leading to a cluster takeover
    
Also see references below, especially [R 3] and references therein.

## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_
    
https://advisories.egi.eu/Advisory-EGI-SVG-2025-04 

https://advisories.egi.eu/Advisory-SVG-CVE-2025-1974

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu

(see [R 99] for further details, and other information on SVG)
    
## REFERENCES

- [R 1] <https://www.cve.org/CVERecord?id=CVE-2025-1974> 
     
- [R 2] <https://www.cve.org/CVERecord?id=CVE-2025-1097>
    
- [R 3]  <https://www.cve.org/CVERecord?id=CVE-2025-24513>
    
- [R 4]  <https://www.cve.org/CVERecord?id=CVE-2025-24514>  

- [R 5] <https://kubernetes.io/blog/2025/03/24/ingress-nginx-cve-2025-1974>

- [R 6] <https://thehackernews.com/2025/03/critical-ingress-nginx-controller.html> 
    
- [R 7] <https://github.com/kubernetes/kubernetes/issues/131006>
    
- [R 8] <https://github.com/kubernetes/kubernetes/issues/131007>
        
- [R 9] <https://github.com/kubernetes/kubernetes/issues/131009>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 
