---
title: Advisory-SVG-2015-9495
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2015-9495]

Title:   **UPDATE*** EGI SVG Advisory 'High' RISK - Vulnerability in the dCache
         SRM server module [EGI-SVG-2015-9495]

Date:    2015-09-22
Updated: 2015-09-30, 2015-10-26



URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2015-9495


Introduction
============

dCache [R 1] is a data storage and retrieval system.

A vulnerability has been found in the dCache SRM server module by the dCache
team, who also alerted SVG to this problem.

A fixed binary version is available on the dCache site [R 2].

**UPDATE**

A fixed version is now available in the EGI UMD.



Details
=======

See the dCache page. [R 1]


Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment
Team.


Affected software
=================


All dCache versions prior to this patch are affected.

The releases which fix this issue are are:

2.13.9
2.12.21
2.11.32
2.10.41
2.6.52


It was noted by the dCache team that several site still run the unsupported 2.6
dCache.  Given these sites currently suffer from a High risk vulnerability,
dCache  have made an additional release: 2.6.52


Mitigation
==========

N/A.


Component installation information
==================================


Updates are available on the dCache site [R 2]

Release notes are available at the dCache site.

https://www.dcache.org/downloads/1.9/release-notes-2.13.shtml
https://www.dcache.org/downloads/1.9/release-notes-2.12.shtml
https://www.dcache.org/downloads/1.9/release-notes-2.11.shtml
https://www.dcache.org/downloads/1.9/release-notes-2.10.shtml
https://www.dcache.org/downloads/1.9/unsupported/release-notes-2.6.shtml


The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

**UPDATE**

UMD 3.13.4 has been released and contains the fix for this issue at:

http://repository.egi.eu/2015/09/29/release-umd-3-13-4/


Other Information
==================


**Original statement**

To give sites time to upgrade their dCache, the dCache team will not release
any details of the vulnerability at this time.  This includes not making
public the source-code for the fix for a 'grace period' of two weeks, as doing
so would also reveal information on the vulnerability.

During this two week grace period, dCache will make no further releases.

Once the grace-period elapses, all code changes will be pushed into github and
dCache will continue normal bug-fix release cycles.

**UPDATE**

A fixed version is now available in the EGI UMD

**UPDATE 2015-10-26 **

The advisory is public, the fix has been in the UMD for over 3 weeks, so info
on details of the vulnerability may become public.


Recommendations
===============

Sites are recommended to update the SRM head node component as soon as possible
if they have not done so already.


Credit
======

This vulnerability was discovered by Gerd Behrmann (NDGF) from the dCache team.


References
==========


[R 1] https://www.dcache.org/

[R 2] https://www.dcache.org/downloads/1.9/




Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

We are currently revising the vulnerability issue handling procedure so
suggestions and comments are welcome.



Timeline
========

Yyyy-mm-dd

2015-09-15 Vulnerability discovered by Gerd Behrmann (NDGF) from the dCache
           team reported to SVG by Patrick Fuhrmann.
2015-09-15 Acknowledgement from the EGI SVG to the reporter
2015-09-18 Assessment by the EGI Software Vulnerability Group reported to the
           software providers.
2015-09-22 Updated packages available on the dCache site.
2015-09-29 Updated packages available in EGI UMD 3
2015-09-30 Updated advisory sent to sites
2015-10-26 Advisory placed on public wiki
```
