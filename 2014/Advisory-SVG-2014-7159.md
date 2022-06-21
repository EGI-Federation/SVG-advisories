---
title: Advisory-SVG-2014-7159
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2014-7159]

Title:   EGI SVG Advisory 'Low' RISK - VOMs Potential DoS  [EGI-SVG-2014-7159]

Date:    2015-08-18
Updated:

URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2014-7159

Introduction
============

A vulnerability has been found which allows a possible DoS attack on the VOMS
server.

This has been fixed by the VOMS team and the fixed version has been released in
the EGI UMD.

Note that this was fixed in Feb 2015, but the advisory was missed.


Details
=======

An error was introduced in VOMS 2.0.11 where there was an attempt to limit the
number of concurrent connections to the VOMS server. However, this was handled
incorrectly and it is possible that a DoS attack could take place.
This is also an operational problem, as the mis-handling means it may not be
possible to connect to a VOMS server when no attempt at a malicious DoS attack
is being made.


Risk category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team

Affected software
=================

This has been fixed in VOMS 2.0.12-1 which was released in UMD 3.11.0 in Feb
2015

VOMs Server version voms-2.0.11-1 has been shown to be vulnerable, and it's
thought that only 2.0.11 is vulnerable.


Mitigation
==========

N/A

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

Sites are recommended to update relevant components in due course.


Credit
======

This vulnerability was reported by Robert Frank from the University of Manchester.


Timeline
========
Yyyy-mm-dd

2014-06-17 Vulnerability reported by Robert Frank
2014       Acknowledgement from the EGI SVG to the reporter
2014-06-17 Software providers responded and involved in investigation
2014-06-18 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2014-06-18 Found it has already been fixed by the VOMS development team, it was
           considered a more serious operational issue
2014-11-10 Update in EMI repository
2015-02-16 Updated packages available in the EGI UMD
2015-08-17 Noticed that the advisory for this issue had been missed
2015-08-18 Advisory sent to sites
2015-08-18 Public disclosure
```
