---
title: Advisory-SVG-2019-15258
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] Up to 'CRITICAL' risk systemd-journald
         vulnerabilities [EGI-SVG-2019-15258]

Date:    2019-01-10
Updated: 2019-01-15   Updates available therefore Advisory issued.
         2019-05-14   Update to inform that an exploit has been released.

Affected software and risk
==========================

Up to CRITICAL risk vulnerabilities concerning systemd-journald

Package : systemd-journald
CVE ID  : CVE-2018-16864,CVE-2018-16865,CVE-2018-16866

A set of vulnerabilities in systemd-journald have been reported by Qualys[R 1]
which can be used in combination to lead to a local root privilege escalation
by any local user.

**UPDATE 2019-05-14** Qualys released their exploit [R 8]



Actions required/recommended
============================

*UPDATE 15/1/2019*: Patches are available for RedHat [R 5], SL [R 6] and CentOS
[R 7]. See also individual RedHat CVE  advisories [R 2][R 3][R 4].

Sites running systemd are urged to update relevant components. This will
primarily include sites that use RHEL/CentOS/SL.
The most urgent hosts to update are worker nodes and UIs where users would
typically have access to.

Sites should be aware that if a public exploit is released which allows easy
root access in the EGI infrastructure this vulnerability is likely to be
elevated to 'Critical' and sites will then be required to patch within 7 days
or risk suspension - Qualys have noted that they will publish a working
exploit.

Component installation information
==================================

The RPM installer for the new version of systemd will re-exec the systemd
daemon, so a reboot is not required.
Sites may in addition wish to restart the systemd-journald process using, for
example, `systemctl restart systemd-journald`.

TLP and URL
===========

** WHITE information -
   Unlimited distribution - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for
   distribution restrictions **

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2019-15258

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 9]

Note that this has been updated and the latest version approved by the
Operations Management Board in November 2017


References
==========

[R 1] https://www.qualys.com/2019/01/09/system-down/system-down.txt
[R 2] https://access.redhat.com/security/cve/cve-2018-16864
[R 3] https://access.redhat.com/security/cve/cve-2018-16865
[R 4] https://access.redhat.com/security/cve/cve-2018-16866
[R 5] https://access.redhat.com/errata/RHSA-2019:0049
[R 6] https://www.scientificlinux.org/category/sl-errata/slsa-20190049-1/
[R 7] https://lists.centos.org/pipermail/centos-announce/2019-January/023143.html
[R 8] https://www.openwall.com/lists/oss-security/2019/05/10/4
[R 9] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was alerted to this vulnerability by David Crooks


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2019-15258]

2019-01-10 SVG alerted to this issue by David Crooks
2019-01-10 Initial EGI SVG Risk Assessment completed
2019-01-10 Heads Up sent to sites
2019-01-15 Changing to Advisory with updates being released by RedHat/SL/CentOS
2019-05-14 Added that an exploit has been released.

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 9] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```
