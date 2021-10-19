---
title: SVG:Advisory-SVG-2017-13915
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] 'Moderate' risk DPM SRM Buffer Overflow  [EGI-SVG-2017-13915]

Date:    2018-04-18
Updated: 2018-05-08 [TLP:WHITE] Public disclosure


Affected software and risk
==========================

MODERATE risk vulnerability concerning DPM SRM Buffer Overflow

Package : DPM
CVE ID  : N/A

A buffer overflow vulnerability has been found in DPM SRM which allows an
authorized user with a client host name longer than 63 characters to crash the
DPM SRM.  It has been inadvertently triggered at a few sites by a legitimate
user.

Actions required/recommended
============================

Sites are recommended to update their DPM servers as soon as possible, to
ensure the service remains available.


Affected software details
=========================

This is fixed as of DPM version 1.9.2.

All versions of the DPM server prior to this version are vulnerable.

More information
================

Investigations into this vulnerability have not shown any exploit more serious
than DoS, and nothing that can lead to access to the DPM host or exposure of
data.

However, it might be very easy to trigger this vulnerability, typically
inadvertently. Hence we are keeping this advisory as 'AMBER' to allow sites to
patch before it is exposed publicly.

**Update 2018-05-08 Advisory made public**


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

This issue is fixed in UMD 4.6.1 where DPM version 1.9.2 has been released

http://repository.egi.eu/2018/03/14/release-umd-4-6-1/


TLP and URL
===========

** WHITE information - Unlimited distribution
- see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2017-13915

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]

Note that this has been updated and the latest version approved by the
Operations Management Board in November 2017


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was reported by Andrea Manzi


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-13915]

2017-12-07 Vulnerability reported by Andrea Manzi, stating that a fix has
           already been produced
2017-12-07 Acknowledgement from the EGI SVG to the reporter
2017-12-08 EGI SVG Risk Assessment completed
2017-12-08 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2018-03-14 Updated packages available in the EGI UMD
2018-04-17 Confirmed that this issue is resolved in DPM 1.9.2
2018-04-18 Advisory sent to sites
2018-05-08 Public disclosure


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group
```
