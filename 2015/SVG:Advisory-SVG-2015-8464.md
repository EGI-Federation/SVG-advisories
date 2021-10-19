---
title: SVG:Advisory-SVG-2015-8464
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2015-8464]

Title:   EGI SVG Advisory 'Low' RISK Buffer overflow vulnerability in XRootD
         client [EGI-SVG-2015-8464]

Date:    2015-05-13
Updated:

URL:     https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2015-8464

Introduction
============

A buffer overflow vulnerability has been found in the XRootD client.

This has been fixed.


Details
=======

A buffer overflow vulnerability has been found in the XRootD client.

If a client were to be directed to a malicious XRootD server it is possible
that a compromised could occur.  This seems unlikely hence the risk category.


Risk category
=============

This issue has been assessed as 'Low' risk by the EGI SVG  Risk Assessment Team


Affected software
=================

This is fixed in XRootD release 4.1.2

Earlier releases are likely to be vulnerable.


Mitigation
==========

N/A


Component installation information
==================================

See the XRootD web page. [R 1]



Recommendations
===============

Sites should upgrade in due course.


Credit
======

This vulnerability was reported by Gerd Behrmann


References
==========

[R 1] http://xrootd.org/


Comments
========

Comments or questions should be sent to svg-rat at  mailman.egi.eu

We are currently revising the vulnerability issue handling procedure so
suggestions and comments are welcome.


Timeline
========

Yyyy-mm-dd

2015-04-10 Vulnerability reported by Gerd Behrmann
2015-04-13 Acknowledgement from the EGI SVG to the reporter
2015-04-14 Software providers responded and involved in investigation
2015-04-17 Updated packages available
2015-04-18 Assessment by the EGI Software Vulnerability Group reported.
2015-05-12 Advisory written, delayed due to more serious issues taking priority
2015-05-13 Public disclosure
```
