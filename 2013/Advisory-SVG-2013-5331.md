---
title: Advisory-SVG-2013-5331
---

```
** White information - unlimited distribution                               **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG  ADVISORY [EGI-SVG-2013-5331]

Title:   EGI SVG Advisory 'High' RISK - EMI WMS Impersonation vulnerability.
Date:    2013-06-28
Updated: 2014-06-23


Only update is to place on public wiki, as sites deploying a vulnerable version
should have migrated away from this by now.

URL:         https://advisories.egi.eu/2013/Advisory-SVG-2013-5331


Introduction
============

A vulnerability has been found in WMS which may allow impersonation.

This vulnerability is present in versions distributed in EMI-2, UMD-2, EMI-3
and UMD-3.

This problem has been fixed in the version of WMS available in EMI-3 and UMD-3,
but not in the version available in EMI-2 and UMD-2.



Details
=======

A vulnerability has been found in WMS which may allow impersonation.

The issue is fixed in versions available in EMI-3 and EGI UMD-3.

This is not fixed in the version available in EMI-2 and UMD-2, however
sites should have migrated from this by now.

It is also noted that the EMI 2 version of WMS does not handle SHA-2
certificates.


Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG


Affected software
=================

For EMI 3 this issue is fixed in  WMS 3.5.1 (glite-wms-interface-3.5.0-8)

This is available from EMI-3 update 4  (available from 21st May 2013)
and from UMD-3 version 3.1.0  (available from 27th June 2013)

Earlier versions are vulnerable.


The current EMI 2 version (whether available from the EGI UMD-2 or directly
from EMI) is vulnerable.



Mitigation
==========

No mitigation is recommended.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Release notes for this version are at:

http://repository.egi.eu/2013/06/26/release-umd-3-1-0/


Sites who wish to install directly from the EMI release should see:

http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/



Recommendations
===============

Sites running versions of WMS directly from EMI-3 should check that the version
they are running is up to date, and if it is not update their software as soon
as possible. Sites are likely to be running a vulnerable version if they have
not updated to the latest version of WMS in EMI-3 since 21st May 2013.

Sites running versions of WMS from EGI UMD-3 should update as soon as possible.

For sites running EMI-2 version of WMS, either directly from EMI or from EGI
UMD-2 are strongly recommended to carry out a planned migration to the EMI-3
version, either directly from EMI or from EGI UMD 3.  This will eliminate this
vulnerability from their sites and help prepare them for the SHA-2 migration
which starts in October 2013.


Other information
================

The ability to impersonate another user puts this vulnerability into the 'high'
risk category, however it is not easy to find therefore we are not insisting on
a rapid migration from the EMI-2 version of WMS due to this vulnerability.
Sites should be aware that this could change if, for example, details of this
exploit were to become public.

Sites will need to migrate away from software which does not support SHA-2
anyway by October 2013 if they wish to continue to support all their users.
This includes the EMI-2 version of WMS.

It is also unclear whether we need to now consider the EMI-2 version of WMS as
out of security support.


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.



Timeline
========

Yyyy-mm-dd

2013-04-09 Vulnerability reported by Simon Fayer
2013-04-10 Acknowledgement from the EGI SVG to the reporter
2013-04-11 Software providers responded and involved in investigation
2013-04-17 Assessment by the EGI Software Vulnerability Group reported
           to the software providers
2013-05-21 Updated packages available in EMI-3
2013-06-27 Updated packages available in EGI UMD 3
2013-06-28 Advisory sent to sites as 'Amber'
2014-06-23 Advisory placed on public wiki
```
