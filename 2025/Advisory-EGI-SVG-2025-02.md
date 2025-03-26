---
title: Advisory-EGI-SVG-2025-02
permalink: /Advisory-EGI-SVG-2025-02
redirect_from:
  - /Advisory-SVG-CVE-2024-0135
  - /Advisory-SVG-CVE-2024-0136
  - /Advisory-SVG-CVE-2024-0137
  - /Advisory-SVG-CVE-2025-23359
---

# ‘ADVISORY’ [TLP:AMBER] CRITICAL risk Vulnerabilities in nvidia-container-toolkit, nvidia-gpu-operator [EGI-SVG-2025-02]

Date:        2025-02-26

CRITICAL risk vulnerabilities concerning nvidia-toolkit <=v1.17.4 and nvidia-gpu-operator <=24.9.2


## IDs AND CVSS SCORE

EGI SVG ID : EGI-SVG-2025-02

CVE ID     : CVE-2024-0135, CVE-2024-0136, CVE-2024-0137, CVE-2025-23359

CVSS Score : Up to 8.3 [R 1]/[R 2]

## AFFECTED SOFTWARE AND VERSIONS

Affected versions vary depending on CVE, but **all vulnerabilities in this advisory are patched in the following versions**:
- nvidia-container-toolkit v1.17.4
- nvidia-gpu-operator 24.9.2.

The breakdown of affected versions based on CVE is as follows [R 1]/[R 2]:

For CVE‑2024-0135, CVE‑2024-0136, CVE‑2024-0137:
- NVIDIA Container Toolkit
    - Affected versions: <=v1.17.2
    - Updated version: v1.17.3
- NVIDIA GPU Operator:
    - Affected versions: <=24.9.0
    - Updated version: 24.9.1

For CVE‑2025-23359:
- NVIDIA Container Toolkit
    - Affected versions: <=v1.17.3
    - Updated version: v1.17.4
- NVIDIA GPU Operator
    - Affected versions: <=24.9.1
    - Updated version: 24.9.2

## ACTIONS REQUIRED/RECOMMENDED

Sites running nvidia-toolkit and nvidia-gpu-operator are required to urgently install new version v1.17.4 and 24.9.2 respectively.

All running resources MUST be either patched or have mitigation
in place or software removed by 2025-03-06 00:00 UTC

Sites failing to act and/or failing to respond to requests from the EGI CSIRT team risk site suspension.

## MITIGATION

Mitigations for these CVEs have been published by NVIDIA on the relevant security bulletin, refer to these for instructions [R 1]/[R 2].

## MORE INFORMATION

EGI SVG has elevated the risk level of CVE-2025-23359 from HIGH to CRITICAL due to the potential for container escape and the potential impact this has on EGI infrastructure.

CVE-2025-23359 is a bypass of the fix for CVE-2024-0132 (see [R 7]) for which we sent Advisory-EGI-SVG-2024-22: https://advisories.egi.eu/Advisory-EGI-2024-22

## STATUS OF THIS ADVISORY

_TLP:AMBER information - Limited distribution_

This advisory will be made public on or after 2025-03-26  at

https://advisories.egi.eu/Advisory-EGI-SVG-2025-02

https://advisories.egi.eu/Advisory-SVG-CVE-2024-0135

https://advisories.egi.eu/Advisory-SVG-CVE-2024-0136

https://advisories.egi.eu/Advisory-SVG-CVE-2024-0137

https://advisories.egi.eu/Advisory-SVG-CVE-2025-23359

Minor updates may be made without re-distribution to the sites.


## CONTACT AND OTHER INFORMATION ON SVG


-----------------------------
    Others may re-use this information provided they:-

    1) Respect the provided TLP classification

    2) Credit the EGI (https://www.egi.eu/) Software Vulnerability Group
-----------------------------



Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu

(see [R 99] for further details, and other information on SVG)


## REFERENCES

- [R 1] <https://nvidia.custhelp.com/app/answers/detail/a_id/5599> (NVIDIA Security Bulletin, January 2025)

- [R 2] <https://nvidia.custhelp.com/app/answers/detail/a_id/5616> (NVIDIA Security Bulletin, February 2025)

- [R 3] <https://www.cve.org/CVERecord?id=CVE-2025-23359>

- [R 4] <https://www.cve.org/CVERecord?id=CVE-2024-0135>

- [R 5] <https://www.cve.org/CVERecord?id=CVE-2024-0136>

- [R 6] <https://www.cve.org/CVERecord?id=CVE-2024-0137>

- [R 7] <https://www.wiz.io/blog/nvidia-ai-vulnerability-deep-dive-cve-2024-0132> (CVE-2024-0132 and CVE-2025-23359 description)

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>

## CREDITS

SVG was alerted to these vulnerabilities by Barbara Krašovec
