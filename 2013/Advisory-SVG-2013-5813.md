---
title: Advisory-SVG-2013-5813
---

```
** White information - Unimited distribution allowed                        **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5813]

Title:   EGI SVG Advisory: Result of CREAM vulnerability Assessment, including
         1 'High' risk problem [EGI-SVG-2013-5813]

Date:    2014-02-06
Updated: 2014-02-13



URL:         https://advisories.egi.eu/2013/Advisory-SVG-2013-5813

Introduction
============

This advisory is updated as there is now a fixed version in EGI UMD-2.

A vulnerability assessment (The active investigation of software for
vulnerabilities) of CREAM has been carried out by the autonomous university of
Barcelona and 4 vulnerabilities have been found.

These have been fixed in the version of CREAM available in UMD-3, and now in
UMD-2.


Details
=======

4 vulnerabilities have been found in CREAM:

CREAM-2013-0001

Allows users in certain conditions to hijack other users jobs, and access the
results.  This is only possible for users sharing a User Interface.

CREAM-2013-0002

This provides potentially helpful error information to an attacker.

CREAM-2013-0003

Allows users to cancel other users jobs running on a CE.

CREAM-2013-0004

This allows users access to CREAM database information.


These vulnerabilities have now been fixed.



Risk category
=============

Issues CREAM-2013-0001, CREAM-2013-0002, and CREAM-2013-0003 have been assessed
as 'Low'  risk by the EGI SVG Risk Assessment Team

Issue CREAM-2013-0004 has been assessed as 'High' risk by the EGI SVG Risk
Assessment Team.



Affected software
=================

This vulnerability Assessment was carried out on CREAM version 1.14.0.

Earlier versions are also likely to be affected.


These vulnerabilities have been fixed in CREAM versions

1.16.2 (EMI-3, UMD-3)
and
1.14.6 (EMI-2, UMD-2)

Interim versions earlier than this are also likely to be affected.



Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

The updated version is in UMD 3.3.0 released on 13th December 2013


Sites who wish to install directly from the EMI release should see:

http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates

EMI-3 update 9 has these problems resolved.


Sites using the EGI UMD 2 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/

The updated version is in UMD 2.8.0 released on 12th February 2014


http://www.eu-emi.eu/emi-2-matterhorn/updates/

EMI-2 update 19 has these problems resolved.


Please note that UMD-2 and EMI-2 end of security support is 30th April 2014 and
these products must be migrated from by 31st May 2014 at the latest.


Recommendations
===============

Sites who have not already upgraded since the versions referred to above were
released are recommended to update cream as soon as possible.
Sites may wish to check they are not running versions earlier than

1.16.2 (EMI-3, UMD-3)
and
1.14.6 (EMI-2, UMD-2)

In which these problems are resolved

Credit
======

These vulnerabilities were reported by Maxime Frydman, Manuel Brugnoli,
Joe Carrion from the autonomous university of Barcelona, as a result
of Vulnerability Assessment.
Elisa Heymann supervised these assessments.




Timeline
========

Yyyy-mm-dd

2013-05-15 Vulnerability CREAM-2013-0001 report received by SVG
2013-06-13 Vulnerability CREAM-2013-0002 report received by SVG
2013-06-25 Vulnerability CREAM-2013-0003 report received by SVG
                  All these were acknowledged, and assessed as 'Low' risk,
                    reported to software providers.
2013-07-15 Vulnerability CREAM-2013-0004 report received by SVG
2013-07-17 Lisa Zangrando stated all 4 fixed in CREAM software
2013-08-13 CREAM-2013-0004 assessed as 'High' risk by the EGI SVG.
           Updated packages available in EMI-3 and EMI-2
2013-12-13 Updated packages available in the EGI UMD-3
2014-02-06 Advisory sent to sites
2014-02-13 Updated as now fixed in EGI UMD-2
2014-02-27 Public disclosure
```
