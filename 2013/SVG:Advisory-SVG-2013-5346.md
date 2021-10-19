---
title: SVG:Advisory-SVG-2013-5346
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5346]

Title:  EGI SVG Advisory 'Moderate' risk, WMS allows other users to access
        logging information [SVG EGI-SVG-2013-5346]

Date:   2013-08-06
Updated:


URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2013-5346

Introduction
============

There was a vulnerability in WMS where users could access other users logging
information.

This is information should not be accessible by general users, it is a
confidentiality issue.

This was confirmed as having been fixed some time ago, during 2013.


Details
=======

There was a file permission problem on the WMS log files which allows users who
understand how to access other users log files the ability to access other
users log files.

This is considered to be a vulnerability, as logging information should not be
accessible by general users.

EGI cannot guarantee confidentiality, and users VOs and NGIs are generally
aware that general usage is not confidential. In particular, log files are
accessible by site administrators across the Grid.


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team.


Affected software
=================

WMS.

It is certainly fixed in the current version, WMS 3.6.5 and probably some
earlier versions going back to 3.6.1 which was released in December 2013.
Versions earlier than 3.6.1 are likely to be vulnerable.

Component installation information
==================================

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Sites who wish to install directly from the EMI release should see:


http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/


Recommendations
===============

Sites are recommended to update to the latest version of WMS in due course if
they

have not already done so in due course.


Credit
======

This vulnerability was reported by Sven Gabriel


Other information
=================

The risk category reflects the fact that EGI takes confidentiality seriously.

EGI's usage of Logging information is stated as point 9 in the EGI Acceptable
Use Policy [R 1]

It is difficult to ascertain whether other middleware allows users access to
other users log files. If any further cases are found, they will be treated as
vulnerabilities.


References
==========

[R 1] The EGI Acceptable Use Policy (AUP)
https://documents.egi.eu/secure/ShowDocument?docid=1779


Timeline
========

Yyyy-mm-dd

2013-04-09 Vulnerability reported by Sven Gabriel
2013-04-09 Acknowledgement from the EGI SVG to the reporter
2013-04-18 Separated from other issue, by Sven Gabriel
2013-05-16 Discussed at SVG monthly meeting. Agreed it is a vulnerability.
2013-06-18 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2013-??-?? Updated packages available in the EGI UMD.
2014-08-04 Asked for confirmation that this has been fixed. Stated fixed quite
           some time ago
2014-08-06 Public disclosure
```
