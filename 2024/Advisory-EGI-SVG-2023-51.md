---
title: Advisory-EGI-SVG-2023-51
permalink: /Advisory-EGI-SVG-2023-51
redirect_from:
  - /Advisory-SVG-CVE-2023-41915
  
published: false
---

## Advisory-EGI-SVG-2023-51

# CRITICAL risk PMIX race condition vulnerability

CRITICAL risk vulnerability concerning PMIx, which may permit a malicious 
user to obtain ownership of an arbitrary file and could thus result in  
privilege escallation to root. [R 1] This is a critical issue for all 
sites that are using Slurm built with PMIx support.

## IDs AND CVSS SCORE 

EGI SVG ID : EGI-SVG-2023-51
    
CVE ID     : CVE-2023-41915

CVSS Score : 8.1 (NVD) [R 2] / 9.8 (RHEL) [R 3]
    
## ACTIONS REQUIRED/RECOMMENDED

First check if Slurm was built with PMIx support by running:
```
$ srun --mpi=list
```
Typical output will be something like
```
MPI plugin types are...
	cray_shasta
	none
	pmi2
	pmix
specific pmix plugin versions available: pmix_v3,pmix_v4 ```

This gives you information about whether slurm is built with PMIx
support and if so which version of PMIx.

If the command returns no pmix option, your Slurm installation is safe. 
Otherwise, upgrade PMIx to the fixed releases v4.2.6 or v5.0.1 [R 1]. 
Note that there is at least one ABI-breaking change between
versions 4.2.3 and 4.2.6, which means that upgrading to 4.2.6
requires Slurm packages to be rebuilt.

If Slurm upgrade isn't an option, you can disable PMIx support by
removing the mpi_pmix*.so libraries on the compute nodes and
adjusting the MpiDefault setting in your Slurm configuration.

You can also patch your current PMIx version by replacing the chown
function  with lchown in the source and rebuilding the PMIx rpm [R 4].
After installing the patched PMIx, this command shouldn't return
any result:

```objdump -t /usr/lib64/libpmi*.so* | grep chown```

After the installation, slurmd on the compute nodes needs to be restarted.

Note that *all* versions prior to PMIx 4.2.6 are vulnerable, but some
older PMIx versions are no longer supported and will not be patched.

Sites should be aware that this is a 'Critical' vulnerability, so it
needs to be patched or mitigated within 7 days or site risks suspension. 

If anyone becomes aware of any other situation where this vulnerability
has significant impact on the EGI infrastructure then please inform EGI SVG.
 

## MORE INFORMATION

A filesystem race condition could permit a malicious user to obtain 
ownership of an arbitrary file on the filesystem when parts of the PMIx 
library are called by a process running as uid 0. This may happen under the
default configuration of certain workload managers, including Slurm. [R 1]

Given that for EGI including in the Grid Worker Nodes many users can access
the service if a site is vulnerable the risk may be higher than suggested
by the CVSS score.
 
## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 
                        
 https://advisories.egi.eu/Advisory-EGI-SVG-2023-51 

 https://advisories.egi.eu/Advisory-EGI-SVG-CVE-2023-41915 

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)   
    
## REFERENCES

- [R 1] <https://github.com/openpmix/openpmix/releases/tag/v4.2.6>

- [R 2] <https://nvd.nist.gov/vuln/detail/CVE-2023-41915>

- [R 3] <https://access.redhat.com/security/cve/CVE-2023-41915>

- [R 4] <https://github.com/openpmix/openpmix/pull/3150>
    

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec 

