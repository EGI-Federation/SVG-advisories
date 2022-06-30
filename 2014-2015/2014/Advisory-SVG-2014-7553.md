---
title: Advisory-SVG-2014-7553
permalink: /Advisory-SVG-2014-7553
---

## Advisory-SVG-2014-7553

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-7553]

Title:   EGI SVG Advisory 'High' Risk - Dirac SQL injection vulnerability
         [EGI-SVG-2014-7553]

Date:    2015-05-13
Updated: 2015-08-13

URL:     https://advisories.egi.eu/2014/Advisory-SVG-2014-7553

Introduction
============

An SQL injection vulnerability has been found in Dirac, which is exploitable by
any authorized user and allows proxy theft.

This has been fixed by the developers.

Update 13th August 2015

Changed to 'White' information - this is now the production version.


Details
=======

An SQL injection vulnerability has been found in Dirac, which allows an
authorized user to steal long lived proxies from other clients in the same
Dirac server, possibly including clients in other VOs.  This allows the
possibility of tampering with data, and impersonation of another user.  An
exploit has been written by the reporter, and the developers confirmed that
this vulnerability exists as described.


Risk category
=============

This issue has been assessed as 'High' Risk by the EGI SVG Risk Assessment
Team.


Affected software
=================

Dirac versions prior to v6r13

This vulnerability is fixed in Dirac v6r13


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

2014-10-14 Vulnerability reported by Simon Fayer from SVG
2014-10-27 Software providers responded and involved in investigation
2014-11-07 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2015-05-08 Updated packages available
2015-05-13 Advisory sent to sites
2015-08-13 Updated as fixed version is now the production version and placed on
           wiki
```
