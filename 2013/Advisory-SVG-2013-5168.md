---
title: Advisory-SVG-2013-5168
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG ADVISORY [EGI-SVG-2013-5138]

Title:   EGI SVG Advisory 'Moderate' RISK  Globus GSI-OpenSSH vulnerability
         [EGI-SVG-2013-5168]

Date:    2013-10-25
Updated: <date  yyyy-mm-dd>

URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2013-5168

Introduction
============

A vulnerability was found in GSI-OpenSSH and fixed by the globus team.

This is now available in the version of GSI-OpenSSH in EGI UMD 2, in release
2.7.0

This software not included in UMD 3 so this advisory is not relevant to sides
running software from UMD-3

Details
=======

Details are as below in the original Globus advisory appended.


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 2 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/

Sites who wish to install directly from the EMI 2 release should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/


Recommendations
===============

Sites are recommended to update relevant components in due course.


Globus Original Advisory
========================

GSI-OpenSSH Security Advisory: pamuserchange-2013-01.adv

URL: http://grid.ncsa.illinois.edu/ssh/pamuserchange-2013-01.adv

Original issue date: March 12 2013
Last revised: None

Software affected:
  GSI-OpenSSH (versions 4.7-5.5)
  GSI patch for OpenSSH (versions 20090831-20120903)

1. Overview

GSI-OpenSSH is a modified version of OpenSSH that adds support for RFC 3820
proxy certificate authentication and delegation. GSI-OpenSSH is provided by
NCSA and is not associated with the OpenSSH project.
GSI-OpenSSH is provided as both a standalone package and as a patch to OpenSSH.

The PermitPAMUserChange feature added to GSI-OpenSSH in August 2009 [1] based
on an earlier OpenSSH patch [2] contains a memory management bug that may allow
an authenticated user to log in to an unauthorized account. The
PermitPAMUserChange feature is disabled by default and must be explicitly
enabled by the system administrator.  It is used primarily with MEG (MyProxy
Enabled GSISSHD) [3].

The PermitPAMUserChange feature allows users to log in to a system using a
username that need not correspond to a local system account, provided that PAM
accepts the username, authenticates the user, and then maps the user to an
existing local system account via PAM_USER.
The memory management bug can cause the authenticated user to be mapped to an
account different than PAM_USER.

2. Affected Configurations

Default configurations of GSI-OpenSSH are not affected.

The bug can be triggered only if sshd_config contains "PermitPAMUserChange yes"
and /etc/pam.d/sshd (or equivalent) is configured with a PAM module that
modifies PAM_USER.

3. Mitigation

Removing "PermitPAMUserChange yes" from sshd_config (if it was previously added
by the system administrator) will disable the affected functionality.

4. Fix

GSI-OpenSSH 5.6 contains a fix for this bug.

Alternatively system administrators may apply the following patch to the
GSI-OpenSSH source code:

diff -Naur old/auth-pam.c new/auth-pam.c
--- old/auth-pam.c  2010-08-10 14:36:30.000000000 +0000
+++ new/auth-pam.c  2013-03-12 19:10:29.000000000 +0000
@@ -312,7 +312,7 @@
            fatal("PAM: could not get passwd entry for user "
                "'%.100s' provided by PAM_USER", user);
        pwfree(sshpam_authctxt->pw);
-       sshpam_authctxt->pw = pw;
+       sshpam_authctxt->pw = pwcopy(pw);
        sshpam_authctxt->valid = allowed_user(pw);
        debug("PAM: user '%.100s' now %svalid", user,
            sshpam_authctxt->valid ? "" : "in");

5. Credit

This issue was reported by Venkatesh Yekkirala.

6. References

[1] https://bugzilla.mcs.anl.gov/globus/show_bug.cgi?id=6839
[2] https://bugzilla.mindrot.org/show_bug.cgi?id=1215
[3] http://wiki.ngs.ac.uk/index.php?title=MEG


Timeline
========

Yyyy-mm-dd

2013-03-12 Advisory draft discussed on Globus Security Committee
2013-04-02 Advisory made public by Globus
2013-04-05 Risk assessed as 'Moderate' for EGI.
2013-04-05 Noted a vulnerable version in UMD
2013-04-05 This was reported to IGE people and UMD people
2013-10-23 Updated packages available in the EGI UMD-2
2013-10-25 Sites informed and Public disclosure of this advisory
```
