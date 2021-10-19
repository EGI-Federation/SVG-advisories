---
title: SVG:Advisory-SVG-2011-1502
---

```
** WHITE information - Unlimited distribution allowed  **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI Software Vulnerability Group (SVG) ADVISORY [EGI-SVG-2011-1502]

Title:       HIGH - WMS vulnerability
Date:        2011-03-16
Updated:     2011-04-04


URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2011-1502


Introduction
============

The gLite Workload Management System (WMS) is a service that can be used by
authorized users of supported Virtual Organizations to manage jobs submitted
to any number of EGI sites.  The WMS is deployed at many EGI sites.

A vulnerability has been found in the gLite WMS that allows authorized
users to gain access to proxy credentials of other authorized users.


Risk Category
=============

The EGI SVG Risk Assessment Team (RAT) has assessed this vulnerability
as 'High' risk.



Affected Software
=================

glite-WMS-3.1.30-0 and all prior versions are affected.



Component Installation information
==================================

Release details may be found at http://glite.cern.ch/R3.1/sl4_i386/updates/


The vulnerability is fixed in update 71 or later.


https://savannah.cern.ch/patch/?4736 fixes this patch.



Recommendations
===============

The SVG recommends that sites running gLite WMS services update to the latest
version (3.1.31-0 or later) as soon as possible.



Credit
======

The potential vulnerability was first discovered by Igor Sfiligoi (UCSD).
Burt Holzman (FNAL) suggested the gLite WMS might be affected and the
presence of the vulnerability was confirmed by David Smith and Maarten
Litmaath.  The fix was designed and provided by David Smith.


References
==========


Timeline
========
Yyyy-mm-dd

2011-01-24 Burt Holzman suggests the gLite WMS might be affected
2011-01-25 Presence of the vulnerability confirmed, design of fix started
2011-02-28 New code packaged and tested
2011-04-04 Updated packages available from gLite
2011-04-04 Public disclosure




On behalf of the  EGI SVG
```
