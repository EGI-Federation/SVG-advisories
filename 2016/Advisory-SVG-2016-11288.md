---
title: SVG:Advisory-SVG-2016-11288
---

```
Title:   EGI SVG Advisory [TLP:AMBER] 'MODERATE' risk dCache READONLY and non-/
         user root not enforced [EGI-SVG-2016-11288]

Date:    2016-06-28
Updated: 2016-07-12

Affected software and risk
==========================

MODERATE risk vulnerability concerning dCache READONLY and non-/ user root not
enforced.

Package : dCache

A regression introduced with dCache v2.15 resulted in some access configured to
be 'read-only' not being honoured. The problem is worse with dCache v2.16 as,
in addition, non-default users' root directory (i.e., other than "/") are not
always honoured.

This affects some versions of dCache available from the dCache site only.

Note that versions in EGI UMD-3 and EGI UMD-4 are not affected.

Actions required/recommended
============================

Sites which install dCache directly from the dCache site are recommended to
check whether they have a vulnerable version installed and to update relevant
components if necessary.

Sites installing dCache from EGI UMD-3 and EGI UMD-4 do not need to take any
action.

Affected software details
=========================

dCache from v2.15.0 to v2.15.9 (readonly problem),
dCache from v2.16.0 to v2.16.3 (readonly and user-root problems).

Unaffected versions:

dCache v2.14 and earlier,
dCache v2.15.10 and later,
dCache v2.16.4 and later.

Note that versions in EGI UMD-3 and EGI UMD-4 are not affected

More information
================

This is a full description from the dCache team

Description:

     A door may be configured to be read-only.  This means that all
     users who use that specific door are not allowed to make any
     changes to dCache, even though such users may have permission to
     modify dCache otherwise.

     The webdav door also supports three different levels of access for
     anonymous users (those who presented no credential): FULL,
     READONLY and NONE.  With FULL, anonymous users can upload, rename
     and delete content in directories but only where the namespace
     permissions grant POSIX "other" users that right.  With READONLY,
     anonymous users cannot upload, rename or delete content
     irrespective of the namespace permissions.  If NONE then all
     operations fail.

     dCache allows the dCache admin to declare that an individual user
     has read-only access.  This means that the user cannot upload,
     rename or delete content, even though the namespace indicates she
     has permission to do so.

     dCache supports user-specific root directories.  With this, the
     dCache admin can declare that a user has access to only some
     subtree of the namespace.

     dCache v2.15.0 introduced a bug where read-only access was not
     enforced.  This problem affected all non-NFS protocols: dcap, ftp,
     srm, webdav and xrootd.  This also affected webdav anonymous
     access: READONLY is treated as FULL.

     In dCache v2.16.0, in addition, user-specific root directories are
     not being enforced for all operations.

Limiting factors:

     The problem does not affect NFS doors.

     The permission checks from the namespace are always enforced.

     We believe that the read-only users feature is not widely used.

     The default configuration of doors is read-write, but we are aware
     of sites deploying read-only doors.

     In 2.15, the problem only affects read-write doors if the user is
     configured read-only.

     In 2.16, the problem only affects read-write doors if the user is
     configured read-only or if the user has a non-'/' user-specific
     root directory.

     The problem only affects read-write users if they access dCache
     through a read-only door.


Mitigation:

     With dCache v2.15, read-only doors should be stopped and read-only
     users temporarily banned.  This will also work for dCache v2.16 if
     all users have '/' as their user-specific root directory.

     There is no mitigation for dCache v2.16 if users have non-'/'
     user-specific root directory.


Component installation information
==================================

See the dCache site - only versions installed from the dCache site are
vulnerable.

https://www.dcache.org/downloads/IAgree.shtml


The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Note that versions in the EGI UMD are not vulnerable.

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/


TLP and URL
===========

** AMBER information - Limited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

This advisory will be placed on the wiki on or after 2016-07-12

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2016-11288

Minor updates may be made without re-distribution to the sites

Credit
======

SVG was alerted to this vulnerability by Paul Millar from the dCache team.

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-11288]

2016-06-27 SVG alerted to this issue by Paul Millar from the dCache team
2016-06-27 Acknowledgement from the EGI SVG to the reporter
2016-06-28 EGI SVG Risk Assessment completed
2016-06-28 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2016-06-28 Updated packages available at the dCache site
2016-06-28 Advisory sent to sites
2016-07-12 Public disclosure


On behalf of the EGI SVG,
```
