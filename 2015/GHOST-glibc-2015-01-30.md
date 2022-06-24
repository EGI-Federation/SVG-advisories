---
title: EGI CSIRT Alert GHOST-glibc-2015-01-30
permalink: /CSIRT_Alerts/GHOST-glibc-2015-01-30
---

```
** WHITE information - Unlimited distribution allowed      **
** see https://go.egi.eu/tlp for distribution restrictions **


EGI CSIRT ADVISORY [EGI-ADV-20150130]

Title:       EGI Alert 'High' risk CVE-2015-0235 GNU C Library (glibc) "GHOST" vulnerability - [EGI-ADV-20150130]

Date:        2015-01-30

Updated:

URL:         https://advisories.egi.eu/CSIRT_Alerts/GHOST-glibc-2015-01-30

Introduction
============

A buffer overflow vulnerability CVE-2015-0235 in the GNU C Library (glibc)
called the "GHOST" vulnerability has been announced which may be exploited
remotely.

This has been defined as having 'Critical' impact by RedHat [R 1]

So far no exploit has been found in software commonly used on the EGI
Infrastructure.

We cannot be sure that there isn't potentially a serious exploit in the EGI
infrastructure which we are not aware of, therefore we ask sites to update as
soon as possible.

Details
=======

It is stated in [R 2] many commonly used applications are not vulnerable.

Additionally, this has not been found to be exploitable in Grid Middleware in
common use in EGI, although we cannot be certain something has not been missed.

Globus has stated that the Globus Toolkit software is not vulnerable to
currently known exploits resulting from this vulnerability [R 3]

Further information can be found at [R 4], [R 5]

Risk category
=============

This issue has been assessed as 'High' risk by the EGI Security officer.

However, if an exploit relevant to the EGI infrastructure were to emerge it is
likely to be revised to 'Critical' risk.


Affected software
=================

See [R 5]



Recommendations
===============

We recommend sites update relevant components as soon as possible due to the
seriousness of this issue if some software on the infrastructure is found to be
vulnerable.

If an exploit relevant to EGI is found the risk will be re-assessed and is
likely to rise, and updates are likely to be requested urgently.


Credit
======

This vulnerability was announced publicly.

EGI SVG and CSIRT were first alerted to this vulnerability by Michal Prochazka
and Eygene Ryabinkin at approx the same time.


References
==========

[R 1] https://access.redhat.com/security/cve/CVE-2015-0235

[R 2] http://www.openwall.com/lists/oss-security/2015/01/27/18

[R 3] https://support.globus.org/entries/87762727

[R 4] https://www.qualys.com/research/security-advisories/GHOST-CVE-2015-0235.txt

[R 5] http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2015-0235


Timeline
========
Yyyy-mm-dd

2015-01-27 Vulnerability announced publicly
2015-01-28 EGI SVG and CSIRT alerted to this vulnerability by Michal Prochazka and Eygene Ryabinkin,
           discussions took place
2015-01-29 Agreed that although no obvious exploit has been found an advisory should be issued
           recommending sites update as soon as possible.
2015-01-30 EGI Security officer and SVG chair agreed to 'High' risk.
2015-01-30 Alert sent to sites


On behalf of the EGI CSIRT and SVG,
```
