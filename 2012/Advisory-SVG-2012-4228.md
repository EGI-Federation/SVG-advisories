---
title: Advisory-SVG-2012-4228
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2012-4228]

Title:   EGI SVG Advisory 'Low' RISK - SAML implementation vulnerability in
         Unicore

Date:    2012-08-19
Updated:

URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2012-4228

Introduction
============

A vulnerability has been found in some Unicore components which may allow a
user to impersonate another user.

This has been fixed in the version of Unicore currently available in EGI UMD 2.


Details
=======


A vulnerability in some implemetations of SAML has been reported [R 1].

This may allow a user to impersonate another user.

Members of the SVG investigated and some of the Unicore components were found
to be vulnerable.

Two types of exploit were found.

One which potentially allows a user to delete another users workflow, but it is
unlikely any sites are configured in a way which allows this.

One allows impersonation, but can only be exploited in very rare circumstances.

No other middleware used in EGI is known to be vulnerable.


Risk category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team


Affected software
=================

The following Unicore components are affected:

   Unicore/X

   U. Registry

   Workflow Service

   Service Orchestrator


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/

This was released as part of the UMD update 2.6.0 on 12th June 2013


Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/

This was released as part of the EMI 2 Update 8 on 28th January 2013.



Recommendations
===============

Sites are recommended to update relevant components in due course, if they have
not updated since the software was released.



Credit
======

The software vulnerability group was alerted to the generic vulnerability
type by Tobias Dussa.
Unicore components were found to be vulnerable by Krzysztof Benedyczak.


References
==========

[R 1] On Breaking SAML: Be Whoever You Want to Be.  Juraj Somorovsky, Andreas
      Mayer, Jörg Schwenk, Marco Kampmann, Meiko Jensen.
      http://www.nds.rub.de/research/publications/BreakingSAML/


Timeline
========

Yyyy-mm-dd

2012-08-13 Tobias Dussa Alerted CSIRT to General Vulnerability type.
2012-08-13 Acknowledgement from the EGI SVG to the reporter
2012-08-28 Krzysztof Benedyczak found that some Unicore components are
           vulnerable
2012-      Vulnerability better understood, and to include classic XSW attacks.
2012-      Various checks on other components, none found to be vulnerable.
2012-12-03 Assessment by the EGI Software Vulnerability Group for the Unicore
           vulnerability reported to the software providers
2013-01-28 Fixed in EMI 2 Update 8
2013-06-12 Updated packages available EGI UMD-2
2013-08-19 After checking 'Low' risk issues, found fixed in UMD.
2012-09-16 Public disclosure
```
