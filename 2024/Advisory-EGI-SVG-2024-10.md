---
title: Advisory-EGI-SVG-2024-10
permalink: /Advisory-EGI-SVG-2024-10
redirect_from:
  - /Advisory-SVG-CVE-2024-2961
---

## Advisory-EGI-SVG-2024-10

# HIGH risk glibc vulnerability 

Date:        2024-05-03
Updated:     2024-06-04

A HIGH risk vulnerability has been found concerning glibc where an 
out-of-bounds write flaw in the ISO-2022-CN-EXT plugin for glibc's 
iconv library may allow remote code execution. [R 1] 

## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2024-10
    
CVE ID     : CVE-2024-2961

CVSS Score : 8.8 [R 1]

## AFFECTED SOFTWARE AND VERSIONS

The affected version is several years old, version 2.28 [R 2]
But this version is included with the common Linux versions

**UPDATE 2024-06-03**

This has been fixed for many Linux versions including RHEL [R 1]

## ACTIONS REQUIRED/RECOMMENDED

Sites are recommended to update if a fixed version is available
for the Linux version they deploy.

Until then sites are recommended to carry out the mitigation below.


## MITIGATION

The mitigation would be to disable this encoding:


Check if your OS is running a vulnerable version:

```
# rpm -qa| grep glib
glibc-2.28-246.el8.x86_64
or
# ldd --version
ldd (GNU libc) 2.28
```

Check if  the vulnerable encoding is enabled:
```
#  echo "iconv -l | grep -E ‘CN-?EXT’" | iconv -t ASCII//TRANSLIT//IGNORE
ISO-2022-CN-EXT//
ISO2022CNEXT//
```
To disable it:

```
# cd /usr/lib64/gconv/gconv-modules.d
Comment it out from gconv-modules-extra.conf:
  #       from                    to                      module          cost
  #alias  ISO2022CNEXT//          ISO-2022-CN-EXT//
  #module ISO-2022-CN-EXT//       INTERNAL                ISO-2022-CN-EXT 1
  #module INTERNAL                ISO-2022-CN-EXT//       ISO-2022-CN-EXT 1
```
or 
```
# cat gconv-modules-extra.conf | grep -v -E 'CN-?EXT' > gconv-modules-extra-patched.conf
# rm gconv-modules-extra.conf
```
Delete the cache and regenerate it as follows:
```
# rm gconv-modules.cache
# iconvconfig
```
The location of the configuration file depends on the OS, you can find it by:
```
# find /usr -name gconv
```

    
## STATUS OF THIS ADVISORY
                          
_TLP:CLEAR information - Unlimited distribution_ 

 https://advisories.egi.eu/Advisory-EGI-SVG-2024-10

 https://advisories.egi.eu/Advisory-SVG-CVE-2024-2961 


Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG


-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------

    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://access.redhat.com/security/cve/CVE-2024-2961>

- [R 2] <https://sourceware.org/glibc/>
    
- [R 3] <https://nvd.nist.gov/vuln/detail/CVE-2024-2961> 

- [R 4] <http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2024-2961>
     
- [R 5] <https://www.cve.org/CVERecord?id=CVE-2024-2961>

- [R 6] <https://www.scientificlinux.org/category/sl-errata/>

- [R 7] <https://lists.centos.org/pipermail/centos-announce/>

- [R 8] <https://security-tracker.debian.org/tracker/CVE-2024-2961> 
    
- [R 9] <https://ubuntu.com/security/CVE-2024-2961>

- [R 10] <https://errata.build.resf.org/>   (RockyLinux)

- [R 11] <https://errata.almalinux.org/>  (AlmaLinux)


- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to this vulnerability by Barbara Krasovec

