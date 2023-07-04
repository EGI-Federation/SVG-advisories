---
title: Advisory-EGI-SVG-2023-20
permalink: /Advisory-EGI-SVG-2023-20
---

## Advisory-EGI-SVG-2023-20

```
Title:       EGI SVG 'ADVISORY' [TLP:WHITE] MODERATE risk Indigo IAM XSS
             vulnerability [EGI-SVG-2023-20]

Date:        2023-07-04

Affected software and risk
==========================

[EGI-SVG-2023-20] MODERATE risk vulnerability concerning INDIGO-IAM

A Cross-site scripting (XSS) vulnerability has been found in INDIGO-IAM.


Actions required/recommended
============================

Sites running INDIGO-IAM are recommended to update in due course.


Component installation information
==================================

See [R 2]

Affected software details
=========================

All the past versions are vulnerable, i.e. <= 1.8.2.

* 1.8.1p1 fixes 1.8.1 (for this vulnerability)
* 1.8.2p1 fixes 1.8.2 (for this vulnerability)

Most deployments are still at 1.8.1, because the latest release introduces a small
backwards incompatibility that requires some additional work for IAM clients.
For this reason, *two* releases have been made.


More information
================

INDIGO-IAM is a centrally-managed service that covers functionality similar
to VOMS, in a world based on OAuth/OpenID Connect. It is meant to replace VOMS
in the not-too-distant future.
There is one instance of IAM per VO and there are already several deployments
in WLCG(e.g. for the four LHC experiments), but also in other contexts.
It is also one of the AAI solutions for the EOSC.
More information on the product is available at [R 1] [R 2]


TLP and URL
===========

** WHITE information - Unlimited distribution -
see https://confluence.egi.eu/display/EGIG/Traffic+Light+Protocol for distribution restrictions**

URL: https://advisories.egi.eu/Advisory-EGI-SVG-2023-20

Minor updates may be made without re-distribution to the sites.


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 99].

References
==========

[R 1] https://github.com/indigo-iam/iam

[R 2] https://indigo-iam.github.io/

[R 99] https://documents.egi.eu/public/ShowDocument?docid=3867

Credit
======

This vulnerability was reported by Chris Lee, and David Crooks informed the EGI SVG

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2023-20]

2023-03-14 Vulnerability reported by Chris Lee
2023-03-14 Acknowledgement from the EGI SVG to the reporter
2023-03-17 EGI SVG Risk Assessment completed
2023-07-03 Updated docker images available on Docker Hub
2023-07-04 Advisory sent to sites and placed on advisories.egi.eu

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's purpose
"To minimize the risk to the EGI infrastructure arising from software vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 99]  in the context of how the software is used in the EGI infrastructure.
It is the opinion of the group, we do not guarantee it to be correct. The risk may also
 be higher or lower in other deployments depending on how the software is used.

-----------------------------
This advisory is subject to the Creative commons licence
https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/
Software Vulnerability Group must be credited.
-----------------------------

Note that the SVG issue handling procedure has recently been modified, to take
account of the increasing inhomogeneity of the EGI infrastructure and speed up
the procedure for publicly announced vulnerabilities.
Changes are in the process of being implemented.
```

On behalf of the EGI SVG,
