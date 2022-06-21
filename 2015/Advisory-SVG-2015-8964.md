---
title: Advisory-SVG-2015-8964
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2015-8964]

Title:   EGI SVG Advisory 'High' Risk - OpenStack Cinder CVE-2015-1850
         [EGI-SVG-2015-8964]

Date:    2015-06-23
Updated:


URL:     https://advisories.egi.eu/2015/Advisory-SVG-2015-8964


Introduction
============

Cinder is file management software which is part of OpenStack Cloud software

A vulnerability has been announced in Cinder which may allow authorized users
access to other users files on the Cinder server.

This is only exploitable if a user is able to upload a malicious image. Since
for the EGI Federated cloud only endorsed VMs are allowed, the likelihood of
this being exploited at sites only supporting the EGI Federated cloud is fairly
low. For sites supporting other cloud users as well as EGI Federated Cloud
users, it is more serious.


Details
=======

By overwriting an image with a malicious qcow2 header, an authenticated user
may mislead Cinder upload-to-image action, resulting in disclosure of any file
from the Cinder server. All Cinder setups are affected.

This is only exploitable if a user is able to upload a malicious image. In the
case where sites only support the EGI Federated cloud then it is unlikely that
this vulnerability can be exploited as it would require a malicious image to
get endorsed, which is not particularly likely. For sites supporting other
cloud users, it may put the EGI federated cloud users' files at risk of being
exposed to another malicious user.



Risk category
=============

This issue has been assessed as 'High' by the EGI SVG Risk Assessment Team in
the case where users are allowed to upload their own images when sites are
supporting non-EGI Federated cloud users as well as EGI federated cloud users.


Affected software
=================

OpenStack Cinder


Mitigation
==========

For the EGI Federated Cloud, users are not generally allowed to upload their own
images. Only endorsed VM images in the AppDB are allowed.


Component installation information
==================================

See [R 1]


Recommendations
===============

Sites running Cinder should update as soon as possible if they have not done so
already, urgently if they support users who are not constrained by the EGI
Federated cloud use cases.


Credit
======

EGI SVG alerted to this vulnerability by Vincent Brillault from CERN.

See [R 1] for original reporter.

References
==========

[R 1] https://bugs.launchpad.net/cinder/+bug/1415087

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

We are currently revising the vulnerability issue handling procedure so
suggestions and comments are welcome.



Timeline
========

Yyyy-mm-dd

2015-06-17 SVG alerted to this Vulnerability by Vincent Brillault
2015-06-17 Acknowledgement from the EGI SVG
2015-06-   Discussion with Fed Cloud expert and risk assessment.
2015-06-22 Advisory drafted
2015-06-23 Advisory sent to sites.



On behalf of the EGI SVG,
```
