---
title: Advisory-SVG-2016-11495
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'Moderate' risk vulnerability - VOMS
         server certificate chain/user validation [EGI-SVG-2016-11495]

Date:    2016-11-24
Updated:

Affected software and risk
==========================

MODERATE risk vulnerability concerning VOMS certificate chain/user validation

Package : VOMS
CVE ID  : N/A

The VOMS server may accept proxies that do not comply with RFC 3281, or other
malformed proxies.

It may be possible for VOMS attributes to be obtained with such proxies, but it
is very unlikely that the resulting proxy might be successfully used for
accessing other grid services.
The various security stacks commonly used in grid services were found to

reject such proxies altogether.


Actions required/recommended
============================

Sites are recommended to update relevant components as soon as it is
convenient.

It is not necessary for sites to respond to this e-mail.

Affected software details
=========================

These problems are fixed in VOMS version 2.0.14 or later.


Mitigation
==========

N/A


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/


For CentOS/EL 7 the VOMS server is available in EPEL 7

https://fedoraproject.org/wiki/EPEL


Please note that EMI repository is no longer maintained.


TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2016-11495

Minor updates may be made without re-distribution to the sites

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report

it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=2538


Credit
======

This vulnerability was reported by Georgios Bitzes.


Timeline
========

Yyyy-mm-dd  [EGI-SVG-2016-11495]

2016-08-22 Vulnerability reported by Georgios Bitzes
2016-08-22 Acknowledgement from the EGI SVG to the reporter
2016-08-22 Software providers responded and involved in investigation
2016-08--- Investigation of vulnerability and relevance to EGI carried out
2016-10-05 EGI SVG Risk Assessment completed
2016-10-05 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2016-11-10 Updated packages available in UMD 3 and UMD 4
2016-11-24 Advisory/Alert sent to sites
2016-11-24 Public disclosure

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
```
