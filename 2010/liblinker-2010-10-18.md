---
title: EGI CSIRT Alert liblinker-2010-10-18
permalink: /CSIRT_Alerts/liblinker-2010-10-18
---

```
** WHITE information - Unlimited distribution allowed      **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI CSIRT ADVISORY [EGI-ADV-20101018]

Title:       HIGH Vulnerability in C library dynamic linker (CVE-2010-3847) [EGI-ADV-20101018]
Date:        October 18, 2010
Last update: November 01, 2010
URL:         https://advisories.egi.eu/CSIRT_Alerts/liblinker-2010-10-18


Introduction
============

Earlier today, Tavis Ormandy released information about a
vulnerability in GNU libc, complete with an exploit that on many
systems can give any local user root privileges. (For full details,
see the link below.)

This vulnerability has been labelled CVE-2010-3847, and is present on
many Linux distributions, including RHEL/CentOS/SL 5 (but *not* RHEL 3
and 4 and their derivatives). Vendor patches are available for many
distributions.

Details
=======

As far as is known, the vulnerability can only be exploited if users can
write to a file system that contains binaries with suid root
permissions. (Since it is necessary for the attacker to create a hard
link to a suid root binary.)

This is, for instance, the case if /bin is located on the same
filesystem as /tmp (or any other user writable location, like /var/tmp,
/home, /var/lib/texmf, and so on). This is unfortunately a common
configuration.

Mitigation
==========

To make it impossible to make the required hard link, directories
containing suid/sgid binaries can be made to appear to as separate
file systems by doing

  mount -o bind /sbin /sbin

for each such directory. 

Please note that these commands must be re-run whenever the system is
rebooted, for example by adding them to a suitable init script.

A baseline list of directories with suid/sgid binaries on a typical
RHEL 5 system is:

  /bin
  /sbin
  /usr/bin
  /usr/libexec
  /usr/lpp
  /usr/sbin

You should check for any additional site specific locations using a command
like

  find / -type f \(-perm /u+s -o -perm /g+s\)

that will list all files with suid/sgid permissions.
 

Recommendations
===============

Apply the mitigation method above for all relevant locations if there are no
vendor patches available for your system.

You may wish to suspend user logins and job submission until these steps
have been taken; please refer to your local site policy. 

Vendor patches are available for RHEL5 and its derivates (SL5, SCL5, CentOS5);
see below for links.  Install the patches as soon as possible.

References
==========

* http://seclists.org/fulldisclosure/2010/Oct/257
* RHEL5: https://rhn.redhat.com/errata/RHSA-2010-0787.html
* SL5: http://listserv.fnal.gov/scripts/wa.exe?A2=ind1010&L=scientific-linux-errata&T=0&P=2516
* SLC5: http://linux.web.cern.ch/linux/updates/updates-slc5.shtml#25.10.2010.shtml
* CentOS5: http://lists.centos.org/pipermail/centos-announce/2010-October/017099.html
```
