---
title: EGI CSIRT Alert LinuxKernel-2014-07-04
permalink: /CSIRT_Alerts/LinuxKernel-2014-07-04
---

```
** WHITE information - Unlimited distribution allowed      **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI CSIRT ADVISORY [EGI-ADV-20140625]

Title:       EGI SVG Advisory 'High' RISK - CVE-2014-3153 Linux kernel privilege
escalation vulnerability    [EGI-ADV-20140704]

Date:        2014-07-04
Updated:     <date  yyyy-mm-dd>

URL:         https://advisories.egi.eu/CSIRT_Alerts/LinuxKernel-2014-07-04

Introduction
============

This vulnerability allows privilege escalation, including escalation to 'root' and
the ability to crash the kernel.

Previously EGI CSIRT sent a 'heads up' about this as a potential 'Critical' risk.
However, no public exploit has been confirmed so it has been assessed as 'High' risk

This has now been fixed in RHEL6 and SL6

RHEL5 and it's derivatives are not affected.



Risk category
=============

This issue has been assessed as 'High' risk by the EGI CSIRT team.


Affected software
=================

RHEL6 and its deriviatives.

For the SL6 the fixed kernel version is 2.6.32-431.20.3
which was provided on 19th June 2014



Mitigation
==========

N/A.


Component installation information
==================================

Sites should see the appropriate SL6 or RHEL6 documentation for further information.


Recommendations
===============

Sites deploying RHEL6 and it's derivatives are recommended to update as soon as possible,
if they have not done so already.

Note that if you updated after 19th June you should already have a fixed version of the kernel.

Credit
======

This vulnerability was found by EGI by Leif Nixon.
It had originally been reported to Google by a Pinkie Pie.



References
==========

[R 1] http://seclists.org/oss-sec/2014/q2/467

[R 2] http://seclists.org/oss-sec/2014/q2/469



Timeline
========
Yyyy-mm-dd


2014-06-06 SVG and EGI CSIRT become aware of the vulnerability
2014-06-10 Discussed at the EGI IRTF meeting and decided it was likely to become
           'critical' if a public exploit became available and a 'Heads up'
            should be sent to sites.
2014-06-11 'Heads up' sent to sites
2014-06-19 Updated packages available in RHEL6
2014-06-19 Updated packages available in SL6
2014-06-25 Risk assessed as 'High'
2014-07-04 Advisory to update sent to sites
```
