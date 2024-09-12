---
title: Advisory-EGI-SVG-2024-15
permalink: /Advisory-EGI-SVG-2024-15
  
---

## Advisory-EGI-SVG-2024-15

# HIGH risk - voms-proxy-init susceptible to proxy theft

Date:        2024-07-31
Updated:     2024-08-02, 2024-09-11

HIGH risk vulnerability concerning the Java version of voms-proxy-init.
During the proxy generation process it is possible for unauthorized
users on the same machine to gain read access to the proxy. 
This allows the user to then perform any action that is possible with 
the original proxy.

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-15
    
CVE ID     : N/A

CVSS Score : N/A 
    
## AFFECTED SOFTWARE AND VERSIONS

The vulnerability was identified in the VOMS Java API (voms-api-java)
v. 3.3.2 and is present in the VOMS Java Clients (voms-clients-java)
v. 3.3.2. Earlier versions may be affected.
  
The vulnerability is fixed in voms-api-java v. 3.3.3 
and in voms-clients-java v. 3.3.4.


## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update voms-api-java to 3.3.3 and 
voms-clients-java to version 3.3.4 as soon as possible using 
information in the references below.


## COMPONENT INSTALLATION INFORMATION

At present, the new version of voms-api-java and voms-clients-java 
are released for EL 9, EL 8 and Centos 7 at [R 2], [R 3] and [R 4].
The rpms are also available from the WLCG repository [R 5].


## MORE INFORMATION

This has been assessed as 'HIGH' risk as it allows impersonation of 
another user.

Some other software is also dependent on the VOMS Java API, but to
our knowledge, none creates new proxies and therefore none should be 
affected by the vulnerability in question.
    
## STATUS OF THIS ADVISORY
                         
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2024-15 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://italiangrid.github.io/voms/>

- [R 2] <https://repo.cloud.cnaf.infn.it/service/rest/repository/browse/voms-rpm-stable/redhat9/>

- [R 3] <https://repo.cloud.cnaf.infn.it/service/rest/repository/browse/voms-rpm-stable/redhat8/>
       
- [R 4] <https://repo.cloud.cnaf.infn.it/service/rest/repository/browse/voms-rpm-stable/centos7/>

- [R 5] <https://linuxsoft.cern.ch/wlcg/>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

This vulnerability was reported by Christophe Haen

