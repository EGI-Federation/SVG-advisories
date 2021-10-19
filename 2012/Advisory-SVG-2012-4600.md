---
title: SVG:Advisory-SVG-2012-4600
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2012-4600]

Title:   EGI SVG Advisory 'High' Risk - EMI-2 dcache-srmclient contains world
         writeable files

Date:    2012-11-14
Updated: 2012-11-21


Introduction
============

A problem has been found with the EMI-2 dcache-srmclient, it contains world
writable executable files.

This allows a malicious user to inject arbitrary code which may be executed by
another user calling these libraries, with the privileges of the user calling
these libraries.

This problem has been fixed and sites are recommended to update relevant
components as soon as possible.



Details
=======

A problem has been found with the EMI-2 dcache-srmclient, it contains world
writable executable files.  This allows a malicious user to inject arbitrary
code which may be executed by another user calling these libraries, with the
privileges of the user calling these libraries.

As far as we can ascertain, it is not possible to inject code which may get
executed as root, and the vulnerability is only exploitable by an authorized
user.

The User Interface (UI) and the Worker Nodes (WN) running EMI 2 or UMD 2
software contain this vulnerability.

Sites are recommended to update relevant components as soon as possible.



Risk category
=============

This issue has been assessed as 'High'  risk by the EGI SVG Risk Assessment
Team.

Affected software
=================

 dcache-srmclient-2.1.1-1 is the affected piece of software.

 Both the sl5 and sl6 versions in both EMI 2 and UMD 2 are affected.


 The issue is fixed in version
dcache-srmclient-2.2.4-2.el5.x86_64.rpm


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/

Update UMD-2.2.2



Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/

(update 5)


Recommendations
===============

Sites who have installed EMI 2 or UMD 2 version of the dcache client are
recommended to immediately update their software.


Other information
=================

Unfortunately, this problem was found after sites were asked to migrate
to this software. Hence it has been fixed as an emergency release.

The advisory made public at
https://wiki.egi.eu/wiki/Advisory-SVG-2012-4600
after sites have had been given 1 week to update (by agreement with CSIRT)


Credit
======

This vulnerability was reported by John Green.


Timeline
========

Yyyy-mm-dd

2012-11-07 Vulnerability reported by John Green.
2012-11-07 Acknowledgement from the EGI SVG to the reporter
2012-11-07 Software providers responded and involved in investigation
2012-11-12 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2012-11-14 Updated packages available in the EGI UMD and EMI distribution
2012-11-21 Public disclosure
```
