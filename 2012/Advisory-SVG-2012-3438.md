---
title: Advisory-SVG-2012-3438
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2012-3438]

Title:        EMI VOMS CRL handling vulnerability 'Low' RISK

Date:         2012-03-03
Updated:      2012-04-02


URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2012-3438

Introduction
============

A vulnerability has been found in EMI VOMS which may allow a user whose
certificate has been revoked to generate a VOMS proxy.  This was reported to
the EGI SVG.

Another result of the software bug that results in this vulnerability is that
some certificates are rejected even though they are valid.

This problem has been fixed and a new version is available.


Details
=======

There is an error in the EMI VOMS service specific to the c/c++ VOMS daemons
which handles CRLs incorrectly.

This error allows most users who possess a revoked certificate to get a VOMS
attribute certificate bound to the revoked certificate. This is considered to
be a 'Low' risk security error since most services carry out further checking
of the certificates and will reject the VOMS proxy associated with the revoked
certificate.

However, another result of this software bug is that some valid certificates
may be rejected.

Risk Category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team.
However, greater urgency for fixing this issue results from the rejection of
valid certificates.


Affected Software
=================

This problem is found in VOMS 2.0.2 released in EMI.

The problem is fixed in  VOMS 2.0.7 released as part of EMI Update 14 and is
available in UMD 1.6.0.

gLite 3.1 and gLite 3.2 are not affected, as they contain different CRL
handling software.


Mitigation
==========

No mitigation is recommended.


Component Installation information
==================================

Release notes for UMD-1.6.0

http://repository.egi.eu/2012/04/02/release-umd-1-6-0/


The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distrbution
(UMD).


http://repository.egi.eu/category/umd_releases/distribution/umd_1/

The update announcement for VOMS from EMI can be found at:

http://www.eu-emi.eu/emi-1-kebnekaise-updates/-/asset_publisher/hHg1/content/important-note-on-automatic-updates#VOMS_v_2_0_7_task_26570


Recommendations
===============


Sites are recommended to update relevant components, not only to solve this
vulnerability but also to avoid rejection of valid certificates.


Credit
======

This vulnerability was reported by Mike Jones from Manchester University


References
==========


http://repository.egi.eu/category/umd_releases/distribution/umd_1/

http://www.eu-emi.eu/emi-1-kebnekaise



Timeline
========
Yyyy-mm-dd

2012-02-17 Vulnerability reported by Mike Jones
2012-02-17 Acknowledgement from the EGI SVG to the reporter
2012-02-20 Software providers contacted and involved in investigation
2012-02-23 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2012-04-04 Updated packages available in the EGI UMD
2012-04-04 Public disclosure
```
