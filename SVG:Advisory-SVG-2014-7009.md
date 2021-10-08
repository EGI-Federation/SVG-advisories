---
title: SVG:Advisory-SVG-2014-7009
permalink: /SVG:Advisory-SVG-2014-7009/
---

```


** WHITE information - Unlimited distribution allowed                       **

** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-7009]

Title:       EGI SVG Advisory 'Moderate' RISK Remote access to dCache
              configuration information  [SVG EGI-SVG-2014-7009]

Date:        2014-08-05

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-7009

Introduction
============

A vulnerability has been found in dCache [R 1] by the dCache team which allows remote
access to the dCache configuration information.

This has been resolved both in versions of dcache available on the dcache site and
in the EGI UMD repository.


Details
=======

This vulnerability is confirmed to exist in the software and be exploitable in principle
by anyone with no credentials.  It was found that sites in EGI were
all configured in ways which made it not possible to actually exploit this vulnerability.
The vulnerability should not be in the software, hence it has been fixed in the UMD.


Risk category
=============

This issue has been assessed as 'Moderate'  risk by the EGI SVG Risk Assessment Team.


Affected software
=================

dCache

Affected versions of dCache are:
================================

v2.6.0 through to v2.6.26 (inclusive),
v2.7.0 through to v2.7.8 (inclusive),
v2.8.0 through to v2.8.5 (inclusive),
v2.9.0 through to v2.9.1 (inclusive).

Unaffected (fixed) versions of dCache are
---------------------------------

v2.2.0 and later v2.2 releases,
v2.6.27 and later v2.6 releases,
v2.7.9 and later v2.7 releases,
v2.8.6 and later v2.8 releases,
v2.9.2 and later v2.9 releases.
all subsequent feature releases.

Note that v2.6.28 in UMD-3.8.0 is the latest version in the EGI UMD and this has
the vulnerability resolved.


Mitigation
==========

No sites were found to be configured in a vulnerable manner, so we do not include
mitigation information.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites is
repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Not vulnerable version of dcache in UMD-3.8.0

http://repository.egi.eu/2014/07/24/release-umd-3-8-0/


Sites installing from EMI should see using

http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/

A fixed version is in EMI 3 update 17.


Sites may also install directly from the dCache site. [R 1]



Recommendations
===============

Sites are recommended to update relevant components in due course.


Credit
======

SVG was alerted to this vulnerability by Patrick Fuhrmann from dCache


References
==========

[R 1] http://www.dcache.org/index.shtml

Timeline
========
Yyyy-mm-dd

2014-05-14 Vulnerability reported by Patrick Fuhrmann
2014-05-14 Acknowledgement from the EGI SVG to the reporter
2014-05-14 Fixed version of the software available on the dCache site
2014-05-16 Confirmed that due to the manner in which sites in EGI are configured
           no sites are currently known to be vulnerable.
2014-05-16 Assessment by the EGI Software Vulnerability Group reported to the software
           providers
2014-07-24 Updated packages available in the EGI UMD.
2014-08-05 Public disclosure
```