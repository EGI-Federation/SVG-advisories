---
title: Advisory-EGI-SVG-2025-21
permalink: /Advisory-EGI-SVG-2025-21
redirect_from:
  - /Advisory-SVG-CVE-2025-49844

---

## Advisory-EGI-SVG-2025-21

# CRITICAL risk Redis vulnerability

Date:        2025-10-09  
Updated:     2025-12-03


CRITICAL risk Lua use-after-free vulnerability in Redis 
which may lead to remote code execution. [R 1]
    
This is used at least in some EGI Federated Cloud sites, but we (EGI SVG)
do not know whether sites are actually exposed, as is explained below.  


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-21
    
CVE ID     : CVE-2025-49844

CVSS Score : 10.0 [R 1]
    

## ACTIONS REQUIRED/RECOMMENDED

Sites running Redis are required to urgently check whether or not they are 
vulnerable and - if they are - to either upgrade to a patched version as
detailed in [R 1], or carry out mitigation detailed below. 

All running resources MUST be either patched or have mitigation
in place or software removed by 2025-10-17  00:00 UTC 

Sites failing to act or respond to requests from the EGI CSIRT
risk site suspension. 



## MITIGATION

A workaround for this issue - without patching the redis-server executable - 
is to prevent users from executing Lua scripts. This can be done using ACLs
to  restrict EVAL and EVALSHA commands. [R 2]
       
It is also possible to just disable EVAL and EVALSHA as a mitigation, 
by adding the following to the redis.conf:
    
    rename-command EVAL ""
    rename-command EVALSHA ""

And restart the service.
           

## MORE INFORMATION

By default, OpenStack tenants should not be able to run EVAL and 
EVALSHA commands (Lua scripts) on Redis instances used by OpenStack. 

For any Redis instance where users are allowed to run such commands,
this vulnerability should be considered 'CRITICAL' risk. 

In any case, sites running Redis should check [R 1] for advice on
configuration best practices to minimize the risk of potential abuse.

We recommend patching Redis even if the service happens not to be
vulnerable in its current configuration.

    
## STATUS OF THIS ADVISORY

                        
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2025-21 

 https://advisories.egi.eu/Advisory-SVG-CVE-2025-49844

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

- [R 1] <https://redis.io/blog/security-advisory-cve-2025-49844/>
    
- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2025-49844>
    


- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 
    
 
