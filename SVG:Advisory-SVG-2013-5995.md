---
title: SVG:Advisory-SVG-2013-5995
permalink: /SVG:Advisory-SVG-2013-5995/
---

```


** WHITE information - Unlimited distribution allowed                       **

** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2013-5995]

Title:       *No action required* EGI SVG Advisory 'Low' RISK - CREAM DoS vulnerability [EGI-SVG-2013-5995]

Date:        2015-08-20
Updated:

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2013-5995


Introduction
============

A vulnerability has been found in CREAM (Computing Resource Execution And Management) job management software.  [R 1]

A vulnerability assessment (The active investigation of software for vulnerabilities)
of CREAM was carried out by the Autonomous University of Barcelona in 2013, 4 vulnerabilities were initially found,
which were resolved in early 2014. A 5th vulnerability was later found which has proven more difficult to resolve.

This will not be resolved.

Details
=======

This vulnerability is a DoS but only exploitable by a user who has valid user submission credentials on the target CE.

An exploit has been written to prove it is possible to cause a DoS.

It has proven difficult to resolve this while keeping CREAM's functionality without a complete redesign of a subsystem
of the service. Since the DoS can be carried out only by an authorized user exploit is considered unlikely.

Therefore it has been decided NOT to fix this but to inform sites.


Risk category
=============

This issue has been assessed as "Low" risk by the EGI SVG Risk Assessment Team.


Affected software
=================

CREAM all versions.


Mitigation
==========

N/A



Recommendations
===============

No action is recommended.



Credit
======

This vulnerability was reported by Elisa Heymann, Joe Carrion, and Manuel Brugnoli after the Vulnerability
Assessment work they carried out on CREAM


References
==========

[R 1] http://grid.pd.infn.it/cream/




Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

We are currently revising the vulnerability issue handling procedure so suggestions and comments are welcome.



Timeline
========
Yyyy-mm-dd

2013-09-05 Vulnerability reported by Manuel Brugnoli, Joe Carrion, and Elisa Heymann
2013-09-05 Acknowledgement from the EGI SVG to the reporter
2013-09--- Software providers responded and involved in investigation
2013-09-13 Assessment by the EGI Software Vulnerability Group reported to the software providers
2014-08-05 Software providers reported that the fix implemented caused problems and could not be released
2015-08-19 Decision not to attempt to fix this issue.
2015-08-20 Advisory sent to sites.
```