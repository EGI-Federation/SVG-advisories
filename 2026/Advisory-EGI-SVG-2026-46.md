---
title: Advisory-EGI-SVG-2026-46
permalink: /Advisory-EGI-SVG-2026-46

redirect_from:
  - /Advisory-SVG-CVE-2026-47489

---

## Advisory-EGI-SVG-2026-46

# Title

Updated:  2026-11-03
    
Date:      2026-10-01
   

## DESCRIPTION 

Multiple HIGH risk vulnerabilities concerning NVIDIA Linux GPU Driver 
some of which may lead to privilege escalation. 

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-46
    
CVE ID     : CVE-2026-47489 and others

CVSS Score : 7.8 [R 1]
    

- EGI SVG: HIGH   
    

## ACTIONS REQUIRED/RECOMMENDED

Please apply updates detailed in [R 1] on affected hosts as soon as possible.

## MORE INFORMATION

(Based on OSG's notification)

NVIDIA has released a security update addressing multiple vulnerabilities  
in the NVIDIA Linux GPU driver and related kernel-mode components [R 1].  
Several of these vulnerabilities can be triggered by an unprivileged local  
user and may result in code execution, privilege escalation, information  
disclosure, data tampering, or denial of service.

These vulnerabilities are relevant to sites operating shared NVIDIA GPU  
worker nodes. Applicability depends on the NVIDIA driver branch and version   
installed on the worker node.

GPU compute jobs do not require an X11 or Wayland display server; however,  
GPU-enabled jobs may interact with the host NVIDIA kernel driver through  
NVIDIA GPU device interfaces.

    
## STATUS OF THIS ADVISORY
   
                        
_TLP:CLEAR information - Unlimited distribution_ 
 
https://advisories.egi.eu/Advisory-EGI-SVG-2026-46 

https://advisories.egi.eu/Advisory-SVG-CVE-2026-47489

 
## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://nvidia.custhelp.com/app/answers/detail/a_id/5861> 

- [R 2] <https://docs.nvidia.com/deploy/nvidia-smi/index.html> 

- [R 3] <https://github.com/NVIDIA/product-security/blob/main/2026/5861/5861.md>
 this is an [R 1] alternative as some could not access [R 1]
  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by OSG (the Open Science Grid) 


