---
title: Advisory-EGI-SVG-2026-21
permalink: /Advisory-EGI-SVG-2026-21
redirect_from:
  - /Advisory-SVG-CVE-2026-46243
  
---

## Advisory-EGI-SVG-2026-21

# CRITICAL risk - local privilege escalation via cifs 

Updated:     2026-07-21

Updated:     2026-06-09
- RHEL fixes available [R 3]
- Rocky Linux patches available [R 5]

Updated:     2026-06-03
- AlmaLinux fixes available [R 2]
- Debian patches available [R 4]

Date:        2026-05-28   


CRITICAL risk vulnerability concerning Linux kernel/cifs-utils 
local root exploit via forged cifs.spnego upcall. [R 1]


## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2026-21
    
CVE ID     : CVE-2026-46243

CVSS Score : 7.8


## ACTIONS REQUIRED/RECOMMENDED

Sites should ensure that the cifs-utils package is removed and/or other
mitigating action (see the "MITIGATION" section below) is in place on
hosts that can be accessed by unprivileged users, e.g. grid worker nodes.

All running resources MUST have mitigation in place or software removed
by 2026-06-05 00:00 UTC.

Sites failing to act or respond to requests from the EGI CSIRT team
risk site suspension. [R 98]


## MITIGATION

See [R 1], under "Immediate-term mitigations", possibilities are:

- deinstall the `cifs-utils` package

- blacklist the `cifs` kernel module:
  ```
  cat > /etc/modprobe.d/blacklist-cifs.conf << EOF
  blacklist cifs 
  install cifs /bin/false
  EOF
  ```
  And make sure it's unloaded:
  ```
  modprobe -r cifs
  ```
  If the latter command fails to unload the module because it is
  in use by something, the host would need to be rebooted.

- Deleting/overriding the default `cifs.spnego` request-key rule
  (if Kerberos cifs is not required), e.g., after adjusting for
  your keyctl path (can be /usr/bin/keyctl instead):
  ```
  cat > /etc/request-key.d/cifs.spnego.conf << EOF
  create cifs.spnego * * /usr/sbin/keyctl negate %k 30 %S
  EOF
  ```

- Disable user namespaces. Note that these are typically required
  for grid jobs relying on apptainer, although apptainer can still
  be configured to be used a set-uid binary instead. That would need
  coordination with the affected VOs.


## STATUS OF THIS ADVISORY
                        
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2026-21  

 https:///advisories.egi.eu/Advisory-SVG-CVE-2026-46243

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG
-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------

See [R 99]
    
## REFERENCES 

- [R 1] <https://www.openwall.com/lists/oss-security/2026/05/28/2>
- [R 2] <https://almalinux.org/blog/2026-05-28-cifswitch/>
- [R 3] <https://access.redhat.com/security/cve/cve-2026-46243>
- [R 4] <https://security-tracker.debian.org/tracker/CVE-2026-46243>
- [R 5] <https://forums.rockylinux.org/t/is-cve-2026-46243-fixed-in-rockylinux-9-7/20569/14>
   
- [R 98] <https://confluence.egi.eu/display/EGIBG/CSIRT+monitoring+for+exposure+to+%27CRITICAL%27+vulnerabilities>  

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>


## CREDITS

SVG was alerted to this vulnerability by Jakub Havrila 
