---
title: SVG:Advisory-SVG-2017-12319
---

```

Title:   EGI SVG Advisory [TLP:WHITE] 'MODERATE' risk ARC 5.2.1 World Writeable
         log directory  [EGI-SVG-2017-12319]
Date:    2017-08-07
Updated:


Affected software and risk
==========================

MODERATE risk vulnerability concerning ARC

Package : ARC
CVE ID  : N/A
Bug ID  :

A world writeable log directory was introduced in ARC 5.2.1.


Actions required/recommended
============================

Sites running ARC 5.2.1 are recommended to update to ARC 5.2.2 as soon as is
convenient.

Affected software details
=========================

This vulnerability was introduced in ARC 5.2.1.  It is only present in this
version.

Mitigation
==========

Likely configurations at sites make it difficult to exploit.

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD.


Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Note that an older version of ARC which does not contain this vulnerability is
in UMD 3


TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2017-12319


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=2538

Credit
======

This vulnerability was reported by Ulf Tigerstedt


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-12319]

2017-01-24 Vulnerability reported by Ulf Tigerstedt
2017-01-25 Acknowledgement from the EGI SVG to the reporter
2017-01-25 Software providers responded and involved in investigation
2017-01-25 Investigation of vulnerability and relevance to EGI carried out by
2017-02-15 EGI SVG Risk Assessment completed
2017-02-15 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2017-02-15 Software updated by software providers
2017-04-04 Updated packages available in the EGI UMD
2017-08-07 Advisory on public wiki


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
