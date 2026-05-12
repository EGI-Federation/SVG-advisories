---
title: Advisory-EGI-SVG-2026-04
permalink: /Advisory-EGI-SVG-2026-04
redirect_from:
  - /Advisory-SVG-CVE-2026-25506  
---

## Advisory-EGI-SVG-2026-04

# CRITICAL Risk Munge MUNGE buffer overflow vulnerability

Date:        2026-02-12
Updated:     2026-03-24, 2026-05-12

**UPDATE 2026-03-24**

This is now fixed in the popular distributions, therefore
if you have not already patched please do so. 

CRITICAL risk buffer overflow vulnerability concerning MUNGE 
allowing key leakage and credential forgery. 
This may lead to privilege escalation. [R 1]

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-04
    
CVE ID     : CVE-2026-25506

CVSS Score : 7.7 [R 2]
    
## AFFECTED SOFTWARE AND VERSIONS

MUNGE versions 0.5 to 0.5.17.  
    
Fixed in 0.5.18.
                             
                            
## ACTIONS REQUIRED/RECOMMENDED

Update munge and associated packages to 0.5.18 and restart munged.
If you have not done so already. 

All running resources MUST be either patched or have mitigation
in place or software removed by 2026-04-01  00:00 UTC 

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension.

See  [R 98]


## COMPONENT INSTALLATION INFORMATION

Update munge and associated packages to 0.5.18 and restart munged,
using references below.
 
Sites have successfully upgraded to 0.5.18 by building their own
packages from source. [R 4]

    
## MITIGATION

For SLURM, a mitigation is to switch to auth/slurm authentication, 
but this requires the cluster to have no active jobs running.
        
Also see [R 1]


## MORE INFORMATION

EGI SVG considers this vulnerability to be 'CRITICAL' risk because it
potentially allows privilege escalation, and a proof of concept exploit
has been developed.
                
Most SLURM installations depend on MUNGE. Also PBS/Torque and 
HTCondor can be configured to use MUNGE. 


## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 
    
    https://advisories.egi.eu/Advisory-EGI-SVG-2026-04 

    https://advisories.egi.eu/Advisory-SVG-CVE-2026-25506 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
---------     
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES
    
- [R 1] 
<https://github.com/dun/munge/security/advisories/GHSA-r9cr-jf4v-75gh>   

- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2026-25506> 
     
- [R 3] <https://www.cve.org/CVERecord?id=CVE-2026-25506>

- [R 4] <https://github.com/dun/munge/releases/tag/munge-0.5.18>

- [R 5] <https://access.redhat.com/security/cve/CVE-2026-25506>

- [R 6] <https://security-tracker.debian.org/tracker/CVE-2026-25506> 
    
- [R 7] <https://ubuntu.com/security/CVE-2026-25506>

    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 
