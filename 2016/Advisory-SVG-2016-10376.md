---
title: Advisory-SVG-2016-10376
---

```
Title:   EGI SVG Advisory 'HIGH' risk CVE-2016-0728 Linux Kernel vulnerability
         [EGI-SVG-2016-10376]

Date:    2016-02-03
Updated:

** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

Affected Software and Risk
==========================

'High' risk vulnerability CVE-2016-0728 concerning some linux kernel versions.
This includes Redhat 7 based kernels, CentOS Linux 7 and Scientific Linux 7,
Debian and Ubuntu.

RedHat 6, RedHat 5, and derivatives are not affected.

Actions Required/Recommended
============================

Sites running vulnerable versions should apply vendor kernel updates as soon as
possible.

More information
================

This advisory is being issued because CVE-2016-0728 [R 1] Linux Kernel
Vulnerability is considered 'High' risk in EGI for vulnerable systems.

Info on this vulnerability is provided by the  [R 1], [R 2] and [R 3]

A detailed description of the vulnerability is publicly available at [R 4]


Affected software
=================

RedHat 7 and its derivatives are affected. [R 1]

Ubuntu is affected [R 2]

Debian is affected [R 3]

RedHat 5, and Red Hat 6 and their derivatives are not affected.


Mitigation
==========

N/A

Component installation information
==================================

See [R 5] for RedHat 7

See [R 6] for CentOS

See [R 7] for Scientific Linux

See [R 2] for Ubuntu

See [R 3] for Debian

URL
===

URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2016-10376

Minor updates may be made without re-distribution to the sites

Credit
======

SVG was alerted to this vulnerability by Ian Neilson who is a member of SVG.

Vincent Brillault able to demonstrate local exploit using a Redhat 7 based
kernel, but did not obtain root.


References
==========


[R 1] Red Hat https://access.redhat.com/security/cve/CVE-2016-0728

[R 2] Ubuntu http://people.canonical.com/~ubuntu-security/cve/2016/CVE-2016-0728.html

[R 3] Debian https://security-tracker.debian.org/tracker/CVE-2016-0728

[R 4] http://perception-point.io/2016/01/14/analysis-and-exploitation-of-a-linux-kernel-vulnerability-cve-2016-0728/

[R 5] https://rhn.redhat.com/errata/RHSA-2016-0064.html

[R 6] https://lists.centos.org/pipermail/centos-announce/2016-January/021625.html

[R 7] https://www.scientificlinux.org/sl-errata/slsa-20160064-1/


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

We are working on improving the advisory template/layout and comments are
welcome

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-10376]

2016-01-19 SVG alerted to this issue by Ian Neilson
2016-01-21 Investigation of vulnerability and relevance to EGI carried out by
           SVG
2016-01-26 Updated packages available for RedHat, SL, CentOS.
2016-01---, 2016-02-01  discussions on risk in EGI.
2016-02-03 Advisory/Alert sent to sites
```
