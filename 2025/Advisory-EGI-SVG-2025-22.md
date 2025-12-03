---
title: Advisory-EGI-SVG-2025-22
permalink: /Advisory-EGI-SVG-2025-22
  
redirect_from:
  - /Advisory-SVG-CVE-2025-23280 
  - /Advisory-SVG-CVE-2025-23330
---
## Advisory-EGI-SVG-2025-22

# CRITICAL risk NVIDIA use-after-free vulnerabilities

Date:        2025-10-16  
Updated:     2025-12-03

CRITICAL risk vulnerabilities concerning NVIDIA including use-after-free 
allowing privilege escalation and/or code execution. [R 1]
There is a public exploit available.


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2025-22
    
CVE ID     : CVE-2025-23280, CVE-2025-23330

CVSS Score : 7.0 [R 3]
    
## ACTIONS REQUIRED/RECOMMENDED

Sites running the affected NVIDIA drivers are required to install 
a fixed version urgently, see [R 1].

All running resources MUST be either patched or have mitigation
in place or software removed by 2025-10-24  00:00 UTC 

Sites failing to act or respond to requests from the EGI CSIRT team 
risk site suspension. See [R 98]
    

## MITIGATION

As far as we are aware, no mitigation is available.
Drivers need to be updated.

## MORE INFORMATION
     
NVIDIA Display Driver for Linux contains a vulnerability where an attacker 
could cause a use-after-free. A successful exploit of this vulnerability 
might lead to code execution, escalation of privileges, data tampering, 
denial of service, and information disclosure. [R 4]

NOTE: the driver may be installed even when no display is connected.
       
Given a public exploit is available and due to the way the EGI infrastucture
operates, the EGI SVG considers this vulnerability to be 'CRITICAL' risk.
      
    
## STATUS OF THIS ADVISORY
                         
_TLP:CLEAR information - Unlimited distribution_ 

This advisory will be made public on or after 2025-11-14  at  
    
https://advisories.egi.eu/Advisory-EGI-SVG-2025-22 

https://advisories.egi.eu/Advisory-SVG-CVE-2025-23280  
https://advisories.egi.eu/Advisory-SVG-CVE-2025-23330

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
---
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvidia.custhelp.com/app/answers/detail/a_id/5703/~/security-bulletin%3A-nvidia-gpu-display-drivers---october-2025>
       
- [R 2] <https://blog.quarkslab.com/nvidia_gpu_kernel_vmalloc_exploit.html>
       
- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2025-23280> 
     
- [R 4] <https://www.cve.org/CVERecord?id=CVE-2025-23280>

    
    
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 
    
 
