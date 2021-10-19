---
title: SVG:Advisory-SVG-2013-5268
---

```

** White information - unlimited distribution                               **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5268]

Title:   EGI SVG Advisory 'High' RISK - CREAM BUpdater improperly validated
         input / arbitrary command execution [EGI-SVG-2013-5268]

Date:    2013-05-24
Updated:

In 2 weeks this will be placed on public wiki at:

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2013-5268

Introduction
============

A Vulnerability has been found in the CREAM BUupdater where input is not
properly validated.

This has been resolved in the version of CREAM distributed both as part of EMI
2 and EMI 3 and in the EGI UMD 2 and EGI UMD 3 and sites are recommended to
update.


Details
=======

A vulnerability was reported where the CREAM BUupdater does not properly verify
input data and may allow authenticated users to submit entries to the job
registry.
This allows arbitrary shell command execution.

Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment Team.


Affected software
=================

This is fixed in BLAH 1.18.3 which is part of EMI 2 earlier versions of this
software are affected.

This is fixed in BLAH 1.20.1 which is part of EMI 3 earlier versions of this
software are affected

Mitigation
==========

No Mitigation is available.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 2 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/

Sites who wish to install directly from the EMI 2 release should see:


http://www.eu-emi.eu/emi-2-matterhorn/updates/


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Sites who wish to install directly from the EMI release should see:


http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/



Recommendations
===============

Sites should update the relevant components as soon as possible.


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.



Timeline
========

2013-03-26 Vulnerability reported by Simon Fayer from Imperial College, London
2013-03-26 Acknowledgement from the EGI SVG to the reporter
2013-04-05 Assessment by the EGI Software Vulnerability Group reported
           to the software providers
2013-04-17 Updated packages available in EMI 2 and EMI 3
2013-05-24 Updated packages in UMD-2 as well as UMD-3
2013-05-24 Advisory released to sites and NGI security contacts
2013-06-14 Public disclosure
```
