---
title: SVG:Advisory-SVG-2011-2296
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI CSIRT ADVISORY [EGI-ADV-20110615-02]

Title:        High Risk - Torque Authentication Bypass Vulnerability -
              Update [EGI-ADV-20110615-02] CVE-2011-2907
Date:         2011-06-14
Updated:      2011-06-20
Updated:      2011-08-15

URL:          https://wiki.egi.eu/wiki/EGI_CSIRT:Alerts/Torque-2011-06-15
URL:          https://wiki.egi.eu/wiki/Advisory-SVG-2011-2296


Introduction
============

This is an update to the advisory [EGI-ADV-20110615], as a patch is available
in EPEL, and additionally this vulnerability has been made public.

This vulnerability has also been assigned CVE-2011-2907


Details
=======

The advisory sent by CSIRT[EGI-ADV-20110615] intentionally did not
contain full details on the vulnerability, since it was not then public.

The impact of the vulnerability can be summarized like this:

If you are running a vulnerable Torque version and have not applied
the recommended "acl_hosts" configuration, an attacker that can
connect to port 15001 on the Torque server from a machine under his
control can submit jobs as any user, bypassing all authentication
checks in Torque. This attack machine may be located anywhere on the
Internet, as long as it can connect to port 15001 on the server.

Irrespective of this particular vulnerability, the EGI CSIRT strongly
recommends that you always limit network connectivity to port 15001 to
trusted hosts that need to contact it. This includes submit hosts
(CEs), worker nodes and any other machines in the cluster that need
to talk to the Torque server.

Full details of the vulnerability are now available on the RedHat Bugzilla
[R 1]

This vulnerability has been assigned CVE-2011-2907

Affected Software
=================

At least Torque versions 2.3.13, 2.4.12 and 3.0.1 are vulnerable,
which are commonly used in the EGI infrastructure. Other versions
might also be vulnerable.


Mitigation
==========

Sites should carry out the following mitigating action. As always,
please follow your change management procedure when making
configuration change in your production environment.

Step 1: put Torque server behind a firewall (but remember that your
        submit hosts and worker nodes need to be able to connect to
        it)

Step 2: for each queue, make the following configuration change

  #Enable queue level host-based ACL
  set queue <queuename> acl_host_enable = True

  #Add a list of trusted hosts (such as your CEs) which can submit jobs to this
  queue set queue <queuename> acl_hosts = Trusted_CE1, trusted_CE2

Step 3: test configuration change thoroughly before rolling it into
        your production system.


Component Installation information
==================================

A patch is now available from RedHat EPEL

They are detailed fully in the release notes:

https://admin.fedoraproject.org/updates/torque-2.5.7-1.el4.1
https://admin.fedoraproject.org/updates/torque-2.5.7-1.el5.1
https://admin.fedoraproject.org/updates/torque-2.5.7-1.el6


Recommendations
===============

Sites are strongly recommended to run Torque behind a firewall, in
particular port 15001 should be restricted so that direct access to
Torque from an untrusted host is not allowed.

Sites should check the configuration and follow the mitigating action to
prevent the expolitation of this vulnerability in the Torque software.

Sites should upgrade as soon as is practical, and leave firewalling in place.


Credit
======

This vulnerability was reported by Bartlomiej Balcerek of the Wroclaw Centre
for Networking and Supercomputing Security Team.


References
==========

[R 1] https://bugzilla.redhat.com/show_bug.cgi?id=713090


Timeline
========
Yyyy-mm-dd

2011-06-09 Vulnerability reported by Bartlomiej Balcerek, in addition to
           reporting to software providers.
2011-06-09 Acknowledgement from the EGI SVG to the reporter
2011-06-13 CSIRT members of SVG carried out further investigations and decided
           to recommend mitigating action.
2011-06-14 Advisory drafted with recommended mitigation.
2011-06-15 Advisory revised after further tests
2011-06-16 Advisory sent to EGI sites and NGI security contacts
2011-06-20 Update advisory sent to EGI sites and NGI security contacts
2011-08-11 Patch available in EPEL, information made public and CVE assigned
2011-08-15 Advisory revised
```
