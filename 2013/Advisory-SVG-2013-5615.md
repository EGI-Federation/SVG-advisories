---
title: SVG:Advisory-SVG-2013-5615
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5615]

Title:   EGI SVG Advisory 'Moderate' RISK - Incorrect permission for APEL
         parser and client config
Date:    2013-08-17
Updated: <date  yyyy-mm-dd>

URL:     https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2013-5615

Introduction
============

A file permission vulnerability has been found in EMI-3 and UMD-3 versions of
APEL which may allow users to modify the APEL configuration.

This has been fixed in the latest version of the  EMI-3 distribution, available
directly  from EMI or from EGI UMD-3.


Details
=======

A file permission vulnerability has been found in EMI-3 and UMD-3 versions of
APEL which may allow users to modify the APEL configuration.

The version of APEL available in UMD-2 is not affected.


Risk category
=============

This issue has been assessed as 'Moderate'  risk by the EGI SVG Risk Assessment
Team


Affected software
=================

This is fixed in EMI-3 version APEL version 1.1.2-0 , available either directly
from EMI or from the EGI UMD-3.

Versions of APEL available in EGI UMD-3 prior to version are affected.

Versions of APEL in EMI-2 and UMD-2 are not affected.


Mitigation
==========

If sites do not wish to upgrade the site admin may enter the command:

chmod 600 /etc/apel/db.cfg



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

Sites running the version of APEL from EMI-3/UMD-3 are recommended to update
their relevant components.

If they prefer, they may carry out the mitigation.


Credit
======

This vulnerability was reported by Franciszek Klajn.


Timeline
========
Yyyy-mm-dd

2013-05-27 Vulnerability reported by Franciszek Klajn.
2013-05-28 Acknowledgement from the EGI SVG to the reporter
2013-05-29 Software providers responded and involved in investigation
2013-06-14 Software providers made a fix available prior to integration in
           EMI-3/EGI UMD
2013-06-14 Risk set to 'Moderate'
2013-06-14 Fixed by the development team.
2013-09-12 Updated packages available in the EGI UMD 3 version
2013-09-17 Public disclosure
```
