---
title: Advisory-EGI-SVG-2024-04
permalink: /Advisory-EGI-SVG-2024-04
redirect_from:
  - /Advisory-SVG-CVE-2023-51786
---

## Advisory-EGI-SVG-2024-04

# HIGH risk vulnerability in Lustre 

Date:        2024-03-05
Updated:     2024-04-10

HIGH risk vulnerability in Lustre where users may gain access to files 
and/or folders which they should not have permission to access
based on their user or group ID. This may lead to data compromise or
possible privilege escalation. [R 1]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-04
    
CVE ID     : CVE-2023-51786

CVSS Score : N/A

## ACTIONS REQUIRED/RECOMMENDED

Sites running Lustre are recommended to update to Lustre 2.15.4 as soon
possible.

## MITIGATION

It is stated in [R 1] that mitigation may be achieved by disabling
user namespaces. However, this may not be suitable for worker nodes,
if jobs of a supported VO depend on user namespaces for running
containers through unprivileged instances of Apptainer etc. 

    
## STATUS OF THIS ADVISORY
                            
_TLP:CLEAR information - Unlimited distribution_ 
 
 https://advisories.egi.eu/Advisory-EGI-SVG-2024-04 

 https://advisories.egi.eu/Advisory-SVG-2023-51786 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG


-----------------------------
    Others may re-use this information provided they:-
    
    1) Respect the provided TLP classification
    
    2) Credit the EGI (https://www.egi.eu/) Software Vulnerability Group
---------------------------
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES


- [R 1] <http://lists.lustre.org/pipermail/lustre-announce-lustre.org/2024/000270.html>

- [R 2] <https://www.lustre.org/lustre-2-15-4-released/>
     

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 


