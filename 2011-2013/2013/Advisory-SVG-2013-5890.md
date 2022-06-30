---
title: Advisory-SVG-2013-5890
permalink: /Advisory-SVG-2013-5890
---

## Advisory-SVG-2013-5890

```
** AMBER information - Limited distribution                                 **
** see https://go.egi.eu/tlp for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2013-5890]

Title:       EGI SVG Advisory 'Critical' RISK - CVMFS root exploit

Date:        2013-08-14
Updated:     2013-09-26 (Placed on wiki)

Information will be placed on the public wiki in 2 weeks.

URL:         https://advisories.egi.eu/2013/Advisory-SVG-2013-5890


Introduction
============

A vulnerability has been found in CVMFS where a user can gain root access.

This was fixed by the CVMFS team, reported to SVG and announced to the
'CVMFS talk' list on 13th August 2013

EGI SVG is sending this advisory to ensure all sites running CVMFS are
aware of the problem, in case some sites using CVMFS do not subscribe to
the CVMFS talk list and to inform of the risk category.

Sites running CVMFS should upgrade immediately.


Details
=======

A vulnerability has been found in CVMFS where a user can gain root access.
The bug is in the CVMFS clients, which allows a local user to gain root access.


Risk category
=============

This issue has been assessed as 'Critical' risk by the EGI SVG Risk Assessment
Team


Affected software
=================

Versions of CVMFS prior to 2.1.13 and 2.0.21 are vulnerable.

cvmfs-2.1.14 and CernVM-FS 2.0.22 are the versions which sites are recommended
to run.

(Note that cvmfs 2.1.13 and 2.0.21 introduced another bug which affected atlas
and possibly other VOs. This was quickly fixed in cvmfs-2.1.14)


Component installation information
==================================


Sites using CVMFS should see the CVMFS portal

http://cernvm.cern.ch/portal/cvmfs/release-2.1
http://cernvm.cern.ch/portal/cvmfs/release-2.0
http://cernvm.cern.ch/portal/filesystem/downloads



Recommendations
===============

Sites running CVMFS should update immediately

All running resources MUST be either patched or otherwise have a work-around
in place by 2013-08-21  T21:00+01:00. Sites failing to act and/or failing to
respond to requests from the EGI CSIRT team risk site suspension.



Credit
======

This vulnerability was discovered by Dmitrijus Bugelskis from CERN who reported
it to Remi Mollon in the CERN security Team.
Remi Mollon then forwarded the information to the CVMFS team and the EGI
Software Vulnerability Group.
The fixed version was provided by Jakob Blomer from the CVMFS team at CERN.


References
==========

[R 1] http://cernvm.cern.ch/portal/

Timeline
========

Yyyy-mm-dd

2013-08-?? Vulnerability discovered by Dmitrijus Bugelskis
2013-08-13 Remi Mollon from the CERN security team alerted EGI SVG
2013-08-13 Jakob Blomer of the CVMFS team provided a fix
2013-08-13 Jakob Blomer alerted cvmfs-talk list to the vulnerability and fix
2013-08-14 Acknowledgement from the EGI SVG
2013-08-14 Advisory drafted
2013-08-14 Risk Assessment by the EGI Software Vulnerability Group
2013-08-14 Advisory sent to sites and NGI security contacts.
2013-09-26 Public disclosure
```
