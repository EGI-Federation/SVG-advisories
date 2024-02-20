---
title: Advisory-EGI-SVG-2023-59
permalink: /Advisory-EGI-SVG-2023-59
redirect_from:
  - /Advisory-SVG-CVE-2023-39933
  - /Advisory-SVG-CVE-2023-39934
  - /Advisory-SVG-CVE-2023-39935
  - /Advisory-SVG-CVE-2023-39936
  - /Advisory-SVG-CVE-2023-39937
  - /Advisory-SVG-CVE-2023-39938
  
published: false
---

## Advisory-EGI-SVG-2023-59

# CRITICAL risk Multiple SLURM Vulnerabilities 

Date:        2023-12-14
Updated:     2024-02-20

Multiple CRITICAL risk vulnerabilities concerning SLURM 

## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2023-59
    
CVE ID's:--   
    
CVE-2023-49933: Slurm Protocol Message Extension
CVE-2023-49934: SQL injection in SLURM DBD database    
CVE-2023-49935: Slurmd Message Integrity Bypass
CVE-2023-49936: Slurm NULL Pointer Dereference
CVE-2023-49937: Slurm Protocol Double Free
CVE-2023-49938: Slurm Arbitrary File Overwrite

CVSS Score : (not available at time of writing)
    

## ACTIONS REQUIRED/RECOMMENDED
 
Sites running SLURM are required to urgently install a new version.
    
See [R 1] below

All running resources MUST be patched by 2023-12-21  00:00 UTC 

Sites failing to act and/or failing to respond to requests from the 
EGI CSIRT team risk site suspension. 

## MORE INFORMATION

Commercial users have already been informed and patches provided, 
prior to public announcement. 
    
Details of the vulnerabilities are available at the SLURM site [R 1]     
    
## STATUS OF THIS ADVISORY   
                        
_TLP:CLEAR information - Limited distribution_ 

                      
https://advisories.egi.eu/Advisory-EGI-SVG-2023-59  

https://advisories.egi.eu/Advisory-SVG-CVE-2023-39933
https://advisories.egi.eu/Advisory-SVG-CVE-2023-39934
https://advisories.egi.eu/Advisory-SVG-CVE-2023-39935
https://advisories.egi.eu/Advisory-SVG-CVE-2023-39936
https://advisories.egi.eu/Advisory-SVG-CVE-2023-39937
https://advisories.egi.eu/Advisory-SVG-CVE-2023-39938 

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1]  <https://www.schedmd.com/news.php?>
    
- [R 2]  <https://www.schedmd.com/downloads.php>

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec


