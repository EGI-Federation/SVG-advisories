---
title: Advisory-SVG-2012-3765
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2012-3765]

Title:       EGI SVG Advisory 'Low' RISK - Gridftp CVE-201203292
Date:        2012-12-20


URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2012-3765

Introduction
============

A vulnerability was found in gridftp in the case where users mapped to a
non-existent user id in grid-mapfile may run as the last user in /etc/passwd

This was fixed by globus in May 2012 and this advisory is issued because
versions in the EGI UMD are no longer vulnerable.



Details
=======

The vulnerability was found in GridFTP 5.2.1.
Users whose DN is mapped to a non-existent unix user id in a grid-mapfile
may be mapped to the last user in /etc/passwd.

Globus announced this and provided a fix in May 2012.


Risk category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team


Affected software
=================

Version GridFTP 5.2.1 provided by Globus is affected.
It is not clear whether earlier versions of gridftp are vulnerable.

This is fixed in GridFTP version 5.2.2 or later.




Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).



http://repository.egi.eu/category/umd_releases/distribution/umd_1/

This is fixed in UMD 1 update 1.9.1
http://repository.egi.eu/2012/12/19/release-umd-1-9-1/


http://repository.egi.eu/category/umd_releases/distribution/umd-2/

This is fixed in UMD 2 update 2.3.1
http://repository.egi.eu/2012/12/17/release-umd-2-3-1/



Recommendations
===============

Sites are recommended to update relevant components in due course.



Credit
======

Vulnerability found by Doug Strain and Neha Sharma.

EGI SVG was alerted to this vulnerability by Romain Wartel, Leif Nixon and
David O'Callaghan.



References
==========

[R 1] globus advisory
http://lists.globus.org/pipermail/security-announce/2012-May/000019.html



Timeline
========
Yyyy-mm-dd

2012-05-?? Vulnerability found by Doug Strain and Neha Sharma.
           Issue fixed by globus.
2012-05-22 SVG alerted to the Vulnerability by  Romain Wartel,
           Leif Nixon and David O'callaghan
2012-05-22 Acknowledgement from the EGI SVG to the alerter
2012-05-29 Assessment by the EGI Software Vulnerability Group reported to
           the EGI DMSU
2012-12-17 Updated packages available in the EGI UMD 2
2012-12-19 Updated packages available in the EGI UMD 1
2012-12-20 Public disclosure
```
