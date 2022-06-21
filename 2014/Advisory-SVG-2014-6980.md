---
title: Advisory-SVG-2014-6980
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-6980]

Title:   EGI SVG Advisory 'Low' RISK - CREAM Proxy delegation
         [EGI-SVG-2014-6980]

Date:    2015-10-12
Updated:

URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2014-6980


Introduction
============

A vulnerability has been found in CREAM (Computing Resource Execution And
Management) job management software [R 1] where a full proxy is delegated to
CREAM instead of a limited proxy.

This was resolved some time ago and updates are available in the EGI UMD.

Details
=======

When a full proxy is delegated to CREAM instead of a limited proxy, it means
that if CREAM were to be compromised then an attacker could impersonate all
users whose proxies are on that CREAM instance.  Although this is not
exploitable by itself, it could make a CREAM compromise a much larger problem
to deal with as potentially a large number of users would need to have their
certificates revoked and re-issued.


Risk category
=============

This issue has been assessed as "Low" risk by the EGI SVG Risk Assessment Team.


Affected software
=================


CREAM all versions prior to version 1.16.4


Mitigation
==========

N/A

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/



Sites who wish to install directly from the EMI release should see:

http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/

This is fixed in EMI-3 Update 21.

http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/-/asset_publisher/5Na8/content/update-21-09-10-2014-v-3-12-0-1

Note that in order to ensure that the client software is correct it is
necessary to explicity carry out

yum install voms-clients3

or one will get the voms-clients version 2.


Recommendations
===============


Sites are recommended to update components in due course if they have not done
so already.


Other information
=================

As this was fixed a long time ago, and it is likely that most sites are up to
date as well as being 'Low' risk this is put on the wiki only.


Credit
======

This vulnerability was reported by Mischa Salle from Nikhef


References
==========

[R 1] http://grid.pd.infn.it/cream/




Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

We are currently revising the vulnerability issue handling procedure so
suggestions and comments are welcome.



Timeline
========
Yyyy-mm-dd

2014-05-08 Vulnerability reported by Mischa salle
2014-05-09 Acknowledgement from the EGI SVG to the reporter
2014-05-09 Software providers responded and involved in investigation
2014-05-09 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2015-02-16 Updated packages available in the EGI UMD
2015-12-16 Public disclosure on SVG wiki.
```
