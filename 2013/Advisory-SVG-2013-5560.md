---
title: Advisory-SVG-2013-5560
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5560]

Title: EGI SVG Advisory 'Moderate' RISK - glite_wms_wmproxy_dirmanager allows
       any user to change the permissions on any directory
       [SVG EGI-SVG-2013-5560]

Date:  2014-08-06


URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2013-5560

Introduction
============

A vulnerability was found in glite_wms_wmproxy_dirmanager where any user is
allowed to change directory permissions.

This has been resolved in the version available in the EGI UMD some time ago.



Details
=======

glite_wms_wmproxy_dirmanager allows any user to create a directory, with any
permissions.

It also allows permissions on any existing directory too be changed.

Note that users cannot execute code on the WMS.

This applies to older versions available  EMI-3/UMD-3.

This has neem resolved some time ago.


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team.


Affected software
=================

This is fixed in glite-wms-interface-3.6.2-1  which was released as part of WMS
3.6.2.
Earliest fixed version in the UMD likely to be WMS 3.6.3 released in April
2014.

All versions of glite-wms-wmproxy-dirmanager prior to this are likely to be
affected.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Sites who wish to install directly from the EMI release should see:


http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/




Recommendations
===============

Sites are recommended to update to the latest version of WMS in due course if
they have not already done so in due course.


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.


Timeline
========

Yyyy-mm-dd

2013-05-22 Vulnerability reported by Simon Fayer.
2013-05-22 Acknowledgement from the EGI SVG to the reporter
2013-06-20 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2014-04-07 Updated packages available in the EGI UMD
2014-08-04 Asked for confirmation that this has been fixed.
2014-08-06 Public disclosure
```
