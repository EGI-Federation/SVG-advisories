---
title: SVG:Advisory-SVG-2014-7372
---

```
** WHITE information - unlimited distribution                               **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-7372]

Title:    EGI SVG Advisory 'HIGH' RISK - Buffer Overflow Vulnerability in
          xrootd-server-atlas-n2n-plugin  for ATLAS FAX sites - N2N xrootd
          service [EGI-SVG-2014-7372]

Date:     2014-09-11
Updated:

URL:      https://wiki.egi.eu/wiki/Advisory-SVG-2014-7372

Introduction
============

A buffer overflow bug was found in the ATLAS VO's 'name-to-name' library that's
used on site's SE head nodes as part of the xrootd federated redirection system
(FAX).

This has been fixed and announced as a bug fix to the
atlas-adc-federated-xrootd@cern.ch mailing list.

EGI SVG and CSIRT consider this to be a software vulnerability, and is treating
it as such and advising sites to update as soon as possible if they have not
done already.


Details
=======

This problem was discovered when a user launched jobs that use a malformed ROOT
url, these jobs crashed many FAX sites. This was not of course a malicious act
but provided awareness of this problem which was due to a buffer overflow.

This has been fixed.

The bug was in the xrootd-server-atlas-n2n-plugin.

This constitutes a vulnerability because a malicious user could intentionally
crash sites, also it is possible that an exploit may be developed which allows
a more serious attack.



Risk category
=============

This issue has been assessed as 'High' risk at present by the EGI CSIRT and
EGI SVG Risk Assessment Team.

Note that if an exploit is found which allows more serious consequences other
than crashing the service it is likely to be elevated to 'Critical' risk.


Affected software
=================

This is fixed in the xrootd-server-atlas-n2n-plugin-2.0-5

All versions earlier than this are likely to be vulnerable.


Mitigation
==========

N/A. Sites should install update.


Component installation information
==================================

The fixed version of this software is available in the WLCG repro

http://linuxsoft.cern.ch/wlcg

xrootd-server-atlas-n2n-plugin

Sites should restart their services after installing the updated module.


Recommendations
===============

Sites are recommended to update relevant components as soon as possible,
if they have not done so already.


Other information
=================

Further examination and improvement to the code is being currently being
carried out, in order to ensure that there are no further vulnerabilities.


Credit
======

This vulnerability was reported to SVG by David Groep from Nikhef.



Timeline
========
Yyyy-mm-dd

2014-08-29 Vulnerability reported by David Groep - after announcement as a bug
           fix.
2014-08-29 Acknowledgement from the EGI SVG to the reporter
                       Various discussions on Risk.
2014-09-08 Agreed to be a 'High' risk vulnerability at EGI IRTF meeting
2014-09-11 Advisory sent to sites, to inform that it is a high risk
           vulnerability, and not just a bug.
2014-09-29 Public disclosure
```
