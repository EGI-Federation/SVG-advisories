---
title: SVG:Advisory-SVG-2011-1866
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2011-1866]

Title:       Low Risk - VOMS file vulnerability
Date:        2011-06-20
Updated:     2011-07-14


URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2011-1866

Introduction
============

A Vulnerability has found in the VOMS server which allows the overwriting of
files.

This vulnerability is not applicable in VOMS 2.0 as available from the EGI
UMD-1 release.


Details
=======

A vulnerability has been found which allows anyone with an account on the VOMS
server to overwrite files on the VOMS server.

This problem does not occur in VOMS 2.0 as available from the EGI UMD-1
release.

This vulnerability is only exploitable by anyone with an account on the same
host as the VOMS server, which should not be the case.


Risk Category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team.


Affected Software
=================

All versions of the VOMS server prior to VOMS 2.0.


Mitigation
==========

N/A

Component Installation information
==================================

Sites may upgrade to  EGI UMD-1
http://repository.egi.eu/category/umd_releases/distribution/umd_1/



Recommendations
===============

Sites should upgrade to VOMS version 2.0 as available in the EGI UMD [R 1]  in
due course.

Sites are reminded that user accounts and/or other user access should not be in
place on the same host as the VOMS server.  Access to the VOMS server should be
restricted to local site administrators.


Credit
======

This vulnerability was reported by Steve Traylen.


References
==========

[R1] http://repository.egi.eu/category/umd_releases/distribution/umd_1/


Timeline
========
Yyyy-mm-dd

2011-05-09 Vulnerability reported by Steve Traylen.
2011-05-09 Acknowledgement from the EGI SVG to the reporter
2011-05-09 Software providers responded and involved in investigation
2011-05-11 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2011-05-11 Confirmation from Software providers that this is not a problem in
           VOMS 2.0 available in EMI.
2011-07-12 Updated packages available in the EGI UMD
2011-07-28 Public disclosure
```
