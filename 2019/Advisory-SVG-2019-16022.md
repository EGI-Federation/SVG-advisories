---
title: SVG:Advisory-SVG-2019-16022
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE ] LOW risk vulnerability in dCache
         xrootd protocol implementation [EGI-SVG-2019-16022]

Date:    2019-11-11
Updated: 2019-12-09 Fixed version in EGI UMD 4.9.1


Affected software and risk
==========================

LOW risk vulnerability concerning dCache

Package : dCache

A vulnerability in dCache Xrootd protocol implementation has been found which
allows authenticated users to list directories outside of a restricted set
configured by the service administrator. Accessing such directories or their
contents is still constrained by their actual permissions: only the restriction
to certain paths is not applied.

Actions required/recommended
============================

Sites are recommended to update relevant components as soon as it is
convenient.

**UPDATE 2019-12-09**

Sites may update from the dCache site [R 1] or from the EGI UMD.


Component installation information
==================================

Updates are available at from the dCache site [R 1]

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

**UPDATE 2019-12-09**

dCache 5.2.10 is available in EGI UMD release 4.9.1 which does not contain this
vulnerability.

http://repository.egi.eu/2019/12/04/release-umd-4-9-1/

Affected software details
=========================

Fixed versions are:--

6.0.1
5.2.7
5.1.12
5.0.23
4.2.44

Earlier versions supported versions - 4.2, 5.0, 5.1, 5.2, 6.0 are all
vulnerable.

TLP and URL
===========

** WHITE information - Unlimited distribution
  - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **
URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2019-16022

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

This vulnerability was reported by Tigran Mkrtchyan from the dCache team.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2019-16022]

2019-10-29 Vulnerability reported by Tigran Mkrtchyan
2019-10-29 Acknowledgement from the EGI SVG to the reporter
2019-10-31 EGI SVG Risk Assessment completed
2019-10-31 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2019-11-05 Updated packages available on the dCache site
2019-11-11 Advisory sent to sites
2019-12-09 Version of dCache with this vulnerability fixed available in the EGI
           UMD - advisory updated.

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 2]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
