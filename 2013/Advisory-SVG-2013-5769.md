---
title: Advisory-SVG-2013-5769
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5769]

Title:   EGI SVG Advisory 'Low' RISK - FTS3 - Lack of Authorization on config
         commands [EGI-SVG-2013-5769]

Date:    2014-08-05
Updated:


URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2013-5769

Introduction
============

A vulnerability has been found in FTS-3 [R 1] where configuration commands are
not authorized.

This has been fixed by the FTS-3 team some time ago.

FTS-2 is not affected.

As it was fixed a long time ago, and it's unlikely that sites are running
insecure

versions, this is not sent to sites but only placed on the wiki.


Details
=======

A vulnerability has been found in FTS-3 where configuration commands are not
properly authorized.

Additionally, in some circumstances a suspended or banned user may be able to
carry out configuration commands if they were able to carry out such commands
prior to the suspension.

This was fixed by the FTS-3 team.

This is included for completeness only on the wiki as it was fixed a long time
ago,

and the SVG was not aware that it was fixed.


FTS-2 which is available in UMD-2 is not affected.


Risk category
=============

These issues has been assessed as 'Low' risk by the EGI SVG Risk Assessment
Team


Affected software
=================

FTS-3

It is possible that the version on the EMI-3 site is still vulnerable, but that
has not been confirmed.


Component installation information
==================================

Software is available at the FTS-3 site.



Recommendations
===============

If sites are using FTS-3 have not upgraded since

If sites are using FTS-3 from EMI-3 they should consider migrating to


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.


References
==========

[R 1]  http://fts3-service.web.cern.ch/


Timeline
========

Yyyy-mm-dd

2013-07-10 Vulnerability reported by Simon Fayer
2013-07-11 Acknowledgement from the EGI SVG to the reporter
2013-07-12 Software providers involved in investigation
2013-07-15 Situation clarified by software providers and actions agreed
2013-08-21 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2013-07-15 Updated packages available at FTS-3 site
2014-08-04 Status update of vulnerability ticket requested, as close to TD
           found fixed immediately the team were alerted to the problem.
2014-08-05 Public disclosure
```
