---
title: Advisory-SVG-2016-11190
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'HIGH' risk - Authorization by user_id to
         manage VMs does not work in V2.1 Nova API for OpenStack
         [EGI-SVG-2016-11190]

Date:    2016-06-07
Updated:

Affected software and risk
==========================

'High' risk vulnerability concerning OpenStack VM management Authorization by
individual user.

Package : OpenStack
CVE ID  : N/A - functionality removed
Bug ID  : OpenStack - https://bugs.launchpad.net/nova/+bug/1539351

Authorization to manage Virtual Machines by individual user_id does no longer
work in V2.1 Nova API for OpenStack. This implies for EGI that users within a
VO can for example delete VMs which do not belong to them, causing a DoS.

Actions required/recommended
============================

For the time being, sites should not upgrade to V2.1 of the Nova API for
OpenStack.

If sites have already upgraded to V2.1 of the Nova API for OpenStack, they
should downgrade to 2.0.

Affected software details
=========================

OpenStack Version 2.1

More information
================

See the bug report [R 1]

The risk may be elevated to 'Critical' if it is found that users are able to
take over other users VMs.

A more permanent solution is being worked on.

There is also a patch provided by CNRS to re-enable the user based
authorization, it may be an alternative to downgrading but we have had no
reports of testing yet. See [R 2]

Mitigation
==========

N/A

Component installation information
==================================

See the OpenStack site.

TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://go.egi.eu/tlp for distribution restrictions **


URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2016-11190

Minor updates may be made without re-distribution to the sites

Credit
======

SVG was alerted to this issue by the EGI Federated Cloud team

References
==========

[R 1] https://bugs.launchpad.net/nova/+bug/1539351

[R 2] https://github.com/vin-c/cloud-security/tree/liberty/patch

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2016-11190]

2016-01-29 Deprecated functionality bug opened on OpenStack webpage.
2016------ Software providers involved in investigation
2016-05-31 This issue discussed at the EGI Federated Cloud Task force meeting
2016-06-02 Issue entered as a vulnerability
2016-06-03 SVG agreed an advisory should be issued to sites.
2016-06-06 EGI SVG Risk Assessment completed
2016-06-07 Advisory/Alert sent to sites
```
