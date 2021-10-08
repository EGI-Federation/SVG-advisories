---
title: SVG:Advisory-SVG-2012-3306
permalink: /SVG:Advisory-SVG-2012-3306/
---

```

** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2012-3306]

Title:       EGI SVG Advisory "Low" RISK - Potential for reduced availability of
             VOMS server

Date:        2013-09-17
Updated:     <date  yyyy-mm-dd>

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2012-3306

Introduction
============

A vulnerability has been found which may allow a Denial of Service attack on
a VOMS server.

This problem has been solved in the version of VOMS available in the EGI UMD-2.

A vulnerable version of VOMS has never been available in EGI UMD-3.


Details
=======

A vulnerability assessment was carried out on the VOMS server by Manuel Brugnoli
at the University of Barcelona.  A Vulnerability was found allowing a DoS attack
on the VOMS server by anyone able to connect to the VOMS server.


Risk category
=============

This issue has been assessed as "Low" risk by the  EGI SVG Risk Assessment Team.


Affected software
=================

This problem was found in VOMS version 2.0.2.

The file which fixes this is in the file:

voms-api-java-2.0.10-1

Earlier versions may be affected.



Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites is
repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).

Sites using the EGI UMD should see:


http://repository.egi.eu/category/umd_releases/distribution/umd-2/


Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/




Recommendations
===============

Sites are recommended to update relevant components in due course, if they have not
upgraded in recent months.


Credit
======

This vulnerability was reported by Manuel Brugnoli



Timeline
========
Yyyy-mm-dd

2012-01-17 Vulnerability reported by Manuel Brugnoli
2012-01-17 Acknowledgement from the EGI SVG to the reporter
2012-01-17 Software providers responded and involved in investigation
2012-02-01 Assessment by the EGI Software Vulnerability Group reported to the software providers
2013-02-13 Updated packages available in the EGI UMD-2
2013-08-19 After checking 'Low' risk issues, found fixed in UMD.
2013-09-16 Public disclosure
```