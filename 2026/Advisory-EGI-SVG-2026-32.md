---
title: Advisory-EGI-SVG-2026-32
permalink: /Advisory-EGI-SVG-2026-32

---

## Advisory-EGI-SVG-2026-32

# HTCondor Software Suite (HTCSS) security vulnerability

Date:      2026-07-22  
Updated:   2026-09-02

HTCondor Software Suite (HTCSS) vulnerability


## DESCRIPTION 

Vulnerability concerning HTCondor Software Suite (HTCSS).

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-32
    
CVE ID     : N/A

CVSS Score : N/A
    

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update relevant components as soon as possible 
or at least apply the mitigation described below.

The security release versions are 24.0.22, 24.12.22, 25.0.12, and 25.11.1.


## MITIGATION

You can mitigate the vulnerability by removing FS and FS_REMOTE from the set 
of authentication methods that the schedd and shadow daemons will use in a 
client role. In a standard setup, you can add these lines to the configuration 
file(s) on your Access Point(s) and then issue a condor_reconfig:

SCHEDD.SEC_CLIENT_AUTHENTICATION_METHODS = IDTOKENS,KERBEROS,SCITOKENS,SSL,ANONYMOUS 
SHADOW.SEC_CLIENT_AUTHENTICATION_METHODS = IDTOKENS,KERBEROS,SCITOKENS,SSL,ANONYMOUS 


## MORE INFORMATION

The vulnerability allows a user with WRITE authorization to the Access Point  
(e.g. allowed to submit jobs) to authenticate as the condor user to daemons  
running on the Access Point host. This can allow the user to issue  
ADMINISTRATOR-level commands, edit any attribute in any job ClassAd, and  
potentially enable the impersonation of other user accounts on the AP. 
The user can also obtain an IDToken identifying them as the condor user,  
which can be used at any other machines that have the same IDToken signing 
key(s) as the vulnerable Access Point.

    
## STATUS OF THIS ADVISORY
                          
_TLP:CLEAR information - Un;imited distribution_ 


https://advisories.egi.eu/Advisory-EGI-SVG-2026-32 
 

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
    
See [R 99] for further details, and other information on SVG.
    
    
## REFERENCES

- [R 1] <https://htcondor.org/security/vulnerabilities/HTCONDOR-2026-0001>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by the HTCondor team 
