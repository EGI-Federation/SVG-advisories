---
title: SVG:Advisory-SVG-2011-504
---

```
Updated 26th January 2012 - Patch available on 24th January 2012 for gLite 3.2.

** WHITE information - Unlimited distribution allowed        **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP  for distribution restrictions **

EGI SVG  ADVISORY [EGI-SVG-2011-504]

Title:       APEL publisher vulnerability - 'Low' RISK
Date:        2011-11-18
Updated:     2011-12-21
Updated:     2012-01-24
Updated      2012-01-26

Introduction
============

A  vulnerability has been found in the APEL accounting publisher software,
which may allow users to make a copy of the host key of the system on which
APEL is running.

This problem has been resolved in the EGI UMD and EMI distributions released.

This advisory is updated as it is now also resolved in gLite3.2.

Details
=======

There is a file permission problem in APEL which may allow users to make a copy
of the host key, this is only a problem if APEL is co-located on another
service accessible by the user, such as a CE.


Risk Category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team


Affected Software
=================

For EMI/UMD versions
--------------------

APEL-publisher versions earlier than version. 3.2.8, containing
glite-apel-publisher-2.0.16-0, are affected.

APEL-publisher version. 3.2.8, containing glite-apel-publisher-2.0.16-0
provides the fix for this issue.

The Fixed version is available in

UMD 1.4 (or later)

EMI EMI 1 (Kebnekaise) - Update 10 (24.11.2011)

gLite 3.2
---------

APEL-publisher versions earlier than glite-apel-publisher-2.0.13-8 are affected
glite-apel-publisher-2.0.13-8 provides the fix for this issue.

This is available from:

http://glite.cern.ch/security_updates

Update 2

Mitigation
==========

If APEL is co-located with another service  (e.g. a CE) then sites may wish to
check and change the file permission on the /etc/grid-security/ keystore if
necessary.

This should be carried out by sites who are not planning to upgrade shortly.


Component Installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distrbution
(UMD).

Sites using the EGI UMD should see:

http://repository.egi.eu/2011/12/19/apel-publisher-3-2-8/


Sites installing directly from EMI may upgrade directly from EMI if they
haven't done so already see:

EMI-1 site http://www.eu-emi.eu/emi-1-kebnekaise, details of this item are at:

http://www.eu-emi.eu/emi-1-kebnekaise-updates/-/asset_publisher/Ir6q/content/update-10-24-11-2011#APEL_publisher_v_3_2_8_task_2390


gLite 3.2:

gLite 3.2 Security Update 2 available from
http://glite.cern.ch/security_updates


Recommendations
===============

Sites installing from the EGI UMD or directly from EMI should update their
sites in due course.

Sites installing gLite 3.2 should update in due course.

If sites are have APEL co-located with another service they should consider
upgrading soon or following the Mitigation.


Other information
=================

This advisory has been updated on 24th January 2012 and made public as the
problem is now also resolved in gLite 3.2.

Credit
======

This vulnerability was reported by Valentin Vidic and later independently by
Jan Astalos.


Timeline
========

Yyyy-mm-dd

2010-11-15 Vulnerability reported by Valentin Vidic
2010-11-15 Acknowledgement from the EGI SVG to the reporter
2010-11-15 Software providers responded and involved in investigation
2010-11-23 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2011-10-12 Issue found and reported again independently by Jan Astalos
2011-11-24 Updated packages available in EMI
2011-12-19 Updated version in EGI UMD.
2011-12-21 Advisory distributed to site and NGI security contacts.
2012-01-24 Advisory updated and uploaded to web page as it is now also resolved
           in gLite 3.2
2012-01-26 Update to correct Affected software EMI/UMD version and gLite 3.2
           version of gLite publisher
```
