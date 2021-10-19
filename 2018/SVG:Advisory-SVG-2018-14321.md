---
title: SVG:Advisory-SVG-2018-14321
permalink: /SVG:Advisory-SVG-2018-14321/
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] LOW risk CREAM command injection attack
         [EGI-SVG-2018-14321]

Date:    2019-11-27
Updated:

Affected software and risk
==========================

LOW risk vulnerability concerning CREAM

Package : CREAM

A 'LOW' risk vulnerability was found which may make CREAM vulnerable to a DoS
attack.

Actions required/recommended
============================

This vulnerability was fixed over a year ago, so most sites will already be
running a non-vulnerable version of CREAM, so will not need to take action.
Sites running CREAM should check that they are running a version of CREAM which
is not vulnerable.

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/


Affected software details
=========================

The fixed version is in [R 1].  This contains the list of components which
constitute the version where the software was fixed.


More information
================

After checking through old tickets it was found that this issue had been fixed
some time ago and SVG was not aware of it.

As this is old and 'LOW' risk this advisory is being placed on the Wiki for
completeness, without sending to sites.

The vulnerability was not mentioned in the release notes for the version of
CREAM in which it was fixed  [R 1]

We note that CREAM is being phased out.


TLP and URL
===========

** WHITE information - Unlimited distribution
  - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2018-14321

Minor updates may be made without re-distribution to the sites

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 2]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.


References
==========

[R 1] https://cream-guide.readthedocs.io/en/latest/Releases.html#release-1-16-7

[R 2] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was alerted to this vulnerability by Jeny Teheran from OSG and Maarten Litmaath


Timeline
========

Yyyy-mm-dd  [EGI-SVG-2018-14321]

2018-05-08 SVG alerted to this issue by Jeny Teheran from OSG and Maarten
           Litmaath
2018-05-08 Acknowledgement from the EGI SVG to the reporter
2018-05-08 Investigation of vulnerability and relevance to EGI carried out,
           only DoS for CREAM.
2018-05-08 EGI SVG Risk Assessment completed
2019-11-20 Checked again with CREAM team after going through 'old' issues
2019-11-21 CREAM team stated that it had been fixed
2019-11-27 Advisory placed on Wiki for completeness


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 2] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
