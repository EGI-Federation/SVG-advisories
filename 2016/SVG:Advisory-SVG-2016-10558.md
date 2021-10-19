---
title: SVG:Advisory-SVG-2016-10558
permalink: /SVG:Advisory-SVG-2016-10558/
---

```
Title:   EGI SVG Advisory - 'Moderate' risk KeyStone VOMS does not check CRLs
         [EGI-SVG-2016-10558]

Date:    2016-08-08
Updated: 2016-08-25 (TLP changed to 'WHITE' and placed on wiki)

Affected Software and Risk
==========================

MODERATE risk vulnerability concerning Keystone VOMS (Used in the EGI Federated
Cloud with OpenStack)

Package :Keystone VOMS
CVE ID  :N/A

Keystone VOMS [R 1] does not check the Certificate Revocation Lists (CRL),
hence access may be granted using certificates which have been revoked.

Actions Required/Recommended
============================

Sites are recommended to update relevant components as soon as is convenient.

If sites are running a version of OpenStack earlier than Liberty or Mitaka they
should migrate to one of these versions as soon as is convenient.

Affected software Details
=====================

All Keystone VOMS versions prior to 8.0.3. Versions equal or newer than 8.0.3
are not affected.

More information
================

Keystone VOMS enables authentication and authorization for sites running
OpenStack using VOMS credentials, this is available in the EGI AppDB [R 1]

A vulnerability has been found such that Keystone VOMS does not check the
Certificate Revocation

Lists (CRL), hence access may be granted via certificates which have been
revoked.

This has been fixed and sites are recommended to update relevant components as
soon as is convenient.

Sites should note that the non-vulnerable version of Keystone VOMS only
supports the more recent versions of OpenStack, i.e. the versions supported by
OpenStack itself see [R 2] and sites should migrate to a supported version as
soon as is convenient.

Software to be used on top of OpenStack (including KeyStone VOMS) to enable the
EGI Federated

Cloud will be placed in the EGI Cloud Middleware Distribution (CMD) in the
coming months. This will follow the OpenStack support schedule. [R 2]

Hence tools which work with older versions of OpenStack, such as those provided
by Ubuntu [R 4] will not be maintained.


Mitigation
==========

N/A.


Component installation information
==================================

See [R 1]  [R 3]

Also note that sites in the EGI Federated Cloud runing OpenStack should be
using versions of

OpenStack which are currently under security support by OpenStack itself, at
present this is

'Liberty' and 'Mitaka' and not other versions which are supported elsewhere,
such as by Ubuntu [R 4]

For sites running OpenStack Liberty, the version of KeyStone VOMS which should
be used is 8.0.3 or greater [R 4]

For sites running OpenStack Mitaka, the version of KeyStone VOMS which should
be used is 9.0.0 or greater [R 5]

Note that although the status of the fixed releases are 'Candidate', we
recommend updating anyway.


TLP and URL
===========

** WHITE information -  Unlimited Distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

This advisory will be placed on the wiki on or after 2016-08-22

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2016-10558

Minor updates may be made without re-distribution to the sites

Credit
======

This vulnerability was reported by Mischa Salle who is a member of SVG.

References
==========

[R 1] https://appdb.egi.eu/store/software/keystone.voms

[R 2] http://releases.openstack.org/

[R 3] https://keystone-voms.readthedocs.org/en/stable-liberty/

[R 4] https://wiki.ubuntu.com/OpenStack/CloudArchive

[R 5] https://appdb.egi.eu/store/software/keystone.voms/releases/stable-liberty/

[R 6] https://appdb.egi.eu/store/software/keystone.voms/releases/stable-mitaka/

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-10558]

2016-02-24 Vulnerability reported by Mischa Salle
2016-02-25 Acknowledgement from the EGI SVG to the reporter
2016-02-25 Software providers responded and reported they are aware of problem,
           and in work
2016-03-01 EGI SVG Risk Assessment completed
2016-03-30 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2016-07-26 Updated packages available in the EGI AppDB
2016-08-08 Advisory/Alert sent to sites
2016-08-25 Public disclosure
```
