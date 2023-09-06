---
title: Test-New-Template-v2
permalink: /Test-New-Template-v2
---

## 'ADVISORY' [TLP:CLEAR] HIGH risk Linux kernel vulnerability [EGI-SVG-2023-33]

Date: 2023-05-17

A HIGH risk Use-after-free flaw was found in the Linux kernel’s TLS protocol, affecting
RHEL8 and RHEL9 and their derivatives.

## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2023-33

CVE ID : CVE-2023-0461

CVSS Score : 7.8 [R 1]

## ACTIONS REQUIRED/RECOMMENDED

Affected sites are recommended to update relevant components as soon as possible.

Sites should update the relevant components using the RedHat or other vendor updates, see
references below.

## MORE INFORMATION

A use-after-free flaw was found in the Linux kernel’s TLS protocol functionality in how a
user installs a TLS context (struct tls_context) on a connected TCP socket. This flaw
allows a local user to crash or potentially escalate their privileges on the system [R 1].
For RHEL this only affects RHEL8 and RHEL9 and their derivatives, 7 and its
derivatives are not affected.

The vulnerability can be exploited only by a local user. Hence sites should update their
affected Grid Worker Nodes, User Interfaces and other shared user systems as the risk may
be higher than suggested by the CVSS score.

Note that Scientific Linux is based on RHEL7 therefore is not affected.

## STATUS OF THIS ADVISORY

**TLP:CLEAR information - Unlimited distribution**

- <https://advisories.egi.eu/Advisory-EGI-SVG-2023-33>
- <https://advisories.egi.eu/Advisory-EGI-SVG-CVE-2023-0461>

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG

Comments or questions should be sent to `svg-rat at mailman.egi.eu`

Vulnerabilities relevant for EGI can be reported at `report-vulnerability at egi.eu`

(see [R 99] for further details, and other information on SVG)

## REFERENCES

- [R 1] <https://access.redhat.com/security/cve/CVE-2023-0461>
- [R 2] <https://lists.centos.org/pipermail/centos-announce/>
- [R 3] <https://security-tracker.debian.org/tracker/CVE-2023-0461>
- [R 4] <https://ubuntu.com/security/CVE-2023-0461>
- [R 5] RockyLinux <https://errata.build.resf.org/>
- [R 6] AlmaLinux <https://errata.almalinux.org/>
- [R 99] [Information on SVG](https://confluence.egi.eu/display/EGISVG/SVG+Advisories)

## CREDITS

SVG was alerted to this vulnerability by Mischa Salle
