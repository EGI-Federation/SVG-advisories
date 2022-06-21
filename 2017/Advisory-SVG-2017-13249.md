---
title: Advisory-SVG-2017-13249
---

```
Title:   EGI SVG Advisory [TLP:WHITE] VOMS Admin privilege escalation
         vulnerability [EGI-SVG-2017-13249]

Date:    2018-02-07
Updated: 2018-03-05 (made public, changed to TLP:WHITE)

Affected software and risk
==========================

MODERATE risk vulnerability concerning VOMS Admin version 3.6.0

Package : VOMS Admin
CVE ID  : N/A
Bug ID  : N/A

A privilege escalation vulnerability has been found in voms-admin 3.6.0 which
allows a user registered in a VO to gain the VOAdmin role and therefore become
a VO administrator.

This has been fixed in voms-admin version 3.7.0


Actions required/recommended
============================

Sites running VOMS Admin are recommended to update relevant components as soon
as it is convenient if they have not done so already.


Affected software details
=========================

This vulnerability was found in VOMS Admin 3.6.0.  Earlier versions may be
affected but this has not been established.

This vulnerability is fixed in VOMS Admin version 3.7.0


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

VOMS admin version 3.7.0 which fixes this vulnerability is in UMD 4.6.0

http://repository.egi.eu/2017/12/18/release-umd-4-6-0/


TLP and URL
===========

** WHITE information - unlimited distribution -
see https://go.egi.eu/tlp for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2017-13249

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

[R 1] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was discovered and reported by Vincenzo Ciaschini


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-13249]

2017-07-19 Vulnerability reported by Vincenzo Ciaschini
2017-07-19 Acknowledgement from the EGI SVG to the reporter
2017-07-19 Software providers responded and involved in investigation
2017-08-01 VOMS team announced that vulnerability fixed, and the fix tested by
           the reporter
2017-08-01 EGI SVG Risk Assessment completed
2017-08-03 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2017-12-18 Updated packages available in the EGI UMD.
2018-02-02 UMD release 4.6.0 Broadcast
2018-02-07 Advisory sent to sites
2018-03-05 Public disclosure


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1] in the context of how the software is used in the EGI
infrastructure.
It is the opinion of the group, we do not guarantee it to be correct.
The risk may also be higher or lower in other deployments depending on how the
software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group
```
