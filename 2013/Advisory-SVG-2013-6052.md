---
title: Advisory-SVG-2013-6052
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-6052]

Title:   EGI SVG Advisory 'Moderate' RISK - PerfSONAR web interface
         vulnerabilities [EGI-SVG-2013-6052]

Date:    2014-08-05
Updated:

URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2013-6052

Introduction
============

Web interface vulnerabilities have been found in PerfSONAR.

These have been fixed some time ago in Perfsonar.

Note that more serious vulnerabilities have been found in perfSONAR since this
was

fixed, and sites asked to update.  Therefore this advisory is simply for
completeness and to acknowledge the reporter of these vulnerabilities. See [R
2]

For this reason this advisory is only placed on the wiki and not e-mailed to
sites.


Details
=======

PerfSONAR is widely used in the EGI infrastructure. [R 1]

A vulnerability has been found in the web interface which allows users to
obtain information which should not be available to them.

This was fixed by the Perfsonar team.


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team


Affected software
=================

Perfsonar.


Mitigation
==========

None.

Information from perfSONAR
==================================

Release notes are available at [R 3]



which includes a fix for this.

Recommendations
===============

No recommendations are made as sites have been told to update Perfsonar due to
a more serious vulnerability since this vulnerability was fixed.


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College.


References
==========

[R 1] https://twiki.cern.ch/twiki/bin/view/LCG/PerfsonarDeployment

[R 2] https://wiki.egi.eu/wiki/Advisory-SVG-2014-7162

[R 3] http://psps.perfsonar.net/toolkit/releasenotes/pspt-3_3_2rc3.html


Timeline
========
Yyyy-mm-dd

2013-09-12 Vulnerability reported by Simon Fayer
2013-09-12 Acknowledgement from the EGI SVG to the reporter
2013-10-01 Software providers contacted and responded and involved in
           investigation
2013-10-10 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2013-12-09 Updated packages available at the perfSONAR site
2014-07-17 Advisory sent for more serious vulnerability
2014-08-05 Public disclosure
```
