---
title: SVG:Advisory-SVG-2011-1870
permalink: /SVG:Advisory-SVG-2011-1870/
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-20110609]

Title:   Advisory for 'Moderate' Risk Torque Server Buffer Overflow
         Vulnerability - CVE- 2011-2193.
Date:    2011-06-09
Updated: 2011-06-23


URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-1870


Introduction
============


A buffer overflow vulnerability has been found in the Torque server. This was
reported to the EGI SVG (RT 1870) as well as to the Torque software providers.

This has been fixed by the Torque Providers, and an updated version is also
available in EPEL.


This has also been assigned vulnerability CVE-2011-2193


Details
=======

Many EGI Sites use Torque (Tera-scale Open source Resource Manager and QUeue
manager) as distributed as part of EPEL.

A buffer overflow vulnerability has been found in the Torque server. So far an
exploit has been found which allows the attacker to crash a server, but no
exploit has been found which allows an attacker to manipulate the buffer
overflow to cause specific behaviour.

This was reported to the EGI SVG (RT 1870) as well as to the Torque software
providers.
This has been fixed by the Torque providers.

The updates have also been applied to EPEL.


Risk Category
=============

This issue has been assessed as 'Moderate' risk by the  EGI SVG  Risk
Assessment Team.


Affected Software
=================

Versions of Torque prior to Torque 2.4.14


Mitigation
==========

Not applicable


Component Installation information
==================================


For sites using EPEL, the patch has been applied to:

torque-2.3.13-2.el5

torque-2.3.13-2.el4

compatible with RHEL 4 and 5 available from EPEL.


Recommendations
===============

The EGI SVG recommends that sites update the software, using the new version in
the EPEL, or directly from the Torque suppliers.


Credit
======

This vulnerability was reported by Bartlomiej Balcerek,  Maciej Kotowicz, and
Adam Zabrocki of the Wroclaw Centre for Networking and Supercomputing Security
Team.


References
==========

CVE assignment:
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-2193

RH bug:
https://bugzilla.redhat.com/show_bug.cgi?id=711463

RH release for SL5:
https://admin.fedoraproject.org/updates/torque-2.3.13-2.el5


Cluster resources ref.
http://www.clusterresources.com/pipermail/torqueusers/2011-June/012982.html


Timeline
========

Yyyy-mm-dd

2011-05-10 Vulnerability reported to SVG by Bartlomiej Balcerek, in addition to
           reporting to software providers.
2011-05-10 Acknowledgement from the EGI SVG to the reporter
2011-06-06 Software provider states issue fixed.
2011-06-07 Bug subitted in RH EPEL, as EGI mostly uses EPEL distribution
2011-06-22 Updated packages formally released in EPEL
2011-06-24 Public disclosure by the EGI SVG
```
