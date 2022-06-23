---
title: EGI CSIRT Alert liblinker-2010-10-23
permalink: /CSIRT_Alerts/liblinker-2010-10-23
---

```
** WHITE information - Unlimited distribution allowed      **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI CSIRT ADVISORY [EGI-ADV-20101023]

Title:       HIGH Vulnerability in C library dynamic linker (CVE-2010-3856) [EGI-ADV-20101023]
Date:        October 23, 2010
Last update: November 01, 2010
URL:         https://advisories.egi.eu/CSIRT_Alerts/liblinker-2010-10-23

Introduction
============

On Friday evening, Tavis Ormandy released information about a
vulnerability in GNU libc, complete with an exploit that on many
systems can give any local user root privileges. (For full details,
see the link below.)

This vulnerability has been labelled CVE-2010-3856, and is present on
many Linux distributions, including RHEL/CentOS/SL 5 (but not RHEL 3
and 4 and their derivatives). Patches are available for most distributions.

Please note that this is a different vulnerability than CVE-2010-3847,
and that recent Red Hat glibc patches for CVE-2010-3847 do *not* address
this new vulnerability.

The EGI CSIRT considers this to be a High vulnerability.


Details
=======

The dynamic linker in GNU libc can be enticed to load insecure shared
libraries when launching suid/sgid binaries by setting the LD_AUDIT
environment variable. By carefully selecting which libraries to load,
it is possible to attain root privileges in many different ways.

The example exploit in Ormandy's write-up relies on the presence of
the libpcprofile.so, which on Red Hat derivatives is part of the
glibc-util package. This is normally not installed. Even if it is,
differences in the behaviour of crond prevents the example exploit
from working.

However, even if no public exploit for Red Hat-like systems is known,
it must be stressed that there are probably many different ways to
exploit this vulnerability.


Mitigation
==========

There are no known mitigation methods.


Recommendations
===============

Patches are available for these distributions:
* Debian
* Ubuntu
* RHEL5
* SL5
* SLC5
* CentOS5

You may wish to suspend user logins and job submission until these steps
have been taken; please refer to your local site policy.


References
==========

Ormandy's original write-up:
http://seclists.org/fulldisclosure/2010/Oct/344

Updates for Debian:
http://www.debian.org/security/2010/dsa-2122

Updates for Ubuntu:
https://lists.ubuntu.com/archives/ubuntu-security-announce/2010-October/001187.html

Updates for RHEL5:
https://rhn.redhat.com/errata/RHSA-2010-0793.html

Updates for SL5:
http://listserv.fnal.gov/scripts/wa.exe?A2=ind1010&L=scientific-linux-errata&T=0&P=2769

Updates for SLC5:
http://linux.web.cern.ch/linux/updates/updates-slc5.shtml#27.10.2010.shtml

Updates for CentOS5:
http://lists.centos.org/pipermail/centos-announce/2010-October/017124.html
```
