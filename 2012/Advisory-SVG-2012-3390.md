---
title: Advisory-SVG-2012-3390
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2012-3390]

Title:       "Low" Risk: DPM Information Leak Vulnerability

Date:        2014-08-05
Updated:

URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2012-3390

Introduction
============

An information leak vulnerability has been found in DPM (Disk Pool Manager.)

This has been resolved via a new version of the dpm-dsi library which is
available in the EGI UMD.



Details
=======

An information leak vulnerability has been found in DPM which may allow users
to access files including log files which they are not entitled to access.

This has been resolved via a new version of the dpm-dsi library used by DPM
which is available in the EGI UMD.

This version of this library which resolves this issue is also available in
EPEL.


Risk Category
=============

This issue has been assessed as "Low" risk by the EGI SVG Risk Assessment Team


Affected Software
=================

DPM versions containing versions of the dpm-dsi library earlier than
dpm-dsi-1.9.3 are affected.

This vulnerability has been fixed by version dpm-dsi-1.9.3 as available
in the EGI UMD-3


Mitigation
==========

No mitigation is recommended.


Component Installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

http://repository.egi.eu/2014/07/24/dpm-dsi-1-9-3-3/


Please note that DPM is no longer maintained in the EMI repository.


DPM is now also available in EPEL

https://fedoraproject.org/wiki/EPEL



Recommendations
===============

Sites are recommended to update their software in due course.


Credit
======

This Vulnerability was reported by  Ulf Tigerstedt


Timeline
========

Yyyy-mm-dd

2012-02-09 Vulnerability reported by Ulf Tigerstedt
2012-02-09 Acknowledgement from the EGI SVG to the reporter
2012-02-14 Software providers responded and involved in investigation
2012-02-20 Assessment by the EGI Software Vulnerability Group reported
           to the software providers
2014-07-24 Updated packages available in the EGI UMD
2014-08-04 Checked that above version fixes this vulnerability.
2014-08-05 Public disclosure
```
