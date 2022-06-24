---
title: EGI CSIRT Alert LinuxCVEs-2015-05-07
permalink: /CSIRT_Alerts/LinuxCVEs-2015-05-07
---

```
** WHITE information - Unlimited distribution allowed      **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI CSIRT ADVISORY [EGI-ADV-20150507]

Title:       EGI SVG Advisory 'High' RISK at least RH7 and derivatives - Linux vulnerabilities
  CVE-2015-1318 CVE-2015-1862 CVE-2015-3315  [EGI-ADV-20150507]

Date:        2015-05-07
Updated:     2015-07-06

URL:         https://advisories.egi.eu/CSIRT_Alerts/LinuxCVEs-2015-05-07


Introduction
============

3 new vulnerabilities have been found in Linux, which may allow privilege
escalation to root.
CVE-2015-1318,  CVE-2015-1862  CVE-2015-3315

Some versions of Linux which are used in the EGI infrastructure are vulnerable
to one or more of these issues.

Sites using vulnerable versions which have been fixed are recommended to patch
as soon as possible.

For sites using Red Hat Enterprise Linux 6 and 7 sites should disable ABRT as
soon as possible.

**UPDATE** Now fixed for RH7 - see [R 8]


Details
=======

Initial information has been sent to [R 1] and see other references.


Risk category
=============

The exact effect and hence the Risk associated with these vulnerabilities
varies for different linux versions.

This issue has been assessed as 'High' risk by the EGI CSIRT and EGI SVG Risk
Assessment Team for CVE-2015-3315 in the case of RedHat 7 and it's derivatives.


Affected software
=================

For RedHat
----------


RH6 and RH7 and derivatives are vulnerable to CVE-2015-3315 See [R 2]

**UPDATE**
This has now been fixed for RedHat See [R 8]

RedHat is not vulnerable to CVE-2015-1318,  CVE-2015-1862 [R 7]


For Debian
-----------

So far not reported to be vulnerable, see [R 3], [R 4], [R 5]


For Ubuntu
----------

CVE-2015-1318 is an issue For Ubuntu 14 - Fixed  [R 6]

CVE-2015-1862 Does not apply

CVE-2015-3315 Does not apply.



Mitigation
==========

Sites should disable ABRT if they are affected and cannot patch - see [2], this
should be carried out urgently in the case of RH7.

**UPDATE**

A patch is now available for RH7.



Component installation information
==================================

See software providers' information


Recommendations
===============


Sites running vulnerable versions are recommended to update relevant components
or take mitigating action as soon as possible.



Credit
======

SVG was first alerted to these vulnerabilities by Mischa Salle at Nikhef.

See references for original discoverer.

References
==========

[R 1] http://seclists.org/fulldisclosure/2015/Apr/34

[R 2] https://access.redhat.com/articles/1415483

[R 3] https://security-tracker.debian.org/tracker/CVE-2015-1318

[R 4] https://security-tracker.debian.org/tracker/CVE-2015-1862

[R 5] https://security-tracker.debian.org/tracker/CVE-2015-3315

[R 6] http://people.canonical.com/~ubuntu-security/cve/2015/CVE-2015-1318.html

[R 7] https://bugzilla.redhat.com/show_bug.cgi?id=1211835#c12

[R 8] https://rhn.redhat.com/errata/RHSA-2015-1083.html

Common Vulnerabilities and Exposures
====================================

http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-1318

http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-1862

http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-3315


NVD
===

https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2015-1318

(Others are not there yet.)


Timeline
========
Yyyy-mm-dd

2015-04-15 SVG alerted to Vulnerabilities by Mischa Salle
2015-04--- On-going checking and assessment by the EGI Software Vulnerability Group.
2015-04-30 Updated packages available in most cases
2015-05-07 Alert sent to sites
2015-07-06 Updated as fixed for RH7.
```
