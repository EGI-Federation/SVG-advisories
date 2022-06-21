---
title: Advisory-SVG-2017-12543
---

```
Title:   EGI SVG ADVISORY [TLP:WHITE] 'CRITICAL' risk vulnerability concerning
         VOMS Admin [EGI-SVG-2017-12543]

Date:    2017-03-20
Updated: 2017-03-27, 2017-07-04

Affected software and risk
==========================

CRITICAL risk vulnerability concerning VOMS Admin.

Package : VOMS Admin

Various vulnerabilities have been found concerning voms-admin.
These include the ability for a user to gain privileged (but not root) access.

Actions required
================

Sites running VOMS Admin are required to urgently install version 3.6.0.

All running resources MUST be either patched or have mitigation in place or
software removed by 2017-04-04  00:00 UTC

Sites failing to act and/or failing to respond to requests from the EGI CSIRT
team risk site suspension.


Affected software details
=========================

This is fixed in VOMS Admin 3.6.0

All VOMS versions prior to this release are affected.

VOMS Admin versions >= 3.4.0 and < 3.5.2 are vulnerable to unauthenticated
attacks.

VOMS Admin v. < 3.4.0 allow the attack only to authenticated clients.


More information
================

These vulnerabilities are publicly known vulnerabilities in Apache Struts, on
which VOMS admin depends.

In the case where VOMS admin >= 3.4.0 and < 3.5.2 an unauthenticated user is
able to exploit this vulnerability and gain privileged access.

Most sites running VOMS have already installed VOMS Admin 3.5.2 to block
unauthenticated attacks.

Mitigation
==========

Mitigation is possible by restricting access to port 8443 to only known,
trusted hosts.

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

Fixed version is in UMD 4.4.1

http://repository.egi.eu/2017/03/24/release-umd-4-4-1/

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Fixed version is in UMD 3.14.9

http://repository.egi.eu/2017/03/24/release-umd-3-14-9/


Sites wishing to install directly from the VOMS site should see

http://italiangrid.github.io/voms/2017/03/23/voms-release-17-03-23.html

TLP and URL
===========

** WHITE information - Unimited distribution - see
https://go.egi.eu/tlp for distribution restrictions **

An advisory will be placed on the wiki after sites have had at least 2 weeks to
upgrade.

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2017-12543

After that, minor updates may be made without re-distribution to the sites


Comments
=========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]


References
=========


[R 1] https://documents.egi.eu/public/ShowDocument?docid=2538

Credit
=====

This vulnerability was reported by Vincenzo Ciaschini


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-12543]

2017-03-15 Vulnerability reported by Vincenzo Ciaschini
2017-03-15 Acknowledgement from the EGI SVG to the reporter
2017-03-15 Software providers responded and involved in investigation, and
           developing a fix
2017-03-16 EGI SVG Risk Assessment completed
2017-03-16 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2017-03-20 Interim version of VOMS admin available which blocks unauthenticated
           exploit
2017-03-20 CSIRT sent alert to sites running VOMS admin to install interim
           version, where applicable.
2017-03-27 Updated packages available
2017-03-27 Advisory/Alert sent to sites
2017-07-04 Public disclosure - changed to TLP WHITE


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1]
in the context of how the software is used in the EGI infrastructure.
It is the opinion of the group, we do not guarantee it to be correct.
The risk may also be higher or lower in other deployments depending on how the
software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group


On behalf of the EGI SVG,
```
