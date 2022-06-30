---
title: Advisory-SVG-2015-9707
permalink: /Advisory-SVG-2015-9707
---

## Advisory-SVG-2015-9707

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2015-9707]

Title:       EGI SVG Advisory - Various Java CVE's with max CVSS score.

Date:        2015-10-29
Updated:     2015-11-26


URL:         https://advisories.egi.eu/2015/Advisory-SVG-2015-9707

Introduction
============

Various vulnerabilities have been publicly announced concerning Java, some of
which have the maximum CVSS (Common Vulnerability Scoring System) score of 10,
but details including the attack vectors are not specified.

We cannot determine the exact effect these vulnerabilities may have in EGI from
the information currently available.

Since they have high CVSS scores if and when information becomes available
publicly there is a fair chance that updating will become urgent, so we are
recommending that sites update in the coming days.

**UPDATE**

Updates are now available resolving these for SL5, SL6 and SL7 [R 3]

We have no further informaiton on these vulnerabilities.


Details
=======

Scientific Linux announced 'critical' updates concerning openjdk listing 17
CVE's [R 1]

1 example of a CVE with CVSS score of 10 [R 2]

It would appear that all sources of java (from Oracle and OpenJDK) were
vulnerable, but fixes are available for most Operating systems.


Risk category
=============

It is not possible to establish the risk category for EGI as insufficient
details o f the vulnerabilities have been released.  However, since the CVSS
score is the maximum of 10 for some of them, there is a fair chance that some
may be considered at least 'high risk' in the EGI environment if and when
public information and public exploits become available.


Affected software
=================

It would appear that this issue affects multiple versions of Java 6, Java 7 and
Java 8.

Versions of Java provided with Scientific Linux, Debian and Ubuntu are stated
as being affected.

See OS provider for more details.

**UPDATE**

Scientific Linux has issued updates to resolve these vulnerabilities for SL5,
SL6 and SL7.  See [R 3]



Component installation information
==================================

See appropriate OS provider sites.


Recommendations
===============

Sites are recommended to update to a non-vulnerable version of OpenJDK in the
coming days if they have not done so already.


Credit
======

SVG was alerted to this by Ian Neilson

References
==========

[R 1] https://www.scientificlinux.org/sl-errata/slsa-20151920-1/

[R 2] https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2015-4883

[R 3] https://www.scientificlinux.org/sl-errata/slsa-20152086-1/

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

We are currently revising the vulnerability issue handling procedure so
suggestions and comments are welcome.



Timeline
========
Yyyy-mm-dd

2015-10-21 Scientific Linux announced java-1.7.0-openjdk security update
2015-10-26 Ian Neilson alerted SVG to the Scientific Linux security
           announcement
2015-10-27 SVG decided to send an advisory to sites recommending updating
2015-10-29 Advisory sent to sites
2015-11-26 Update as scientific linux has provided patches.
```
