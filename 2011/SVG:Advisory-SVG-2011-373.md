---
title: SVG:Advisory-SVG-2011-373
permalink: /SVG:Advisory-SVG-2011-373/
---

```


** WHITE information - Unlimited distribution allowed                       **

** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-20110311]

Title:  SQL injection vulnerability in the APEL software
Date:

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-373

Introduction
============

The EGI Software vulnerability group has been alerted to a vulnerability in the APEL server.
This vulnerability has been eliminated from the software, and installed on the APEL server.
As there is only 1 instance of the APEL server, and the client is unaffected, no action needs
to be taken by sites.


Details
=======

APEL is used for accounting in the EGI environment. An SQL injection vulnerability has been
found in the APEL server software. Depending on the target SQL database engine and its version,
injection can result in reading of arbitrary files at the server, command injection and even
execution of arbitrary code.

Risk Category
=============

This issue has been assessed as 'Moderate' risk by the  EGI SVG Risk Assessment Team.


Affected Software
=================

The APEL accounting software server.


Mitigation
==========

Not applicable


Component Installation information
==================================

As only one instance of the APEL server is installed which has already been updated,
sites do not need to take any action.

Recommendations
===============

No action needs to be taken, this is for information only.


Credit
======

This vulnerability was reported by Romain Wartel


References
==========



(Note - some delay from SVG side - as this was the first issue handled with EGI process)

========
Yyyy-mm-dd

2010-10-04 Vulnerability reported by Romain Wartel
2010-10-04 Acknowlegement from the EGI SVG to the reporter
2010-10-13 Software providers responded and involved in investigation
2010-10-22 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2011-02-03 Server updated by APEL team.
2011-03-11 Public disclosure




On behalf of the EGI SVG,
```