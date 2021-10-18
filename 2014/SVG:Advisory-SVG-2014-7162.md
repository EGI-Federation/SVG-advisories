---
title: SVG:Advisory-SVG-2014-7162
permalink: /SVG:Advisory-SVG-2014-7162/
---

```
** White information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG ADVISORY [EGI-SVG-2014-7162]

Title:   EGI SVG Advisory "Critical" Risk. EGI-SVG-2014-7162 Perfsonar "Cacti
         Graphs" web vulnerability

Date:    2014-06-25
Updated:

URL:     https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-7162

Introduction
============

A vulnerability has been announced in Perfsonar to those subscribing to their
list whereby the web display can be defaced by an unauthorized person.

At least one web display has been defaced by a hacker.

Today it has been found that it is possible to upload code and remotely
execute, anonymously.

A patch is available, and was announced by the Perfsonar team.

This advisory is to state that sites using perfsonar should update according to
the e-mail from Perfsonar urgently, if they have not already done so.

It also alerts any site which does not subscribe to the perfsonar e-mail list
to become aware of the problem and update.

Details
========


This is as stated to the Perfsonar Announce e-mail address on 19th June 2014:

All,

Yesterday an issue was found with the Cacti configuration on all perfSONAR
Toolkit nodes.
The issue allows someone to access a settings web page unauthenticated from
which they can change titles and other display values on the Cacti graphs. The
extent of the harm that can be done appears to be limited to defacing the Cacti
web pages, and unfortunately this was exploited in a few cases. Yesterday we
posted manual work-arounds to correct this issue but today we have updates that
will automatically apply the necessary fixes.

The updates will 1) clear out any defaced fields and
2) require authentication to ANY cacti page, including just viewing the graphs.
We recommend ALL users update as soon as possible by taking the following
steps:

NetInstall Users:
 - Login to the command-line of your host and run 'yum update'
-  Run ' /sbin/service httpd restart'

LiveCD/LiveUSB Users:
 - Download and create a new CD from the relevant images found here:

http://software.internet2.edu/pS-Performance_Toolkit/

Thank you to all our users that brought this to our attention and have helped
us get to a solution. The perfSONAR core development team takes issues like
this very seriously, and we do our best to get fixes out as soon as possible.
As always, it's important to remember that the Toolkit nodes are at their
center just Linux servers and it is important to keep them patched like any
other host. Please let us know if you have any further questions about this
issue and thanks again for everyone's help and understanding while we worked
toward getting this resolved.

Thank you,

The perfSONAR Development Team

Risk category
=============

This issue has been assessed as "Critical" by the EGI CSIRT and EGI SVG Risk
Assessment Team


Affected software
=================

Perfsonar


Component installation information
==================================

Sites should update according to the Perfsonar instructions.


Recommendations
===============

Sites running Perfsonar should upgrade as soon as possible if they have not
already done so.

All running resources MUST be either patched or otherwise have a work-around in
place by 2014-07-02  T21:00+01:00. Sites failing to act and/or failing to
respond to requests from the EGI CSIRT team risk site suspension.


Other Information
=================

This issue was discussed at the EGI SVG meeting on 19th June 2014

At that time it was considered less serious, as perfsonar is loosly coupled to
other EGI resources, and this is thought to not pose a risk of damage to other
resources.

A member of the SVG team took action to further investigating Perfsonar
Security.

Later another member was able to demonstrate anonymous remote code execution
due to this vulnerability.



Credit
======

EGI SVG was alerted to this vulnerability was reported by Christopher Walker of
QMW.

Remote code execution demonstrated by the Nikhef team.

Timeline
========

Yyyy-mm-dd

2014-06-18 SVG Alerted to this by Christopher Walker.
2014-06-18 Acknowledgement from the EGI SVG to the reporter
2014-06-18 Updated packages available.
2014-06-19 Issue discussed at SVG monthly meeting.
2014-06-25 Anonymous remote code execution demonstrated by Nikhef.
2014-06-25 Elevated to 'Critical' risk.
2014-06-25 Advisory issued to sites by SVG.
2014-07-17 Advisory placed on public wiki.
```
