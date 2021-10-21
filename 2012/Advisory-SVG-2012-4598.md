---
title: Advisory-SVG-2012-4598
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2012-4598]

Title:   EGI SVG Advisory 'Moderate' RISK - VOMS Java APIs incorrect CRL
         checking
Date:    2013-02-19
Updated: 2013-04-17


URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2012-4598

Introduction
============

A vulnerability has been found in the VOMS Java APIs where CRL checking is not
correctly carried out.

This has been fixed by the developers and a new version is available.

This advisory is updated as some components required a re-release in order to
fully resolve the problem.


Details
=======

The developers found a problem with the VOMS Java API where the CRL is not
correctly checked.
This means that if a VOMS server were to be compromised, and the appropriate
server added to the CRL, VOMS certificates from this server may still be
accepted.

Although it is unlikely that a VOMs server were to be compromised, and this
vulnerability is not exploitable by itself, serious problems would arise if a
VOMS server were to be compromised and the CRL checking was not properly
carried out.

Hence this problem has been fixed.


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team


Affected software
=================

All versions of the VOMS Java API up to and including version 2.0.8.

This is fixed in VOMS version 2.0.10 as available in EMI 1 Update 23 and EMI 2
Update 8.

The package has also been released in EGI UMD-1  Release 1.10.0
http://repository.egi.eu/2013/02/19/release-umd-1-10-0/

and UMD-2 Release 2.4.0
http://repository.egi.eu/2013/02/18/release-umd-2-4-0/


Additionally, in order to complete the elimination of this vulnerablity
re-built components have been released as part of UMD-2 release 2.4.1
http://repository.egi.eu/2013/04/05/release-umd-2-4-1/


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD should see:


http://repository.egi.eu/category/umd_releases/distribution/umd-2/


Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/



Recommendations
===============


Sites are recommended to update relevant components to the VOMS java API 2.0.9



Credit
======

This vulnerability was reported by Andrea Ceccanti



Timeline
========
Yyyy-mm-dd

2012-11-06 Vulnerability reported by Andrea Ceccanti stating that the VOMS
           team had found this problem and were fixing it
2012-11-07 Acknowledgement from the EGI SVG to the reporter
2012-11-20 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2013-01-28 Updated packages available in the EMI distribution
2013-02-19 Updated packages available in the EGI UMD distributions
2013-02-19 Public disclosure
2013-02-19 Removed from public web page as some components required re-build to
           fully resolve
2013-04-05 UMD 2.4.1 release made available which fully resolves the problem
2013-04-17 Public disclosure
```
