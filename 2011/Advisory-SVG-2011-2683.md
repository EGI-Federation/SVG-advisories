---
title: Advisory-SVG-2011-2683
permalink: /Advisory-SVG-2011-2683
---

## Advisory-SVG-2011-2683

```
** WHITE information - unimited distribution allowed                        **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2011-2683]

Title:       "High" Risk: DPM SQL injection vulnerability
Date:        2013-02-08
Updated:     2013-02-19

URL:         https://advisories.egi.eu/2011/Advisory-SVG-2011-2683

Introduction
============

Multiple SQL injection vulnerabilities has been found in DPM (Disk Pool
Manager)

A new version of DPM which resolves these vulnerabilities is now available
in the in the EMI-1 and EMI-2 distributions.

This advisory is updated as this new version is now available in
EGI UMD-1 and EGI UMD-2.


Details
=======

Insufficient input validation in parts of the DPM code allow an authenticated
user to inject arbitrary SQL commands via the DPM headnode.  This could result
in unauthorised modification of DPM metadata or, depending on the privileges of
the DPM SQL user, the creation of files on the DPM SQL server.

The issue was originally assessed as 'Low' risk but some time later an exploit
was demonstrated and it was re-assessed as 'High' risk.


Risk Category
=============

This issue has been assessed as "High" risk by the EGI SVG Risk Assessment Team


Affected Software
=================

DPM versions up to and including DPM 1.8.5 are affected.

This vulnerability has been fixed in DPM 1.8.6 as available
in EMI 1 Update 23 and EMI 2 Update 8.

The package has also been released in EGI UMD-1
Release 1.10.0 http://repository.egi.eu/2013/02/19/release-umd-1-10-0/

and UMD-2 Release 2.4.0
http://repository.egi.eu/2013/02/18/release-umd-2-4-0/


Mitigation
==========

No mitigation is recommended.


Component Installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


http://repository.egi.eu/category/umd_releases/distribution/umd_1/

http://repository.egi.eu/category/umd_releases/distribution/umd-2/


Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/

http://www.eu-emi.eu/emi-1-kebnekaise-updates/


Recommendations
===============

Sites are recommended to update their software as soon as possible.


Credit
======

This vulnerability was originally reported by  Adam Zabrocki.
A serious exploit was demonstrated by Leif Nixon after which the Risk was
re-assessed as 'High'.


References
==========


Timeline
========
Yyyy-mm-dd

2011-08-03 Vulnerability reported by Adam Zabrocki
2011-08-03 Acknowledgement from the EGI SVG to the reporter
2011-08-03 Software providers responded and involved in investigation
2011-09-06 Assessment by the EGI Software Vulnerability Group reported to the
           software providers (Low risk)
2012-11-13 Re-assessed as 'High' risk after exploit demonstrated by Leif Nixon.
2013-01-28 Updated packages available in the EMI distribution
2013-02-08 Advisory sent as 'Amber' information as past Target Date and sites
           installing directly from EMI should be made aware of this.
2013-02-19 Updated packages available in the EGI UMD-1 and EGI UMD-2
2013-03-05 Public disclosure on wiki, after allowing sites to upgrade.
```
