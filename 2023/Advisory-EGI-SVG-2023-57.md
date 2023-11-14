---
title: Advisory-EGI-SVG-2023-57
permalink: /Advisory-EGI-SVG-2023-57
redirect_from:
  - /Advisory-SVG-CVE-2023-41914
  
published: false
---

## Advisory-EGI-SVG-2023-57

# 'ADVISORY' [TLP:CLEAR] HIGH risk Slurm race condition vulnerability

HIGH risk race condition vulnerabilities concerning Slurm were found which  may 
result in the user taking ownership of an arbitrary file on the system. 
This has been fixed in Slurm versions 23.02.6 and 22.05.10 [R 1]


## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2023-57
    
CVE ID     : CVE-2023-41914

CVSS Score : N/A
    
## ACTIONS REQUIRED/RECOMMENDED

Sites running Slurm are recommended to update as soon as possible, see [R 1] below.

Sites should be aware that if a working public exploit is released this vulnerability 
is likely to be elevated to 'Critical' and sites will then be required to patch or 
have mitigation in place within 7 days or risk suspension. 

## MORE INFORMATION

More information is available from the SLURM site [R 2]
    
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 

 This advisory will be made public on or after 2023-11-13 at 
 
 <https://advisories.egi.eu/Advisory-EGI-SVG-2023-57>

 <https://advisories.egi.eu/Advisory-EGI-SVG-41914>

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1]  <https://www.schedmd.com/downloads.php> 

- [R 2]  <https://www.schedmd.com/news.php?id=280#OPT_280>


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec.
