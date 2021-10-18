---
title: SVG:Advisory-SVG-2014-6884
permalink: /SVG:Advisory-SVG-2014-6884/
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG  ADVISORY [EGI-SVG-2014-6884]

Title:   EGI SVG Advisory 'CRITICAL' RISK - WN and UI tarballs in the EMI
         repository contain a version of OpenSSL vulnerable to CVE-2014-016
         [SVG EGI-SVG-2014-6884]

Date:    2014-04-10
Updated:


URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-6884

Introduction
============

EGI CSIRT has already issued an alert concerning CVE-2014-0160 for the OpenSSL
Heartbleed vulnerability [R 1] on 8th April 2014 with updates on 9th April
2014.

This advisory concerns a specific occurance of the vulnerable version of
OpenSSL in the EMI-3 repository.

It is only relevant to sites who install the EMI WN or the UI from tarballs
provided in the EMI repository.

It is also only relevant to sites who include the 'os-extras' along with the WN
and/or glite UI tarball.


Details
=======

EGI CSIRT has already issued an alert concerning CVE-2014-0160 for the OpenSSL
Heartbleed vulnerability [R 1] on 8th April 2014 with updates on 9th April
2014.

A vulnerable version of OpenSSL has since been found in the EMI repository.

This has been replaced by a non-vulnerable version.

Sites which use the WN and/or UI tarballs present in the EMI respository may
have a vulnerable version on their systems downloaded from the EMI repository.

This separate advisory is considered necessary to inform sites that a
vulnerable version of OpenSSL WAS in  the EMI repository, but has been replaced
by a non-vulnerable version.

Whether sites get their OpenSSL from the EMI repository or elsewhere they need
to ensure they are not running a vulnerable version.


Risk category
=============

This issue has been assessed as 'Critical' risk by the EGI CSIRT and EGI SVG
Risk Assessment Team. This has been previously reported.


Affected software
=================

Tarballs for the gLite WN and UI available in the EMI repository for SL6.

The vulnerable version of OpenSSL was found in:--

emi-wn-3.7.1-1_v2.sl6 and
emi-ui-3.7.1-1_v2.sl6

This is fixed in version:--

emi-wn-3.7.3-1_v1.sl6 and
emi-ui-3.7.3-1_v1.sl6

Earlier versions may also be vulnerable.

Note that SL5 versions are not affected.


Mitigation
==========

N/A.


Component installation information
==================================

The fixed versions are as follows:


Sl6 WN:
http://repository.egi.eu/mirrors/EMI/tarball/test/sl6/emi3-emi-wn/emi-wn-3.7.3-1_v1.sl6.tgz
http://repository.egi.eu/mirrors/EMI/tarball/test/sl6/emi3-emi-wn/emi-wn-3.7.3-1_v1.sl6.os-extras.tgz


SL6 UI:
http://repository.egi.eu/mirrors/EMI/tarball/test/sl6/emi3-emi-ui/emi-ui-3.7.3-1_v1.sl6.tgz
http://repository.egi.eu/mirrors/EMI/tarball/test/sl6/emi3-emi-ui/emi-ui-3.7.3-1_v1.sl6.os-extras.tgz

Only sites that use the "os-extras" from this repository will have the
vulnerable OpenSSL downloaded from the EMI repository in their tarball area
from this source.
Others will need to upgrade OpenSSL if they have not done so anyway.


For further information see the Tarball wiki page [R 2]


You may also contact the Tarball support list tarball-grid-support@cern.ch
if you have any questions.



Recommendations
===============

All running resources MUST be either patched or otherwise temporarily removed
from service as soon as possible, and at the latest by by 2014-04-15
T21:00+01:00.
Sites failing to act and/or failing to respond to requests from the EGI CSIRT
team risk site suspension.

This is considered to be part of the same campaign to eliminate CVE-2014-0160
as described in [R 1].


Credit
======

SVG alerted to the vulnerable version of OpenSSL being present in the EMI
repository by Matt Doidge, who also resolved this.


References
==========

[R 1] https://wiki.egi.eu/wiki/EGI_CSIRT:Alerts/OpenSSL-2014-04-08

[R 2] https://www.sysadmin.hep.ac.uk/wiki/EMI3Tarball#Downloading


Timeline
========
Yyyy-mm-dd

2014-04-09 SVG alerted to this problem by Matt Doidge.
2014-04-09 Acknowledgement from the EGI SVG to the reporter
2014-04-09 It was decided as it concerns middleware SVG should issue a
            separate advisory to the general one concerning OpenSSL.
2014-04-10 Software providers (also Matt Doidge) provided a new version.
2014-04-10 Advisory issued
2014-04-10 Public disclosure
```
