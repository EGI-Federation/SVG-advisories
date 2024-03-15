---
title: Advisory-EGI-SVG-2024-03
permalink: /Advisory-EGI-SVG-2024-03
redirect_from:
  - /Advisory-SVG-CVE-2024-21626
  
published: false
---

## Advisory-EGI-SVG-2024-03

# HIGH risk vulnerability in runc affecting containers.

Date:        2024-02-12
Updated:     2024-03-15

HIGH risk vulnerability concerning runc.
A file descriptor leak issue was found in the runc package which may 
allow container escapes. [R 1] [R 2]

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2024-03
    
CVE ID     : CVE-2024-21626

CVSS Score : 8.6 [R 3]
    
## ACTIONS REQUIRED/RECOMMENDED

Sites running affected containers (Docker and Kubernetes containers) 
should update as soon as possible, using links below. 

## MORE INFORMATION

Docker is used in the in EGI Cloud Container Compute service [R 4], 
therefore this is affected.

Kubernetes is also affected.

In some Grid Sites in EGI, Docker or Kubernetes is used to provide Worker Node services. 
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 

  https://advisories.egi.eu/Advisory-EGI-SVG-2024-03 

  https://advisories.egi.eu/Advisory-SVG-CVE-2024-21626 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

Others may re-use this information provided they:-
    
1) Respect the provided TLP classification

2) Credit the EGI (https://www.egi.eu/) Software Vulnerability Group
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/security/vulnerabilities/RHSB-2024-001>

- [R 2] <https://github.com/opencontainers/runc/security/advisories/GHSA-xr7r-f8xq-vfvv>
    
- [R 3] <https://access.redhat.com/security/cve/cve-2024-21626>
     
- [R 4] <https://www.egi.eu/service/cloud-container-compute/>

- [R 5] <https://www.scientificlinux.org/category/sl-errata/>

- [R 6] <https://lists.centos.org/pipermail/centos-announce/>

- [R 7] <https://security-tracker.debian.org/tracker/CVE-2024-21626> 
    
- [R 8] <https://ubuntu.com/security/CVE-2024-21626>

- [R 9] <https://errata.build.resf.org/ >  (RockyLinux)

- [R 10]  <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99]  https://confluence.egi.eu/display/EGIBG/SVG+Advisories

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec


