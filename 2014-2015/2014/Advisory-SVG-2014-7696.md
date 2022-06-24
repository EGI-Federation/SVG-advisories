---
title: Advisory-SVG-2014-7696
---

```
** WHITE information - unlimited distribution                               **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2014-7696]

Title:   EGI SVG Advisory 'High' risk FTS3 and GFAL2 allow attacker to
         impersonate other users and destroy their data [EGI-SVG-2014-7696]

Date:    2014-12-08
Updated: 2014-12-10

This advisory will be placed on the wiki on or after 2014-12-22

URL:     https://advisories.egi.eu/2014/Advisory-SVG-2014-7696

Introduction
============

2 vulnerabilities have been found concerning FTS3 and GFAL2 which allow an
authorized user to access, write, and delete files with other authorized users
credentials.

These vulnerabilities have been fixed in the versions of FTS3 and GFAL2
available for use in the EGI infrastructure.

Updated 10th December 2014 - clarify difference in cases where FTS3 server is
running and where only GFAL is running.


Details
=======

2 vulnerabilities have been found concerning FTS3 and GFAL2.

These allow an authorized user to attack and destroy other user's data, and
remove traces of what they have done.

1. The vulnerability that affects FTS3 allows an attacker *with valid
   credentials* to delete or submit files with any other user credentials (e.g.
   trigger a transfer or a deletion using ATLAS or LHCb delegated credentials)

2. The vulnerability that affects GFAL2 allows an attacker *with valid
   credentials* that controls an endpoint *with a valid certificate* to trigger
   a transfer copying any local file that FTS3 can read to a remote storage.
   This includes user's proxies and the server certificate and private key,
   among others.  This attack cannot be detected unless debug output was
   enabled for the offending job, which is unlikely.


Risk category
=============

These issues have been assessed as 'High' risk by the EGI SVG Risk Assessment
Team This is considered the more serious end of 'High'.

Affected software
=================

Fixed in FTS 3.2.30

earlier versions are likely to be vulnerable.


Fixed in GFAL 2.8 and backported to GFAL 2.7.8.

earlier versions are likely to be vulnerable.

Mitigation
==========

N/A.


Component installation information
==================================

Non vulnerable versions of FTS3 and GFAL may obtained from:--

http://grid-deployment.web.cern.ch/grid-deployment/dms/fts3/repos/el6/x86_64/

GFAL is available in EPEL

https://fedoraproject.org/wiki/EPEL

(FTS3 is also in EPEL testing)

Recommendations
===============

Updated 10th December 2014

Sites running FTS servers should update urgently if they have not already done
so.

Other sites should install the fixed GFAL package as part of normal routine
updates.


Other information
=================

Added 10th December 2014

We have had some requests for further information concerning the use of GFAL2
on nodes other than FTS servers.

We have discussed further with the software providers, the UKNGI security team,
and the SVG found that:--

1) In the case of an FTS3 server, the vulnerability is serious as described
above, and sites should update both the FTS3 package (to at least 3.2.30-1) and
the GFAL2 package (to at least 2.7.8-1) urgently.

2) For other node types with the GFAL2 clients installed (e.g. Worker Nodes and
UIs), it is less serious and requires quite a contrived situation to exploit.
So we recommend installing the fixed GFAL2 package as part of normal routine
updates.

Finally, GFAL 2.8 is expected to be released in February, but we would still
suggest that sites install the fixed 2.7.8-1 release in the interim, rather
than waiting.


Credit
======

These vulnerabilities were reported by Alejandro Alvarez Ayllon from the FTS3
product team at CERN.

Timeline
========
Yyyy-mm-dd

2014-11-18 Vulnerability reported by Alejandro Alvarez Ayllon from the product
           team
2014-11-18 Acknowledgement from the EGI SVG to the reporter
2014-11-20 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2014-12-04 Discussion on advisory and updates 2014-12-?? Updated packages
           available
2014-12-08 Advisory sent to sites.
2014-12-10 Updated advisory sent
2015-01-15 Public disclosure
```
