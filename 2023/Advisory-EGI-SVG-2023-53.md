---
---
title: Advisory-EGI-SVG-2023-53
permalink: /Advisory-EGI-SVG-2023-53
  
published: false
---

## Advisory-EGI-SVG-2023-53

# 'ADVISORY' [TLP:WHITE] 'HIGH' Risk INDIGO-IAM Vulnerability [EGI-SVG-2023-53]

Date:        2023-09-21
Updated      2023-11-14

A HIGH risk vulnerability has been found concerning 
INDIGO-IAM where a user may be granted rights to which they are not
entitled.  Effectively this is a privilege escalation vulnerability.
This is fixed in INDIGO-IAM version 1.8.1p2 and 1.8.2p2. 

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2023-53
    
CVE ID     : N/A

## ACTIONS REQUIRED/RECOMMENDED

Sites running INDIGO-IAM servers are recommended to update as soon as 
possible, from the github distribution in the reference below. [R 1]

## MORE INFORMATION

Documentation on INDIGO-IAM is available at [R 2], [R 3]

There is also the possibility that an unauthorized user may gain 
authorization by tricking an authorized user to approve a request.
    
## STATUS OF THIS ADVISORY
    
_TLP:WHITE information - Unlimited distribution_ 

<https://advisories.egi.eu/Advisory-EGI-SVG-2023-53> 

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
        
## REFERENCES

- [R 1] <https://github.com/indigo-iam/iam/releases>

- [R 2] <https://indigo-iam.github.io/v/current/docs/tasks/user/client-registration/>

- [R 3] <https://indigo-iam.github.io/v/current/docs/reference/api/oidc-client-registration/>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

This vulnerability discovered by Ahmad Alkhansa. 
The detailed description of the vulnerability was drafted by Roberta Miccoli. 

