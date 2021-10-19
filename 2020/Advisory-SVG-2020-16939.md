---
title: SVG:Advisory-SVG-2020-16939
---

```
Title:   EGI SVG 'ADVISORY' **UPDATE** [TLP:WHITE] CRITICAL risk Vulnerability
         concerning dCache [EGI-SVG-2020-16939]

Date:    2020-11-19
Updated: 2020-11-25, 2021-01-14


Affected software and risk
==========================

CRITICAL risk vulnerability concerning dCache

Package : dCache

A vulnerability has been reported in dCache concerning file ownership checks.
This may in some circumstances allow an unauthenticated person to change file
ownership, view and delete arbitrary files.

Actions required/recommended
============================

Sites running dCache should urgently update relevant components, or carry out
the mitigation described below.

All running resources MUST be either patched or have mitigation in place or
software removed by 2020-12-03 00:00 UTC

Sites failing to act and/or failing to respond to requests from the EGI CSIRT
team risk site suspension.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

**UPDATE 2020-11-25**

A fixed version of dCache is now available in the EGI UMD.

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

The fixed version of dCache is included in UMD-4.12.5

https://repository.egi.eu/2020/11/23/release-umd-4-12-5/

Sites installing directly from dCache should see [R 1].


Mitigation
==========

This 'CRITICAL' risk vulnerability affects only the dcap family of doors (dcap,
gsidcap, kerberised-dcap). dCache instances that do not run a dcap-family door
are not vulnerable to this problem.  Stopping all dcap doors provides a
mitigation against this vulnerability.

Sites should in general ensure, through local firewall settings, that plain
(i.e. unauthenticated) DCAP access to dCache is _only_ permitted (if needed)
from hosts whose users are authenticated and authorized by the site.


Affected software details
=========================

This has been fixed in dCache versions 6.2.10, 6.1.18, 6.0.29, 5.2.35.

Earlier versions may be vulnerable.


More information
================

The latest release of dCache actually fixes 2 completely separate
vulnerabilities.

One has been assessed as 'CRITICAL' risk, as it may allow an unauthenticated
person to change file ownership, view and delete arbitrary files.

The other merely allows a user in some circumstances to change the group
ownership of a file or directory they are authorized to change to one they are
not entitled to change it to. This has been assessed to be 'LOW' risk.


TLP and URL
===========

** AMBER information - Limited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

This advisory will be placed on the wiki on or after 2020-12-19

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2020-16939

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 2]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.


References
==========

[R 1] https://www.dcache.org/

[R 2] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was reported by Paul Millar from the dCache team


Timeline
========

Yyyy-mm-dd  [EGI-SVG-2020-16939]

2020-10-29 Vulnerability reported by Paul Millar
2020-10-30 Acknowledgement from the EGI SVG to the reporter
2020-11-10 EGI SVG Risk Assessment completed
2020-11-10 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2020-11-18 Updated versions produced by the dCache team
2020-11-19 Advisory sent to sites
2020-11-23 Fixed version of dCache in the EGI UMD
2020-11-25 Advisory updated
2021-01-14 Public disclosure - placed on the wiki


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 2]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.  The risk may also be higher or lower in other deployments depending
on how the software is used.


-----------------------------
Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group
------------------------------

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
