---
title: Advisory-SVG-2011-3202
permalink: /Advisory-SVG-2011-3202
---

## Advisory-SVG-2011-3202

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2011-3202]

Title:       'Low' RISK - L&B servers not being checked properly
Date:         2013-02-25
Updated:

URL:         https://advisories.egi.eu/2011/Advisory-SVG-2011-3202

Introduction
============

A vulnerability has been found in gLite Logging and Bookkeeping client,
where although the validity of the X509 certificate is checked properly,
the identity of the servers is not properly checked.

This has been resolved in the version of L&B available in the EGI UMD 2,
EMI 2, EGI UMD 1 and EMI 1.

Details
=======

A vulnerability has been found in gLite Logging and Bookkeeping client,
where although  the validity of the X509 certificate is checked properly,
the identity of the servers is not properly checked.

This vulnerability exists but is difficult to exploit, difficult to gain
anything from an exploit, and probably not exploitable without being traceable.


Risk Category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team.


Affected Software
=================

Logging and Bookkeeping version 3.0.12 and earlier.

This is resolved in Logging and Bookkeeping version 3.2.9

Sites wishing to ensure they have a fixed version should look for
glite-lbjp-common-gss-3.1.3 or later.

This is included in UMD version UMD 2.1.0

This is included in  UMD version UMD 1.10.0


Component Installation information
==================================

The official repository for the distribution of grid middleware for
EGI sites is repository.egi.eu which contains the EGI Unified Middleware
Distribution (UMD).

Sites using the EGI UMD should see:


http://repository.egi.eu/category/umd_releases/distribution/umd-2/

http://repository.egi.eu/category/umd_releases/distribution/umd_1/


For sites installing directly from EMI

Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/

http://www.eu-emi.eu/emi-1-kebnekaise-updates/



Recommendations
===============

Sites are recommended to update their systems in due course, if they are not
already running a version of the Logging and Bookkeeping which has this issue
resolved.


Credit
======

This vulnerability was reported by Daniel Kouril.

References
==========


Timeline
========
Yyyy-mm-dd

2011-11-29 Vulnerability reported by Daniel Kouril
2011-11-29 Acknowledgement from the EGI SVG to the reporter
2011-12-29 Software providers responded and involved in investigation
2011-12-02 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2012-08-06 Updated packages available in the EGI UMD-2
2012-12-17 SVG checked the status with the developers, as no progress had been
           reported.
           Found to have been resolved in August for EGI UMD 2, but not yet for
           EGI UMD 1 so decided to wait until fully resolved as 'Low' risk.
2013-02-25 Confirmed that it is now resolved in UMD-1
2013-02-25 Public disclosure


This is a placeholder for Vulnerability issue 3202.
The advisory has not been publicly released yet.
```
