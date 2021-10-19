---
title: SVG:Advisory-SVG-2015-8706
permalink: /SVG:Advisory-SVG-2015-8706/
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2015-8706]

Title:   EGI SVG Advisory - Up to 'High' RISK - Persistent XSS in OpenStack
         Horizon admin dashboard. CVE-2015-3988 [EGI-SVG-2015-8706]

Date:    2015-06-05
Updated:

URL:     https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2015-8706

Introduction
============

SVG has been alerted to a Persistent XSS in OpenStack in Horizon admin
dashboard, in the image metadata pannel.

This may allow privilege escallation.




Details
=======

See [R 1] [R 2] and [R 3]



One member of our team looked at the patch and the vulnerability and the attack
scenario would be:
- An authenticated user adds malicious metadata to an image (via the APIs)
- An admin go on the admin panel, then select this very image and look/edit its
- metadata, the stored XSS will
only be exposed in a page specific to the image, not a summary.

On one site which was investigated, the Horizon admin dashboard was disabled.


Risk category
=============

It is not clear that it is all that easy to exploit this issue in the EGI
infrastructure.
However, to be cautious it should be considered  'High' risk if sites are
running OpenStack and the Horizon admin dashboard is enabled.



Affected software
=================


Horizon metadata dashboard.


Mitigation
==========

Sites running OpenStack with the horizon metadata dashboard may disable the
horizon metadata dashboard.


Component installation information
==================================

See OpenStack instructions.


Recommendations
===============

Sites running OpenStack with the horizon metadata dashboard enabled should
consider either updating or disabling the horizon metadata dashboard.


Credit
======

SVG was alerted to this vulnerability  by Alvaro Lopez Garcia


References
==========

[R 1] https://security.openstack.org/ossa/OSSA-2015-009.html

[R 2] https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2015-3988

[R 3] Wiki XSS description - http://en.wikipedia.org/wiki/Cross-site_scripting


Comments
========

Comments or questions should be sent to svg-rat at mailman.egi.eu

We are currently revising the vulnerability issue handling procedure so
suggestions and comments are welcome.



Timeline
========
Yyyy-mm-dd

2015-05-28 SVG alerted to this publicly announced Vulnerability by Alvaro Lopez
           Garcia
2015-05-28 Acknowledgement from the EGI SVG
2015-05--- Discussions on impact and risk in EGI
2015-06-04 Advisory drafted
2015-06-05 Advisory sent to sites



On behalf of the EGI SVG,
```
