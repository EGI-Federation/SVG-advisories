---
title: SVG:Advisory-SVG-2011-1641
permalink: /SVG:Advisory-SVG-2011-1641/
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2011-1641]

Title:       'Low' RISK - gLExec - prevention of job logging
Date:        2012-05-09
Updated:     2012-11-15

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-1641

Introduction
============

A vulnerability has been found in gLExec allowing a job to prevent the job
completed log record from being written to the gLExec log or syslog

This has been resolved in gLExec 0.9.0 which is released as part of EMI 2, and is
available in the EGI UMD 2 distribution.


Details
=======

gLExec is an identity switching program which allows a job to execute under a
different identity. This identity is selected using the user provided X.509
credential, and one of the various mapping services used on the Grid.

A detailed vulnerability assessment of gLExec 0.8 was carried out by
Daniel Crowell from the  University of Wisconsin Vulnerability assessment
group [R 1] and this vulnerability was reported.

It was found that a job can prevent the completion of log records from being
completed.


Risk category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team.


Affected software
=================

Versions of gLExec earlier than 0.9.0 are affected.

This is fixed in version gLExec version 0.9.0 released as part of EMI 2, which
is also released in EGI UMD 2.

Mitigation
==========

None is recommended.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

The EGI UMD 2 distribution is available from:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/


Recommendations
===============

Sites should update in due course, as is convenient to them.
It is recommended that gLExec is executed in Linger mode, and gLExec
configuration is suitable for the site.  See documentation  [R 2]

Further information
===================

Distribution of advisory delayed until solution available to sites installing
software from the EGI UMD, as SVG in contact with the developers and was aware
that progress was taking place.


Credit
======

This vulnerability was reported by Daniel Crowell of the University of
Wisconsin.

References
==========


[R 1] http://research.cs.wisc.edu/mist/includes/vuln.html

[R 2] https://wiki.nikhef.nl/grid/GLExec


Timeline
========

Yyyy-mm-dd

2011-03-28 Vulnerability reported by Daniel Crowell
2011-03-28 Acknowledgement from the EGI SVG to the reporter
2011-03-26 Software providers responded and involved in investigation.
2011-03-16 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2012-05-18 Updated packages available in EMI 2
2012-08-07 Updated packages available in the EGI UMD 2
2012-11-15 Confirmed correct packages are in EGI UMD 2
2012-11-15 Public disclosure
```
