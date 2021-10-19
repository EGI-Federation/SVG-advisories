---
title: SVG:Advisory-SVG-2016-11839
permalink: /SVG:Advisory-SVG-2016-11839/
---

```
Title:   EGI SVG Advisory [TLP:WHITE] LOW risk vulnerability - VOMS Admin
         allows VO membership requests from users without a certificate
         [EGI-SVG-2016-11839]

Date:    2017-08-07
Updated:


Affected software and risk
==========================

LOW risk vulnerability concerning VOMS Admin

Package : VOMS Admin
CVE ID  : N/A
Bug ID  : N/A

A vulnerability was found where a user without a valid certificate could
request membership of a VO, and the request be forwarded to the VO
administrator.  Borderline between just a bug and a 'low' risk vulnerability.


Actions required/recommended
============================

None as this was fixed some time ago and sites have been instructed to update
to more recent versions since this was fixed. This is for info/completeness and
to credit the reporter only.

Affected software details
=========================

Versions of VOMS Admin earlier than 3.5.0. This was fixed in Version 3.5.0.

TLP and URL
===========

** WHITE information - Unlimited distribution - see

https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions***

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2016-11839

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=2538

Credit
======

This vulnerability was discovered by Marco Verlato from INFN, Vincent Brillault
alerted SVG

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2016-11839]

2016-10-13 Vulnerability reported by Marco Verlato.
2016-10-13 Acknowledgement from the EGI SVG to the reporter
2016-10-20 EGI SVG Risk Assessment completed
2016-11-16 Updated packages available in the EGI UMD
2017------ More serious issues dealt with
2017-08-07 Advisory on wiki for completeness, and to credit the reporter.



Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1]  in the context of how the software is used in the EGI
infrastructure.

It is the opinion of the group, we do not guarantee it to be correct. The risk
may also be higher or lower in other deployments depending on how the software
is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group

On behalf of the EGI SVG,
```
