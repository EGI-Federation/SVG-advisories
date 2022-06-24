---
title: EGI CSIRT Alert Shellshock-2014-09-29
permalink: /CSIRT_Alerts/Shellshock-2014-09-29
---

```
** WHITE information - unlimited distribution              **
** see https://go.egi.eu/tlp for distribution restrictions **

Title:       URGENT: Update 1: EGI CSIRT 'CRITICAL' Risk - 'shellshock' vulnerability - arbitrary code execution via crafted environment variables

Date:        2014-09-29
Updated


This advisory will be placed on the public wiki at:

URL:         https://advisories.egi.eu/CSIRT_Alerts/Shellshock-2014-09-29


Introduction
============

Multiple vulnerabilities that allows malicious user to run arbitrary
code with the privileges of victim that runs Bash scripts was found in
Bourne Again Shell (bash).

This has been called the 'shellshock' vulnerability and has been
widely publicised.

NOTE: EGI CSIRT issued an initial advisory about shellshock on
September 26, but since then additional problems and vulnerabilities
have been discovered.

All running resources MUST be either patched or otherwise have a
work-around in place by 2014-10-03T21:00+01:00. Sites failing to act
and/or failing to respond to requests from the EGI CSIRT team risk
site suspension.


Details
=======

A specially constructed environment variable that contains a function
definition and trailing executable statements will make bash execute
this code at the point of script initialization. This vulnerability
was assigned CVE-2014-6271 and is assessed CRITICAL by EGI CSIRT.

The initial patches issued by vendors like Red Hat and Ubuntu have
unfortunately been shown to be incomplete, and multiple additional
weaknesses allowing an attacker to trigger unintended code execution
have been found. The most serious of these is CVE-2014-6278, which is
assessed CRITICAL by EGI CSIRT.

There is a wide range of vectors that can be used to trigger the
shellshock vulnerabilities, including - but not limited to - batch
systems like Torque and Slurm, web cgi scripts and mail filters like
procmail.

Various exploits are publically available and are currently being used
on a massive scale by many groups of attackers.


Component installation information
==================================

To fully patch the vulnerabilities, sites must immediately install the
latest bash updates:

For Red Hat-type systems, these are the versions to update to:

 - Enterprise Linux 7 - bash-4.2.45-5.el7_0.4
 - Enterprise Linux 6 - bash-4.1.2-15.el6_5.2
 - Enterprise Linux 5 - bash-3.2-33.el5_11.4
 - Enterprise Linux 4 - bash-3.0-27.el4.4

For Ubuntu, these are the versions to update to:

 - Ubuntu 14.04 LTS - bash 4.3-7ubuntu1.4
 - Ubuntu 12.04 LTS - bash 4.2-2ubuntu2.5
 - Ubuntu 10.04 LTS - bash 4.1-2ubuntu3.4


Compatibility notes
===================

The latest bash update packages unavoidably break backward
compatibility for bash function export.

This can cause problems for certain software.

In particular, the TCL modules system wants to export a function
called "module". This was previously stored in a variable called
"module", but with the latest bash patches it needs to be called
"BASH_FUNC_module" instead - there is a separate name space for
functions.

Thus, if your site depends on TCL modules, it is important to
coordinate updates of bash and modules so that compatible versions are
used. Remember that you may have queued jobs that expect the old bash
syntax and will break with the updated bash. Depending on your
specific local environment, it may be possible to patch queued jobs in
place to use the new bash syntax.


Mitigation
==========

Due to the wide variety of vectors to trigger shellshock, EGI CSIRT
does not consider mitigation efforts a viable approach.


Credits
=======

The initial vulnerability was discovered by Stephane Chazelas (and
named by Andreas Lindh).

Additional vulnerabilites have been discovered by Florian Weimer,
Michal Zalewski and Todd Sabin.


References
==========

Red Hat support article: https://access.redhat.com/articles/1200223

Red Hat errata notice: https://rhn.redhat.com/errata/RHSA-2014-1306.html

Ubuntu security notice: http://www.ubuntu.com/usn/usn-2364-1/

Zalewski blog entry announcing CVE-2014-6278:
http://lcamtuf.blogspot.se/2014/09/bash-bug-apply-unofficial-patch-now.html
```
