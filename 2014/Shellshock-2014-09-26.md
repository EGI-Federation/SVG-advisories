---
title: EGI CSIRT_Alert Shellshock-2014-09-26
permalink: /CSIRT_Alerts/Shellshock-2014-09-26
---

```
** WHITE information - unlimited distribution              **
** see https://go.egi.eu/tlp for distribution restrictions **

Title:       EGI CSIRT 'CRITICAL' Risk - 'shellshock' vulnerability - arbitrary code execution via crafted environment variables

Date:        2014-09-26
Updated


This advisory will be placed on the public wiki.

URL:         https://advisories.egi.eu/CSIRT_Alerts/Shellshock-2014-09-26



Introduction
============

A vulnerability that allows malicious user to run arbitrary code with
the privileges of victim that runs Bash scripts was found in Bourne
Again Shell (bash).

This has been called the 'shellshock' vulnerability and has been
widely publicised.


Details
=======

A specially constructed environment variable that contains function
definition and trailing executable statements will make bash execute
this code at the point of script initialization.

Various exploits are already publicly available.


Risk Category
=============

This issue has been assessed as 'Critical' risk by the EGI CSIRT
and EGI SVG Risk Assessment Team.


Affected Software
=================

Components : All scripts that employ bash as the scripting language

Releases:
 - bash 3.0 up to (but not including) 3.0 patchlevel 017
 - bash 3.1 up to (but not including) 3.1 patchlevel 018
 - bash 3.2 up to (but not including) 3.2 patchlevel 052
 - bash 4.0 up to (but not including) 4.0 patchlevel 039
 - bash 4.1 up to (but not including) 4.1 patchlevel 012
 - bash 4.2 up to (but not including) 4.2 patchlevel 048
 - bash 4.3 up to (but not including) 4.3 patchlevel 025


Component installation information
==================================

Currently software updates are available from most OS vendors.

CentOS:
 - general announcement: http://lists.centos.org/pipermail/centos/2014-September/146099.html
 - CentOS 5.x: http://lists.centos.org/pipermail/centos-announce/2014-September/020582.html
 - CentOS 6.x: http://lists.centos.org/pipermail/centos-announce/2014-September/020585.html
 - CentOS 7.x: http://lists.centos.org/pipermail/centos-announce/2014-September/020583.html
Versions in which this issue was fixed:
 - CentOS 5.x: bash-3.2-33.el5.1
 - CentOS 6.x: bash-4.1.2-15.el6_5.1
 - CentOS 7.x: bash-4.2.45-5.el7_0.2

RedHat:
 - general announcement: https://access.redhat.com/solutions/1207723
 - RHEL 5/6/7: https://rhn.redhat.com/errata/RHSA-2014-1293.html
 - RHEL 5/6, Shift_IJS packages: https://rhn.redhat.com/errata/RHSA-2014-1295.html
 - RHEL extended support: https://rhn.redhat.com/errata/RHSA-2014-1294.html
Versions in which this issue was fixed:
 - Red Hat Enterprise Linux 7 - bash-4.2.45-5.el7_0.2
 - Red Hat Enterprise Linux 6 - bash-4.1.2-15.el6_5.1
 - Red Hat Enterprise Linux 5 - bash-3.2-33.el5.1
 - Red Hat Enterprise Linux 4 Extended Lifecycle Support - bash-3.0-27.el4.2
 - Red Hat Enterprise Linux 5.6 Long Life - bash-3.2-24.el5_6.1
 - Red Hat Enterprise Linux 5.9 Extended Update Support - bash-3.2-32.el5_9.2
 - Red Hat Enterprise Linux 6.2 Advanced Update Support - bash-4.1.2-9.el6_2.1
 - Red Hat Enterprise Linux 6.4 Extended Update Support - bash-4.1.2-15.el6_4.1
 - SJIS for Red Hat Enterprise Linux 6 - bash-4.1.2-15.el6_5.1.sjis.1
 - SJIS for Red Hat Enterprise Linux 5 - bash-3.2-33.el5_11.1.sjis.1




Mitigation
==========

Check that no externally-supplied environment variables will leak
into environment of bash scripts.


Recommendations
===============

You can check if your bash version is vulnerable by running the following
command:

  env x='() { :;}; echo vulnerable' bash -c "echo this is a test"

Vulnerable versions will produce two lines of output,

{{{
vulnerable
this is a test
}}}

while patched versions will give a diagnostic message instead of the first
line:

{{{
bash: warning: x: ignoring function definition attempt
bash: error importing function definition for `x'
this is a test
}}}

Those who have not already done so should be updated as soon as possible.

All running resources MUST be either patched or otherwise have a
work-around in place by 2014-10-03T21:00+01:00. Sites failing to act and/or
failing to respond to requests from the EGI CSIRT team risk site suspension.


Other information
=================

As a basic security best practice, it is strongly recommended to
disallow control on the environment variables to the external parties.

This includes passing environment to the set-uid scripts, programs
that make parts of user-provided data to HTTP/CGI pages to be a part
of the environment for the processing script, programs that pass data
to external scripts via environment variables, etc.

This advisory will be updated as more information comes available


Credits
=======

The vulnerability was discovered by Stephane Chazelas (and named by
Andreas Lindh).


References
==========

[1] http://seclists.org/oss-sec/2014/q3/650
[2] https://securityblog.redhat.com/2014/09/24/bash-specially-crafted-environment-variables-code-injection-attack/


Timeline
========

Yyyy-mm-dd

2014-09-25 EGI SVG and CSIRT alerte to problem by Leif Nixon
2014-09-25 'Heads up'sent to EGI site and NGI security contacts.
2014-09-25 Advisory drafted by Eygene Ryabinkin.
2014-09-26 Assessed as 'Critical'
2014-09-26 Advisory issued.
```
