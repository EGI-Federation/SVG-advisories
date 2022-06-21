---
title: Advisory-SVG-2013-5266
---

```
** White information - unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5266]

Title:   EGI SVG Advisory 'Moderate' RISK - BDII Password access vulnerability
         [EGI-SVG-2013-5266]

Date:    2013-09-17
Updated: 2013-10-25

URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2013-5266

Introduction
============

A vulnerability has been found where it is possible in limited circumstances
for a user with a valid certificate to access the ldap password.

This vulnerability has been fixed by the BDII developers and a fixed version is
available in EMI 2 and EMI 3 and in EGI UMD2 and EGI UMD 3.



Details
=======

A vulnerability has been found where it is possible in limited circumstances
for a user with a valid certificate to access the ldap password. While an
exploit has been written to prove this is possible, it is difficult to exploit.


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team


Affected software
=================

This has been fixed in

bdii-5.2.21-1
glite-yaim-bdii-4.3.14-1
glite-info-provider-service-1.13.1-1


Earlier versions are likely to be vulnerable.


Component installation information
==================================


The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites who wish to install directly from the EMI 2 release should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Sites who wish to install directly from the EMI release should see:


http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/



Recommendations
===============

Sites are recommended to update relevant components.

Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.


Timeline
========
Yyyy-mm-dd

2013-03-22 Vulnerability reported by Simon Fayer
2013-03-25 Acknowledgement from the EGI SVG to the reporter
2013-04-03 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2013-08-02 Updated packages produced by the BDII team
2013-09-12 Updated packages available in the EGI UMD 3, and past the target date.
2013-09-17 Sending by e-mail, but not posting on web page until fixed in UMD-2
2013-10-23 Fixed version in UMD 2.7.0
2013-10-25 Public disclosure
```
