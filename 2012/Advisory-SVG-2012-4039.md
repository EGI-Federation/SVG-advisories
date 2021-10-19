---
title: SVG:Advisory-SVG-2012-4039
---

```
** White information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2012-4039]

Title:       "High" Risk - WMS proxy theft impersonation vulnerability
Date:        2012-07-16
Updated:     2012-07-23, 2012-08-01, 2012-08-29

URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2012-4039

Introduction
============


A vulnerability has been found in WMS, which may allow a user to steal another
user's proxy.

This has been resolved in version 3.3.5-1 of the EMI WMS released July 12,
2012.

This has also been resolved in the EGI UMD on July 23rd 2012.

This vulnerability is also present in gLite 3.1 WMS which is no longer
supported, but see below for further information.

This advisory was re-sent on 1st August 2012 to state that sites should update
by 20th August 2012.

It is now public.

Details
=======

This vulnerability was found by the WMS development team.
It allows an authorized user in certain circumstances to steal another user's
proxy, hence it may result in identity theft.


Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment
Team.


Affected software
=================

The gLite WMS software distributed by EMI and redistributed in the EGI UMD is
affected.

The version in gLite 3.1 is also affected.

There is no WMS in gLite 3.2.



Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD should see:

http://repository.egi.eu/category/umd_releases/distribution/umd_1/

The WMS patch has been released in the UMD update 1.7.1

http://repository.egi.eu/2012/07/23/release-umd-1-7-1/

It can be now deployed by the sites.


gLite 3.1:

Should migrate to EMI WMS as soon as possible, but start with applying the
following special emergency update to resolve this issue:

-----------------------------------------------------------------------------
Procedure for gLite 3.1 WMS
===========================

1. Upgrade the affected rpm:

   rpm -Uvh \
http://cern.ch/grid-deployment/glite/ICE-fix/glite-wms-ice-3.1.54-3.sl4.i386.rpm

2. Restart the affected daemon:

   /opt/glite/etc/init.d/glite-wms-ice restart
-----------------------------------------------------------------------------



Recommendations
===============

Sites using EMI WMS either directly from EMI or from the EGI UMD should update
as soon as possible.

Sites using gLite 3.1 WMS should apply the emergency update immediately.

** Please carry out these actions by 20th August 2012 **

CSIRT will monitor sites for the presence of the vulnerability.

Sites using gLite 3.1 WMS should migrate to EMI WMS as soon as possible.



Important
=========

All sites using unsupported software, including any gLite 3.1 or other SL4
services and most of the gLite 3.2 services, should migrate away from
unsupported software as soon as possible.

Sites should be aware that:

1) The update for gLite 3.1 WMS is an exceptional emergency release, and
updates for unsupported software cannot be expected in future.

2) If a further high or critical risk vulnerability is found in unsupported
software (gLite 3.1, gLite 3.2 or SL4) it is unlikely that an update will be
made available and sites will be expected to migrate to supported software or
shutdown services immediately.

3) From 1st October 2012 sites deploying software gLite 3.1 or SL4 will be
asked to migrate to supported software or shutdown services immediately.



Other information
=================

Members of the SVG are aware that there has been a reluctance to migrate to EMI
WMS as in the past there have been problems with this software.
Several updates have been made to EMI WMS since then and it is of the experts'
opinion that the main problems have been resolved to a sufficient extent.

Due to gLite 3.1 WMS being deployed on a number of sites and a proper patch
not being available this advisory has not been placed on the public web page.

Advisory originally sent to site security contacts as 'AMBER' on request of
CSIRT to allow sites to upgrade before information further exposed.


Credit
======

This vulnerability was reported by Marco Cecchi of the WMS development team.

Timeline
========

Yyyy-mm-dd

2012-07-02 Vulnerability reported by Marco Cecchi
2012-07-02 Acknowledgement from the EGI SVG to the reporter
2012-07-02 Software providers responded and involved in investigation
2012-07-03 Assessment by the EGI SVG reported to the software providers
2012-07-12 Resolved in version 3.3.5-1 of the EMI WMS
2012-07-23 Updated packages available in the EGI UMD and as an exceptional
           update for gLite 3.1 WMs.
2012-07-23 Advisory sent to site security contacts as 'AMBER' on request of
           CSIRT to allow sites to upgrade before information further exposed.
2012-08-01 Resent to include a date by which time sites should update.
           (20th August)
2012-08-29 Distribution changed to White. Public disclosure
```
