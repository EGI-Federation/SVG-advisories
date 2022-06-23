---
title: EGI CSIRT Alert systemtap-2010-11-18
permalink: /CSIRT_Alerts/systemtap-2010-11-18
---

```
** WHITE information - Unlimited distribution allowed      **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI CSIRT ADVISORY [EGI-ADV-20101118]

Title:       Critical Local root vulnerability in systemtap (CVE-2010-4170) [EGI-ADV-20101118]
Date:        November 18, 2010
Last update: November 18, 2010
URL:         https://advisories.egi.eu/CSIRT_Alerts/systemtap-2010-11-18


Introduction
============

Yesterday, updates for the systemtap package were released, fixing a
vulnerability that can give any local user root privileges on RHEL 5
and 6 (and their derivates) systems that have systemtap installed.

The reporter, Tavis Ormandy, has released an exploit for this issue.

This issue has been labeled CVE-2010-4170, and is regarded as a
critical vulnerability by the EGI CSIRT. Sites are requested to take
immediate action as outlined below. Failure to do so within 7 days may
lead to site suspension.

This issue also affects RHEL 4 and derivates, but is much less serious
there.

Vendor updates have been released for RHEL, CentOS, Scientific Linux
and SLC.


Details
=======

Systemtap is a tool for instrumenting a live running kernel and is
typically used for debugging or diagnosis of performance problems. To
let selected users run systemtap without giving them full root
permissions, the staprun binary is installed suid root (and performs
additional internal authorization checks).

However, before doing any authorization checks, staprun first tries to
load the uprobes kernel module by running /sbin/modprobe, and it does
not properly sanitize the environment first. This makes it possible to
supply a fake configuration file for modprobe which lets an attacker
run arbitrary commands with root privileges.

For example, Tavis Ormandy's one-line exploit launches a root shell:

  $ printf "install uprobes /bin/sh" > exploit.conf; MODPROBE_OPTIONS="-C exploit.conf" staprun -u whatever

  sh-4.0#

The problem also exists on RHEL 4, but there an attacker must be a
member of the stapusr group to exploit the issue, which reduces the
risk significantly.


Mitigation
==========

If vendor updates are not yet available for your system, the issue can
be worked around by:

a) if at all possible, uninstalling the vulnerable rpm package, systemtap-runtime

or

b) removing the suid bit from /usr/bin/staprun


Recommendations
===============

Sites should evaluate the need for having systemtap installed. If
there is a requirement to have the package installed, please apply
vendor updates immediately, otherwise uninstall the systemtap-runtime
rpm package.

If vendor updates are not yet available for your system, immediately
apply mitigation steps as outlined above.

Any of these actions can be taken without rebooting the system.


References
==========

Red Hat advisory: https://rhn.redhat.com/errata/RHSA-2010-0894.html
```
