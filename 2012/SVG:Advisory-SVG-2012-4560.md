---
title: SVG:Advisory-SVG-2012-4560
permalink: /SVG:Advisory-SVG-2012-4560/
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2012-4560]

Title:       EGI SVG Advisory 'Moderate' RISK DPM world writeable files

Date:        2012-12-19
Updated:

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2012-4560

Introduction
============

World writable files have been found in DPM version 1.8.4, available both
from the EGI UMD 2 repository and directly from EMI in the EMI 2 repository.

This has been fixed in the version of DPM available in the EGI UMD 2 and EMI 2.


Details
=======

World writable files have been found in DPM version 1.8.4 available both from
the EGI UMD 2 repository and directly from EMI in EMI 2.

The files affected are log files, hence a user may be able to alter logging
information.  There is no indication that more serious damage can be done.

This has been fixed in DPM version 1.8.5.


Risk category
=============

This issue has been assessed as "Moderate" risk by the EGI SVG Risk Assessment
Team.


Affected software
=================

DPM version 1.8.4 available both in the EMI 2 distribution and the EGI UMD 2
distribution.

This is fixed in DPM version 1.8.5.

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/

Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/


Recommendations
===============

Sites are recommended to update relevant components.


Credit
======

This vulnerability was reported to SVG by Mario David after originally been
found by the developers.

Timeline
========

Yyyy-mm-dd

2012-11-01 Vulnerability reported by to SVG by Mario David after originally
           been found by the developers.
2012-11-01 Acknowledgement from the EGI SVG to the reporter
2012-11-11 Software providers already fixing the problem
2012-11-15 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2012-11-22 Updated packages available in the EMI 2 repository
2012-12-17 Updated packages available in the EGI UMD 2 repository
2012-12-19 Public disclosure
```
