---
title: SVG:Advisory-SVG-2016-11033
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'High' Risk Arbitrary file overwrite
         vulnerability in WebAppDIRAC [EGI-SVG-2016-11033]

Date:    2016-05-25
Updated:


Affected Software and Risk
=======================

HIGH risk vulnerability concerning Arbitrary file overwrite in WebAppDIRAC

Package : WebApp DIRAC

Actions Required/Recommended
============================

Sites are recommended to update relevant components as soon as possible if they
have not already installed a non-vulnerable version.

Affected software Details.
=======================

Versions of DIRAC prior to v6r14p31 are affected.

More information
================

There is the possibility of unauthenticated remote code execution, but it is
probably hard for an attacker to find and it is not clear how many sites are
have a vulnerable configuration.

The file uploading feature on which this vulnerability is based was removed
from the DIRAC WebApp project starting from v6r14p31 version release.


Component installation information
==================================

See [R 1]

TLP and URL
===========

** WHITE information - Unlimited distribution                               **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2016-11033

Minor updates may be made without re-distribution to the sites

Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.

References
==========

[R 1] https://github.com/DIRACGrid/DIRAC/wiki

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-11033]

2016-05-06 Vulnerability reported by Simon Fayer who is a member of SVG.
2016-05-09 Software providers confirmed they are aware of this issue and
           already working on its resolution
2016-05-18 EGI SVG Risk Assessment completed - discussed at SVG meeting.
2016-05-19 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2016-05-19 Software providers stated that the issue has already been fixed in
           current production version, and gave version number
2016-05-25 Advisory/Alert sent to sites
2016-06-08 Advisory placed on the wiki
```
