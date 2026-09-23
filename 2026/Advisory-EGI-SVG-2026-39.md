---
title: Advisory-EGI-SVG-2026-39
permalink: /Advisory-EGI-SVG-2026-39
 
---
## Advisory-EGI-SVG-2026-39

# CRITICAL risk Rucio vulnerability 

Date:        2026-08-12


## DESCRIPTION

The Rucio development team has fixed an authentication bypass 
via SSH challenge tokens in Rucio. The issue affects all Rucio  
deployments that expose the `/auth/ssh_challenge_token` API endpoint. 
This is every deployment by default.

The vulnerability is critical: an attacker can receive a valid  
authentication token for any account and use it against any other  
API endpoint to view/modify/delete resources managed by Rucio. 

Supported Rucio versions must be updated accordingly: see below. 

Once a fixed Rucio version is deployed, the fix is active immediately 
irrespective of already issued challenge tokens.


## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2026-39
    
CVE ID     : N/A

CVSS Score : 10.0

    
## AFFECTED SOFTWARE AND VERSIONS
    
Supported Rucio versions must be updated as follows, as soon as possible:

35 LTS -> 35.9.1
38 LTS -> 38.6.1
40 -> 40.4.2
41 LTS -> 41.1.1


## ACTIONS REQUIRED/RECOMMENDED

Sites running Rucio are strongly advised to update and restart Rucio ASAP,  
using information provided above. A mitigation option is provided below.

Rucio service managers can check the access logs if the endpoint  
`/auth/ssh_challenge_token` was accessed at all. If not, all is good. 
Else, IP addresses can be checked to see if the requests were unauthorized  
and then followed further to see if subsequent commands were submitted and 
what their impact was, if any.


## MITIGATION

The Rucio policy package can be adjusted to override the permission request  
`perm_get_auth_token_ssh` to always return False. The service would need to 
be reloaded or restarted for the change to take effect. 

For the Rucio server container image (docker.io/rucio/rucio-server),  
this is handled by Apache `mod_wsgi`. Refer to  
https://www.modwsgi.org/en/develop/user-guides/reloading-source-code.html  
for more information.

If Rucio is deployed in high availability (HA) deployments, it should be possible  
to restart each running application server one by one without disrupting the service.  


## STATUS OF THIS ADVISORY
                   
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-39

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
    
See [R 99] for further details, and other information on SVG.
    
    
## REFERENCES
    
- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Benedikt Ziemons of the Rucio Team
     
