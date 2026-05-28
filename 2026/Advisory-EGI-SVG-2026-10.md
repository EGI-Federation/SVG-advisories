---
title: Advisory-EGI-SVG-2026-10
permalink: /Advisory-EGI-SVG-2026-10

---

## Advisory-EGI-SVG-2026-10

# HIGH risk GPUBreach vulnerability

Date:        2026-04-15  
Updated:     2026-05-28

Specially crafted GPU workloads can induce bit flips in GDDR6 memory.

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-10
    
CVE ID     : N/A

CVSS Score : N/A
    
## IMPACTED VERSIONS:
    
GPUs using GDDR6 memory (demonstrated on NVIDIA RTX A6000; 
other GDDR6 GPUs may also be susceptible). 
       

## ACTIONS REQUIRED/RECOMMENDED

Sites running GPUs with GDDR6 memory should be aware of this, 
and consider taking action if appropriate.

If anyone becomes aware of any situation where this vulnerability has a 
significant impact on the EGI infrastructure, then please inform EGI SVG.


## MITIGATION

Avoid multi-tenant GPU sharing to reduce the likelihood of exploitation. 
Keep GPU drivers up to date to mitigate potential escalation paths. 
Enable ECC on GPUs (if supported) to reduce the probability of successful bit flips. 
Limit and monitor GPU access where feasible. 
Monitor vendor advisories for updates, as patch availability is not yet confirmed.


## MORE INFORMATION

This vulnerability affects GPUs (NVIDIA, AMD, Intel) using GDDR6 memory 
for which there is currently no patch.

Most of the HPC-related GPUs are not affected (such as A100, H100, B200)  
because they have HBM2 or HBM3 memory.

The problematic ones are RTX-series graphics cards, particularly the
RTX 6000 Pro, which is currently in widespread use, as well as models
such as the L40S, which are commonly used for AI workloads. These
devices have GDDR6 memory.

Recent research (GPUBreach) demonstrates that specially crafted GPU workloads 
can induce bit flips in GDDR6 memory, potentially corrupting GPU page tables.
Under certain conditions, this could be chained with GPU driver vulnerabilities 
to achieve host-level (root) compromise. 

This may allow:

Unauthorized GPU memory access, including possible cross-process data exposure. 
In combination with GPU driver vulnerabilities, potential escalation to root access 
on the host system. In a demonstrated scenario, researchers achieved root shell access, 
resulting in full system compromise.


## STATUS OF THIS ADVISORY
    
                
_TLP:CLEAR information - Unimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-10  

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
------
    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES
        
- [R 1] <https://gpubreach.ca/> 
    
- [R 2] <https://www.nvidia.com/en-us/security/>
    
- [R 3] <https://radar.offseq.com/threat/gpubreach-root-shell-access-achieved-via-gpu-rowha-1215a777>
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by the OSG security team 


