---
title: SVG:Advisory-SVG-2014-7191
permalink: /SVG:Advisory-SVG-2014-7191/
---

```

** WHITE information - unlimited distribution                               **

** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2014-7191]

Title:       EGI SVG Advisory "High" Risk  CVE-2014-5261,  CVE-2014-5262
            Cacti remote command and code execution vulnerabilities - relevant to sites running Perfsonar.

Date:        2014-12-01
Updated:

This will be placed on the wiki on or after 15th December 2014.

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-7191


Introduction
============

Two vulnerabilities were found in Cacti by a member of the EGI software vulnerability group.

The only place in the EGI infrastructure where cacti is in use that we are aware of is sites running
Perfsonar.

This advisory is to alert sites to this, and suggest sites check that suitable mitigation is in place,
as recommended by the perfsonar team.

Fixes are available for this particular cacti issue for debian, but not redhat.

The two vulnerabilities have CVEs assigned CVE-2014-5261 [R 1], CVE-2014-5262 [R 2]


Details
=======

For the description of the cacti vulnerabilities see [R 1] and [R 2]


Risk category
=============

These vulnerabilities have both been assessed as 'High' risk by the EGI SVG Risk
Assessment Team, if sites are configured badly.


Affected software
=================

These are fixed in debian, see [R 3], [R 4]

For RedHat they have not yet been fixed.
The upstream release fixing these issues is cacti-0.8.8c



Mitigation
==========

Sites can mitigate cacti problems by doing both of the following:

- put behind firewall/only trusted people should be able to access the  webfrontend
- remove the line
 $guest_account = true;
 from the top of graph_settings.php


Sites running perfsonar should ensure that they are configured correctly according
to the instructions given by the perfsonar team [R 5].

Information on security considerations is also provided by the perfsonar team [R 6]



Component installation information
==================================

For Debian, see [R 3] [R 4]

For RedHat they have not yet been fixed.
The upstream release fixing these issues is cacti-0.8.8c



Recommendations
===============

Sites running cacti/perfsonar should ensure that they are configured in a suitable way as described
by the Perfsonar team in the link above.

This is regardless of whether the cacti version is updated.

Sites running debian version, additionally should update.


Other information
==================

This was discussed at the SVG meeting on 20th November, and agreed that an advisory should be sent advising
sites to ensure they are configured correctly. Agreed 'High' risk for poorly configured sites.


Credit
======

These vulnerabilities were discovered by Mischa Salle and Wilco Baan Hofman from

Nikhef.

References
==========

[R 1] http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2014-5261

[R 2] http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2014-5262

[R 3] https://security-tracker.debian.org/tracker/CVE-2014-5261

[R 4] https://security-tracker.debian.org/tracker/CVE-2014-5262

[R 5] https://twiki.opensciencegrid.org/bin/view/Documentation/InstallUpdatePS

[R 6] http://www.perfsonar.net/deploy/security-considerations/


Timeline
========
Yyyy-mm-dd

2014-07-27 Vulnerabilities reported by Mischa Salle and Wilco Baan Hofman
2014-07-27 Acknowledgement from the EGI SVG to the reporter
2014--     Mischa Salle in touch with developers to arrange resolution
2014-11-20 Discussed in SVG meeting, agreed 'High' if poorly configured site
           and that an advisory should be sent
2014-11--- Advisory drafted - further discussions.
2014-12-01 Advisory sent to sites
2015-01-15 Public disclosure

```