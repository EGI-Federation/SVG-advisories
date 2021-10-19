---
title: SVG:Advisory-SVG-2017-12435
permalink: /SVG:Advisory-SVG-2017-12435/
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'LOW' risk Remote authenticated DoS on
         CREAM-CE [EGI-SVG-2017-12435]

Date:    2018-12-14
Updated:


Affected software and risk
==========================

LOW risk vulnerability concerning CREAM CE

Package : CREAM CE
CVE ID  : N/A

A vulnerability has been found on the CREAM CE which allows remote DoS.
This has been demonstrated by a member of the EGI SVG.
No exploit has been found beyond DoS and it can only be exploited by an
authenticated and authorized user.

Actions required/recommended
============================

Sites are recommended to update CREAM in due course if they have not done so
since July 2018.

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

This issue is fixed at least in Version 1.16.5-5 released on 24th July 2018 as
part of UMD 4.7.1 Earlier versions may be vulnerable.

TLP and URL
===========

** WHITE information - Unlimited distribution -
   see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions**

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2017-12433

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 2]
Note that this has been updated and the latest version approved by the
Operations Management Board in November 2017



References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=2538

[R 2] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was reported by Simon Fayer who carried out a thorough
investigation.

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2017-12435]

2017-02-21 Vulnerability reported by Simon Fayer who is a member of SVG
2017-02-21 Acknowledgement from the EGI SVG to the reporter
2017-02-23 Software developers involved.
2017-03-22 EGI SVG Risk Assessment completed
2017-03-31 Assessment by the EGI Software Vulnerability Group reported to
           the software providers
2018-07-13 Checked with development team, issue fixed but not released.
2018-12-07 Confirmed fix released in current UMD release.
2018-12-14 Advisory placed on wiki



Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, in the context of how the software is
used in the EGI infrastructure. It is the opinion of the group, we do not
guarantee it to be correct.
The risk may also be higher or lower in other deployments depending on how the
software is used.
This was handled according to the EGI SVG issue handling procedure [R 1] which
has since been replaced by [R 2] approved by the Operations Management Board in
November 2017.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group


On behalf of the EGI SVG,
```
