---
title: SVG:Advisory-SVG-2011-342
permalink: /SVG:Advisory-SVG-2011-342/
---

```

** WHITE information - Unlimited distribution allowed                       **

** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2011-342]

Title:  LOW Risk - Insecure Library Loading Vulnerability in the VOMS server.
Date:   2011-07-14

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-342

Introduction
============


This advisory is being issued because an insecure Library loading vulnerability has
been found in the VOMS Server.  This vulnerability has been assigned CVE-2010-3388.

The VOMS Server software has been updated to resolve this problem.


Details
=======


The vulnerability has been confirmed as existing. However, VOMS does not run with elevated privileges,
so no user whould be able to gain elevated access from exploiting this vulnerability.
Also, ordinary users do not have access to the VOMS server therefore would not be able to exploit it.


Risk Category
=============

This issue has been assess as 'Low' risk by the EGI SVG Risk Assessment Team.


Affected Software
=================


All versions of the VOMS server prior to VOMS 2.0.




Component Installation information
==================================


Sites may upgrade to  EGI UMD-1
http://repository.egi.eu/category/umd_releases/distribution/umd_1/






Recommendations
===============


Sites should upgrade to VOMS version 2.0 as available in the EGI UMD [R 1] in due course


Credit
======

This vulnerability was reported by Raphael Geissert


References
==========

[R1] http://repository.egi.eu/category/umd_releases/distribution/umd_1/





Timeline
========
Yyyy-mm-dd

2010-09-17 Vulnerability reported by  Raphael Geissert
2010-09-17 Acknowledgement from the EGI SVG
2010-09-17 Software providers responded and involved in investigation
2010-09-27 Assessment by the EGI Software Vulnerability Group reported to the software providers
2011-07-12 Updated packages available in the EGI UMD
2011-07-28 Public disclosure
```