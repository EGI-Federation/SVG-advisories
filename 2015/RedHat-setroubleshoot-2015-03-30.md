---
title: EGI CSIRT_Alert RedHat-setroubleshoot-2015-03-30
permalink: /CSIRT_Alerts/RedHat-setroubleshoot-2015-03-30
---

```
** WHITE information - Unlimited distribution allowed      **
** see https://go.egi.eu/tlp for distribution restrictions **


EGI CSIRT ADVISORY [EGI-ADV-20150330]

Title:       EGI Advisory 'CRITICAL' RISK CVE-2015-1815 RedHat setroubleshoot [EGI-ADV-20150330]

Date:        2015-03-30
Updated:


URL:         https://advisories.egi.eu/CSIRT_Alerts/RedHat-setroubleshoot-2015-03-30


Introduction
============

A vulnerability has been announced by RedHat in setroubleshoot software. [R 1]

This has been fixed in RedHat Enterprise linux and Scientific Linux.


Details
=======

This vulnerability allows command injection and privilege escalation by a specially crafted filename.

For vulnerable sites it is thought to be exploitable remotely by people with no credentials.

For more details see [R 1] and [R 2].


Risk category
=============

This issue has been assessed as 'Critical' by the EGI SVG Risk Assessment Team.


Affected software
=================

setroubleshoot

For version details see [R 3]



Component installation information
==================================

See [R 3], [R 4]



Recommendations
===============

Sites which have setroubleshoot installed are recommended to update relevant
components immediately, or de-install setroubleshoot.

All running resources MUST be either patched or otherwise have a work-around in
place at the latest by 2015-04-07  T21:00+01:00. Sites failing to act and/or
failing to respond to requests from the EGI CSIRT team risk site suspension.

However, we recommend any site which has setroubleshoot installed acts
immediately, and we hope no sites expose this vulnerability over the Easter
break.



References
==========

[R 1] https://bugzilla.redhat.com/show_bug.cgi?id=1203352

[R 2] http://seclists.org/oss-sec/2015/q1/1011

[R 3] https://rhn.redhat.com/errata/RHSA-2015-0729.html

[R 4] https://www.scientificlinux.org/sl-errata/slsa-20150729-1/


Timeline
========
Yyyy-mm-dd

2015-03-30 EGI alerted to the public announcement this vulnerability.
2015-03-30 Assessment by the EGI Software Vulnerability Group.
2015-03-30 Alert sent to sites
```
