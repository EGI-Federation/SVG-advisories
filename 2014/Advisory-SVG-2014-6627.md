---
title: SVG:Advisory-SVG-2014-6627
---

```
** WHITE information - Unimited distribution **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-6627]

Title:   EGI SVG Advisory 'High' RISK - CVE-2013-4495 Torque Vulnerability:
         arbitrary code execution via job submission [EGI-SVG-2014-6627]
         **UPDATE**

Date:    2014-01-24
Updated: 2014-02-21, 2014-03-27 (made public)


URL:     https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-6627

Introduction
============

A vulnerability in Torque has been made public which allows a user to execute
arbitrary code as root.

**UPDATE** a patched version of Torque for SL5 and SL6 has been made available
in the EGI AppDB part  of the UMD.  This resolves all known vulnerabilities and
works with APEL.

The previous advisory provided a mitigation suggestion which protected sites
until a better solution became available.


Details
=======

A vulnerability has been found which enables a user to execute arbitrary code
as root.
This has been fixed by the Torque providers. [R 1]

Information on this vulnerability has been made public at [R 2]

This has been given CVE-2013-4495 [R 3]

The versions produced by the Torque providers do not solve all known
vulnerabilities, and some versions of Torque do not work with APEL.

A version has been produced by the EGI SVG in the SVG area of the AppDB area of
the EGI UMD which contains no known vulnerabilities and works with APEL.

Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment Team

Affected software
=================

Versions of Torque earlier than 4.2.6 are affected by this vulnerability.

The latest version (21st February 2014)  in the SVG AppDB area of the EGI UMD
has no known vulnerabilities.


Mitigation
==========


Sites may protect themselves from this vulnerability by disabling the embedded
mail by setting the server

qmgr -c 'set server mail_domain = never'



Component installation information
==================================


A version of Torque is provided in the AppDB area of the UMD solves all
currently known problems.

https://appdb.egi.eu/store/software/software.vulnerability.group/releases/torque/

This is available for el5, el6 and its derivatives, and should be suitable for
most sites.

Limited support on a best efforts basis is provided by the EGI SVG, and support
is not guaranteed in the future.



Recommendations
===============

If sites are running Torque and have not previously carried out mitigating
action, i.e. disabled the embedded mail as described above, they should either
carry out mitigating action, or better still update to the version in the SVG
AppDB area of the EGI UMD



Other information
==================

Torque Version 4.2.6 which solves this problem is available from adaptive
computing a lso has one of the 'high' risk vulnerabilities described in the
advisory [SVG-2013-5999] resolved, but it is not clear at present whether all
problems are solved.

Some versions of Torque do not work with the EGI accounting system, APEL, but
the version in the EGI AppDB area does.

Credit
======

SVG was alerted to this problem by Leif Nixon.

Fixed/non-vulnerable version of Torque produced and tested by Eygene Ryabinkin.

Version placed in SVG AppDB area of the EGI UMD by Mischa Salle.


References
==========

[R 1] https://www.adaptivecomputing.com/wp-content/uploads/releasenotes/releaseNotes-4.2.6.html

[R 2] Red Hat bugzilla https://bugzilla.redhat.com/show_bug.cgi?id=1026910

[R 3] http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2013-4495



Timeline
========
Yyyy-mm-dd

2013-11-?? Vulnerability found and fixed by adaptive computing?
2013-11-20 Vulnerability Announced in the National Vulnerability Database
2014-01-21 SVG alerted to vulnerability by Leif Nixon, as it was public.
2014-01-22 Acknowledgement of Leif by SVG
2014-01-23 SVG actively carrying out risk assessment, and deciding on strategy
2014-01-24 Interim advisory issued, alerting sites and suggesting mitigating
           action.
2014-02-20 Non vulnerable version available in the SVG AppDB area of the UMD.
2014-02-20 Assessment by the EGI Software Vulnerability Group reported.
2014-02-21 Updated advisory sent to sites.
2014-03-27 Public disclosure
```
