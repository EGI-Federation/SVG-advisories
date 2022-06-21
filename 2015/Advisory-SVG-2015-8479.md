---
title: Advisory-SVG-2015-8479
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2015-8479]

Title:   EGI SVG Advisory 'High' RISK - perfSONAR potential for a remote root
         exploit (in non-recommended configuration)   [EGI-SVG-2015-8479]

Date:    2015-05-07
Updated: 2015-05-27


URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2015-8479


Introduction
============

A vulnerability has been found in fakewww, which is part of the NDT package,
which in turn is part of perfSONAR, which could potentially lead to a remote
root exploit.

This has been fixed in NDT version 3.7.0 which is part of perfSONAR 3.4.2 and
sites should make sure they have auto-updates enabled as recommended or update
manually.

If sites are configured as recommended by the WLCG perfSONAR team, in [R 1],
with NDT disabled, then they are not vulnerable even if they are running a
vulnerable version of perfSONAR.

However, it is not clear how many sites in the EGI or WLCG environment are
configured such that NDT is not disabled.

Sites running perfSONAR are asked to check they do not have a vulnerable
configuration and take action if necessary.


Details
=======

The potential for a remote exploit has been found in in fakewww, which is part
of the NDT package, which in turn is part of perfSONAR.
If sites are configured as recommended by the perfSONAR team, with NDT
disabled, then they are not vulnerable.  See [R 1]

It is not clear how many sites are vulnerable, the tools which CSIRT normally
uses for checking for vulnerabilities cannot be used to check for this.

This has been fixed in NDT version 3.7.0 which is part of perfSONAR 3.4.2 and
sites should make sure they have auto-updates enabled as recommended or update
manually.


Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment Team.

Affected software
=================

All versions of perfSONAR running NDT version prior to 3.7.0 are vulnerable.

If NDT is disabled as recommended, then sites are not vulnerable.


Mitigation
==========

Sites running perfSONAR should check that NDT is disabled as recommended and if
it is not disabled either update urgently or disable NDT.


Component installation information
==================================

Please see the perfSONAR wiki instructions [R 1]


A “yum update” will mitigate this security problem with no other steps needed.

However, for those who do not trust fakewww and prefer to  use Apache instead,
doing a “yum install ndt-server-apache” would switch NDT to use Apache.
It is necessary to install package 'ndt-server-apache' using yum,
and run "service ndt restart" and "service httpd restart".




Recommendations
===============

Sites running perfSONAR should check that NDT is disabled as in instructions in
[R 1]

Sites should also check that they are running the latest version of NDT (3.7.0)
and preferably (as recommended by the perfSONAR team) have auto-updates
enabled.


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London

References
==========

[R 1] https://twiki.opensciencegrid.org/bin/view/Documentation/InstallUpdatePS

Timeline
========

Yyyy-mm-dd

2015-04-18 Vulnerability reported by Simon Fayer (a member of SVG)
2015-04-22 Software providers responded and involved in investigation
2015-04-30 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2015-05-01 Updated packages available at perfSONAR website
2015-05-07 Advisory sent to sites
2015-05-27 Public disclosure
```
