---
title: Advisory-SVG-2015-8580
permalink: /Advisory-SVG-2015-8580
---

## Advisory-SVG-2015-8580

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-8580]

Title:   EGI SVG Advisory 'High' Risk - Dirac does not check CRLs
         [EGI-SVG-2015-8585]

Date:    2015-09-29
Updated: 2015-10-13



URL:     https://advisories.egi.eu/2015/Advisory-SVG-2015-8580

Introduction
============

A vulnerability has been found where Dirac does not check Certificate
Revocation Lists (CRLs) when making its SSL connections.

This has been fixed in the current production version of Dirac.


Details
=======

In the worst case scenario this may allow a user or someone with a stolen
certificate to submit jobs even after the certificate has been revoked in cases
where gLexec is not being used.


Risk category
=============

This issue has been assessed as 'High' Risk by the EGI SVG Risk Assessment
Team.


Affected software
=================

Dirac versions prior to v6r14

This vulnerability is fixed in Dirac v6r14


Mitigation
==========

N/A


Component installation information
==================================

See [R 1]


Recommendations
===============

Sites are recommended to update relevant components as soon as possible.


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.

References
==========

[R 1] https://github.com/DIRACGrid/DIRAC/wiki


Timeline
========
Yyyy-mm-dd

2015-05-05 Vulnerability reported by Simon Fayer from SVG
2015-05-05 Software providers responded and involved in investigation
2015-05-12 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2015-09-28 Updated packages available
2015-09-29 Advisory sent to sites
2015-10-13 Advisory placed on wiki.
```
