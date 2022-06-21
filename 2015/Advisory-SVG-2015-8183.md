---
title: Advisory-SVG-2015-8183
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2015-8183]

Title:   EGI SVG Advisory - dCache vulnerability for some access methods [SVG
         EGI-SVG-2015-8183]

Date:    2014-02-20
Updated:


URL:     https://wiki.egi.eu/wiki/Advisory-SVG-2015-8183

Introduction
============

A vulnerability has been found in dCache where username and password
authenticating FTP doors have been accidentally set to allow 'write' access by
default, whereas they should be 'read' access only.

Most deployments in EGI should not be vulnerable to this, as access is X.509
based with authorization methods in place and this vulnerability is not
exploitable.

If a site has set up an FTP door which allows read access to public data, not
via the EGI recommended access methods, then a user may be able to delete and
modify files.

Note also that the version in the EGI UMD is not vulnerable as the version in
the EGI UMD is version 2.6, and this vulnerability was introduced in dCache 2.7
and higher.


Details
=======

dCache supports the FTP protocol with three authentication schemes: GSI
("GridFTP"), Kerberos and Plain. The last option supports username and password
authentication and sends data unencrypted over the network; therefore, it is
also known as the "weak" FTP door.

In general, dCache doors (FTP, HTTP, dcap, ...) may be configured read-write
(ftp.authz.readonly=false for the FTP door) or read-only
(ftp.authz.readonly=true).  A read-write door allows clients to both read and
modify dCache contents, whereas a read-only door only allows clients to read
contents. All attempts to modify dCache through a read-only door will be
rejected.

Irrespective of whether the door is read-write or read-only, the other
authorisation schemes still apply. For example, a user will still only be able
to read files that the namespace (file and directories) allows. Similarly, a
user can only write into those directories that she is authorised to do so.

Each of the three FTP authentication schemes have independent default
ftp.authz.readonly values. For GSI-FTP and Kerberos-FTP the default is
read-write.  In dCache v2.6, the default for Plain-FTP is read-only. A mistake
was recently discovered where, in dCache v2.7, the default for Plain-FTP
changed to read-write.  This is unintended.

With the release of dCache v2.11.9, 2.10.18, 2.9.21, 2.8.25 and 2.7.29, the
default behaviour for Plain-FTP doors is read-only, in keeping with dCache
v2.6.


Risk category
=============

Since the standard EGI deployment is not vulnerable, we have not carried out a
risk assessment for EGI, but send this advisory in case some sites have a
vulnerable configuration.


Affected software
=================

dCache release 2.7 and higher prior to the fixed releases.

Fixed in releases v2.11.9, 2.10.18, 2.9.21, 2.8.25 and 2.7.29 and higher.


Mitigation
==========

Vulnerable sites should explicitly configured to be read-only.

Alternatively, update to a non-vulnerable version.

Component installation information
==================================

Note that the version in the EGI UMD is not vulnerable.

Sites which have a vulnerable version should see [R 1]



Recommendations
===============

Sites should check whether they allow access to data via plain username and
password.

If sites are allowing username and password access to data then they should
either update to a non-vulnerable version directly from the dCache site [R 1]
or take mitigating action.

Credit
======

This vulnerability was reported by Patrick Fuhrmann and Paul Millar from the
dCache team.


References
==========

[R 1] http://www.dcache.org/downloads/IAgree.shtml


Timeline
========

Yyyy-mm-dd

2015-02-05 Vulnerability reported by Patrick Fuhrmann and Paul Millar
2015-02-05 Acknowledgement from the EGI SVG to the reporter
2015-02-06 Updated packages available at the dCache site
2015-02-20 Alert sent to sites
2015-02-20 Public disclosure.
```
