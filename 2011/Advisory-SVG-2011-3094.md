---
title: Advisory-SVG-2011-3094
---

```
Update 26th January 2012 - fix for gLite 3.2 released on 24th January.

** White information - Unlimited distribution allowed            **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2011-3904]


Title:        High Risk - Torque Munge Impersonation vulnerability

Date:         2011-12-21
Updated:      2012-01-24

URL:          https://advisories.egi.eu/2011/Advisory-SVG-2011-3094


Introduction
============

A vulnerability has been found in Torque which may allow users to impersonate
other users.

This has been fixed in the version of Torque in EPEL, and it is recommended
that sites using EMI and UMD upgrade to a fixed version of Torque from the EPEL
site.

This advisory has been updated as a fixed version of Torque is now available in
gLite 3.2.


Details
=======

Torque server does not properly check user credentials in the case where Munge
is present.
In some situations one user may be able to impersonate another user and perform
actions inlcuding submitting a job.

Full details of the vulnerability are now available on the RedHat Bugzilla
[R 1]


Risk Category
=============

This issue has been assessed as 'High'  risk by the  EGI SVG Risk Assessment
Team.


Affected Software
=================

For EPEL, versions of Torque in EPEL prior to:

torque-2.5.7-7.el4
torque-2.5.7-7.el5
torque-2.5.7-9.el6

may be affected.



Component Installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distrbution
(UMD).

A patch is now available from RedHat EPEL this is appropriate for use of sites
installing from the EGI UMD and sites installing directly from the EMI
distribution.

They are detailed fully in the release notes:

https://admin.fedoraproject.org/updates/torque-2.5.7-7.el4
https://admin.fedoraproject.org/updates/torque-2.5.7-7.el5
https://admin.fedoraproject.org/updates/torque-2.5.7-9.el6

A patch is also available for sites installing from gLite 3.2

gLite 3.2:

http://glite.cern.ch/security_updates

gLite 3.2 Security Update 2

It should be noted that the above versions require Munge [R2], both on the WN
for the torque-client as well as the server.

Some notes on Munge installation and configuration (from EPEL5 earlier version
of Torque):

The updated EPEL5 build of torque-2.5.7-1 and later as compared to previous
versions enables munge as an inter node authentication method.

It is highly advisable that prior to upgrading to version 2.5.7-1 or later of
this torque package that munge is installed and enabled. A munge package is
available within EPEL5.

https://admin.fedoraproject.org/community/?package=munge#package_maintenance

To enable munge on your torque cluster:

  * Install the munge package on your pbs_server and submission hosts in your
    cluster.

  * On one host generate a key with /usr/sbin/create-munge-key

  * Copy the key, /etc/munge/munge.key to your pbs_server and submission hosts
    on your cluster.

  * Start the munge daemon on these nodes.. service munge start && chkconfig
    munge on


Recommendations
===============

It is recommended that sites installing from EMI or the EGI UMD update Torque
from the Redhat EPEL site as soon as possible if they have not done so already.

Sites installing gLite 3.2 should update as soon as possible from if they did
not update from:
http://software.nikhef.nl/temporary/torque-patch-5169/rhel5/RPMS/ earlier.


Credit
======

This vulnerability was reported by Adam Smutnicki and Lukasz Flis


References
==========

[R 1] https://bugzilla.redhat.com/show_bug.cgi?id=752079
[R 2] http://code.google.com/p/munge/


Timeline
========

Yyyy-mm-dd

2011-11-03 Vulnerability reported by Adam Smutnicki and Lukasz Flis
2011-11-03 Acknowledgement from the EGI SVG to the reporter
2011-11-08 Risk Assessment complete and Issue reported as EPEL bug.
2011-12-20 Patch available from EPEL
2011-12-21 Advisory released to community
2012-01-24 gLite 3.2 update available, advisory released publicly


For the EGI SVG,
```
