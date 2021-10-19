---
title: SVG:Advisory-SVG-2014-6963
---

```
Title:   EGI SVG Advisory 'High' RISK - DPM version in EPEL [EGI-SVG-2014-6963]
Date:    2014-05-12
Updated:

URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2014-6963


Introduction
============

A vulnerability has been introduced to one version of DPM released in EPEL.

This allows an unauthenticated user to access data, and to modify data.

This has now been fixed.


Details
=======

A vulnerability has been introduced by the developers and found by the
developers in a version of DPM released in EPEL.

This vulnerable version of DPM has only been made available in EPEL and is only
deployed on a small number of sites.

This vulnerability has been fixed in the version of DPM now available in EPEL.

Information on DPM itself is available on the DPM Wiki [R 1]

Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment
Team.



Affected software
=================

DPM version available in EPEL dmlite-libs-0.6.2-1 is affected.
Note that this is the **ONLY** vulnerable version.

This is fixed in dmlite-libs-0.6.2-2

Earlier versions of DPM are not affected.

The versions in the EGI UMD are not affected.


Mitigation
==========

N/A - any sites which have installed the vulnerable version should update as
soon as possible.


Component installation information
==================================

Sites installing from EPEL who have the vulnerable version should simply update
using

yum update


Followed by a restart of the DPM daemons (incl. httpd, xrootd and gridftp).

(or alternatively re-start the machine.)

More information in the installation and configuration of DPM is available in
[R 2] and [R 3]



Recommendations
===============

Affected sites are recommended to update relevant components as soon as
possible.


Credit
======

This vulnerability was reported by David Smith of the DPM team.


References
==========

[R 1] Main DPM wiki: https://svnweb.cern.ch/trac/lcgdm/wiki/Dpm

[R 2] Installation: https://svnweb.cern.ch/trac/lcgdm/wiki/Dpm/Admin/Install

[R 3] Configuration:
https://svnweb.cern.ch/trac/lcgdm/wiki/Dpm/Admin/ConfigurationIdx


Timeline
========

Yyyy-mm-dd

2014-05-02 Vulnerability reported by David Smith
2014-05-02 Acknowledgement from the EGI SVG to the reporter
2014-05-02 Software providers providing fix
2014-05-08 Assessment by the EGI Software Vulnerability Group at EGI SVG
           monthly meeting
2014-05-08 Risk reported to the software providers
2014-05-08 Updated packages available in the EPEL repository
2014-05-12 Amber advisory sent to sites.
2014-06-02 Public disclosure
```
