---
title: SVG:Advisory-SVG-2014-7628
permalink: /SVG:Advisory-SVG-2014-7628/
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-7628]

Title:   EGI SVG Advisory 'Moderate' RISK - Torque CVE-2014-3684 resolved in
         Torque version in the EGI AppDB part of the UMD [EGI-SVG-2014-7628]

Date:    2015-02-11
Updated:

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-7628

Introduction
============

A vulnerability has been announced publicly in Torque, CVE-2014-3684 [R 1], [R
2].

The patch for this has been applied to the version of Torque available in the
EGI AppDB part of the UMD.  [R 3]


Details
=======

For details see [R 1], [R 2]


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team.


Affected software
=================

Torque.

In the AppDB (for RedHat) this is fixed in version 2.5.13-1cri-9nik In this
case the patch for this specific vulnerability has been applied to an older
version of Torque.

For Debian this has been fixed by the software providers in version
2.4.16+dfsg-1+deb7u4., and they have produced their advisory [R 4]

For other software providers, see links in [R 1] and [R 2].


Mitigation
==========

N/A


Component installation information
==================================

A version of Torque is provided in the AppDB area of the UMD solves all
currently known problems.

https://appdb.egi.eu/store/software/software.vulnerability.group/releases/torque/

This is available for el5, el6 and its derivatives, and should be suitable for
most sites.

Limited support on a best efforts basis is provided by the EGI SVG, and support
is not guaranteed in the future.



Recommendations
===============

Sites are recommended to update relevant components.

Credit
======

SVG alerted to Vulnerability announcement by David Crooks from Glasgow

Patch incorporated into the SVG Fixes area of the EGI AppDB by Mischa Salle
from Nikhef.

References
==========

[R 1] http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2014-3684

[R 2] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-3684

[R 3]https://appdb.egi.eu/store/software/software.vulnerability.group/releases/torque/2.5.13-1cri-9nik/

[R 4] http://www.debian.org/security/2014/dsa-3058


Timeline
========

Yyyy-mm-dd

2014-11-03 SVG alerted to Vulnerability announcement by David Crooks from
           Glasgow
2014-11-03 Acknowledgement from the EGI SVG to the reporter
2014-11-20 Assessment agreed at SVG meeting.
2015-02-09 Updates added to AppDB version
2015-02-11 Public disclosure
```
