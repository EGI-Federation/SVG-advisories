---
title: SVG:Advisory-SVG-2016-11476
---

```
Title:   EGI SVG Advisory 'CRITICAL' risk - gridsite impersonation
         vulnerability [EGI-SVG-2016-11476]

Date:    2016-09-21
Updated: 2016-10-10 - changed to 'white'


Affected software and risk
==========================

CRITICAL risk vulnerability concerning gridsite /canl-c

Package : canl-c
CVE ID  : N/A

A vulnerability has been found in the canl-c library which is used by gridsite
where it is possible for a user with any certificate, including a self-created
one, to impersonate any other user. This is present in all recent versions of
gridsite up to version 2.2.5, and all versions of canl-c up to and including
2.1.6.

Actions required/recommended
============================

Sites running gridsite/canl-c are required to urgently install updates.

Please ensure all potentially affected services are restarted after the update.
In particular for the DPM, FTS, and LFC:

     service httpd restart


All running resources MUST be patched or software removed by 2016-09-29  00:00
UTC

Sites failing to act and/or failing to respond to requests from the EGI CSIRT
team risk site suspension.


Affected software details
=========================

This is fixed in caNl-c version 2.1.7-1. Earlier versions are all likely to be
affected.

Affected software dependent on this include:--

anything which depends on Gridsite

DPM

LFC

FTS - but only in limited circumstances.

WMS - ditto

Also the CREAM CE uses GridSite, but it turns out not to be affected.


More information
================

The reporter recently discovered a security vulnerability in gridsite, through
which it is possible to impersonate any user with the help of a
specially-crafted proxy.

The error was found to be in the caNl-c software, on which gridsite depends.

This vulnerability is exploitable in cases where authorization is dependent on
DN only, using caNl-C, and the attacker has created a specially crafted
certificate.

The services most affected are DPM and LFC. For these services an attacker can
impersonate any user of any VO supported by that service, though only with an
unprivileged role. Privileged roles generally require authorization via VOMS.

For The DPM and LFC this would give read and/or write access according to the
ACLs for the files and directories of the chosen VO. For example, the
impersonated user could have access to a group-writable area and delete or
modify data of other users.

FTS is also affected in a less extensive manner.


Mitigation
==========

N/A

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

Further information including links to detailed release notes are available
from

https://wiki.egi.eu/wiki/UMD-4:UMD-4.2.1


Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Further information including links to detailed release notes are available
from

https://wiki.egi.eu/wiki/UMD-3:UMD-3.14.4


Sites who wish to install directly from the github site should see:

https://github.com/CESNET/canl-c/wiki/caNl-c-Release-Page#caNlc_2171


TLP and URL
===========

** WHITE information -Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2016-11476

Minor updates may be made without re-distribution to the sites

Credit
======

This vulnerability was discovered and reported by Georgios Bitzes from CERN.

Extensive testing and work to resolve this issue carried out by Daniel Kouril,
Maarten Litmaath, Georgios Bitzes, Andrea Ceccanti and others.

References
==========



Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-11476]

2016-08-17 Vulnerability reported by Georgios Bitzes from CERN
2016-08-17 Acknowledgement from the EGI SVG to the reporter
2016-08-17 Software providers responded and involved in
           investigation/resolution
2016-08-22 EGI SVG Risk Assessment completed
2016-08-22 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2016-08-22 Software fix produced and tested
2016------ Some issues with verification/release
2016-09-21 Updated packages available in the EGI UMD
2016-09-21 Advisory/Alert sent to sites
2016-10-10 Public disclosure



On behalf of the EGI SVG,
```
