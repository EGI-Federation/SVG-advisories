---
title: Advisory-SVG-2017-12728
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'LOW' risk - XROOTD potential for remote
         code execution  [EGI-SVG-2017-12728]

Date:    2017-08-22
Updated:


Affected software and risk
==========================

LOW risk vulnerability concerning XROOTD

Package : XROOTD
CVE ID  : N/A
Bug ID  : N/A

A vulnerability was reported where unauthenticated remote code execution in
some configurations may be possible. However, there is no practical way to
exploit this vulnerability.  The faulty code is no longer being used.


Actions required/recommended
============================

Sites are recommended to update relevant components as soon as it is
convenient.


Affected software details
=========================

This vulnerability has been fixed in xrootd version 4.6.1.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

This update is in UMD 4.5.0:

http://repository.egi.eu/2017/08/10/release-umd-4-5-0/

Please note the EMI repositories are no longer maintained and may no longer be
used.


TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2017-12728

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

SVG was alerted to this vulnerability by Vincent Brillault

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-12728]

2017-04-19 SVG alerted to this issue by Vincent Brillault
2017-04-19 Acknowledgement from the EGI SVG to the reporter
2017-06-19 Reporter said it has been fixed by the developers
2017-06-19 EGI SVG Risk Assessment completed
2017-08-11 Updated packages available in the EGI UMD.
2017-08-22 Advisory placed on wiki only



Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1]  in the context of how the software is used in the EGI
infrastructure.  It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```
