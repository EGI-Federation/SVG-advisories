---
title: Advisory-SVG-2015-8056
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2015-8056]

Title:   EGI SVG Advisory 'High' RISK - CVE-2015-1195 OpenStack for
         [EGI-SVG-2015-8056]

Date:    2015-02-11
Updated:

URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2015-8056

Introduction
============

A vulnerability has been announced in OpenStack Image service (glance) which
allows authorized users to access and delete files accessible by the glance
user.

Sites running OpenStack are recommended to update as soon as possible if they
have not already done so.


Details
=======

Details are available in [R 1], [R 2], [R 3]


Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment Team.


Affected software
=================

V2 API in OpenStack Image Registry and Delivery Service (Glance) before
2014.1.4 and 2014.2.x before 2014.2.2


Mitigation
==========

N/A


Component installation information
==================================

In Juno (2014.2) the fix has been included in the 2014.2.2 release
(https://wiki.openstack.org/wiki/ReleaseNotes/2014.2.2) therefore sites should
update all the glance packages to the 2014.2.2 version.

In Icehouse (2014.1) the fix be included in the 2014.1.4 release, planned for
February 19th.
A patch may be made available sooner, and the version of this advisory on the
wiki will be updated if it is.


Recommendations
===============

Sites are recommended to update relevant components if they have not done so
already.

Once the update is complete, all the credentials accessible by the glance user
(e.g. OpenStack service username and password, MySQL connection details, etc.)
should be revoked as a precautionary measure.


Credit
======

This vulnerability was announced publicly and EGI SVG alerted to it by Alvaro
Lopez Garcia


References
==========

[R 1] https://github.com/openstack/ossa/blob/master/ossa/OSSA-2015-002.yaml

[R 2] http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2015-1195

[R 3] http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-1195


Timeline
========

Yyyy-mm-dd

2015-01-15 Vulnerability announced publicly
2015-01-27 EGI SVG alerted by Alvaro Lopez Garcia
2015-01-30 Risk Assessment by the EGI Software Vulnerability Group.
2015-02-11 Advisory sent to sites
```
