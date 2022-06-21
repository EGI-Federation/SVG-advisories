---
title: Advisory-SVG-2017-12276
---

```
Title:   EGI SVG Advisory 'HIGH' risk canl-c impersonation vulnerability
         [EGI-SVG-2017-12276]

Date:    2017-03-24
Updated: 2017-06-01 - Changed to 'WHITE'


Affected software and risk
==========================

'HIGH' risk impersonation vulnerability concerning canl-c.

Package : canl-c
CVE ID  : N/A

A vulnerability has been found which may allow a user to impersonate another
user where it is hard to trace the origin.
This is present in all recent versions of canl-c.

Actions required/recommended
============================

Sites running services depending on canl-c should update as soon as possible.

Please ensure all potentially affected services are restarted after the update.
In particular for the DPM, FTS, and LFC:

     service httpd restart

Affected software details
=========================

This is fixed in canl-c version 2.1.8-1. Earlier versions are all likely to be
affected.

Affected software particularly includes anything which uses canl-c via
GridSite:

    DPM

    LFC

    FTS - but only in limited circumstances.

    WMS - ditto

CREAM also uses gridsite and canl-c, but happens not to be vulnerable.


More information
================

This exploit has been demonstrated to exist by the reporter.

The mitigating circumstances are that the issue is difficult to find, there is
no public information on it, and the exploit requires a valid certificate from
a trusted CA.

If information on how to exploit this were to become public, then it will be
raised to 'Critical'.

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

This is fixed in UMD 4.4.0

http://repository.egi.eu/2017/03/23/release-umd-4-4-0/


This has also been released in EGI UMD 3:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

This is fixed in UMD 3.14.8

http://repository.egi.eu/2017/03/16/release-umd-3-14-8/


Please note the EMI repositories are no longer maintained.



TLP and URL
===========

** WHITE information - Unlimited distribution
- see https://go.egi.eu/tlp for distribution restrictions  **

URL:   https://advisories.egi.eu/2017/Advisory-SVG-2017-12276

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

This vulnerability was reported by Georgios Bitzes

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2017-12276]

2017-01-16 Vulnerability reported by Georgios Bitzes who is a member of SVG.
2017-01-16 Acknowledgement from the EGI SVG to the reporter
2017-01-20 Software providers responded and involved in investigation
2017------ Investigation of vulnerability and relevance to EGI carried out
2017-02-09 EGI SVG Risk Assessment completed
2017-02-09 Assessment by the EGI Software Vulnerability Group reported to
           the software providers
2017-03-23 Updated packages available in UMD-3 and UMD-4
2017-03-24 Advisory/Alert sent to sites
2017-06-01 Public disclosure on Wiki


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group


On behalf of the EGI SVG,
```
