---
title: Advisory-SVG-2015-10134
---

```
Title:   EGI SVG Advisory [TLP:White] 'Low' risk STORM WebDAV interface XXE
         vulnerability [EGI-SVG-2015-10134]

Date:    2016-06-20
Updated:

Affected Software and Risk
==========================

LOW risk XXE vulnerability concerning STORM WebDAV interface

Package : STORM

Actions Required/Recommended
============================

Sites are recommended to update relevant components in due course.

Affected software Details.
==========================

STORM versions prior to 1.11.10

This is fixed in Version 1.11.10

More information
================

WebDAV is a protocol, based on HTTP, that makes use of XML as a
machine-readable format.  The XML External Entity (XXE) processing feature of
XML make services that use it, like WebDAV, potentially vulnerable to attacks.

An XXE problem was identified with the Milton library. STORM uses this library
to process WebDAV requests.

More information on the XML External Entity Vulnerability is available at [R 1]

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

STORM version 1.11.11 has been placed in the EGI UMD-4

http://repository.egi.eu/2016/05/27/release-umd-4-1-0/

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

STORM version 1.11.11 has been placed in EGI UMD 3.14.2

This may also be upgraded from the StoRM website, - see

http://italiangrid.github.io/storm/2016/01/22/storm-v1.11.10-released.html



TLP and URL
===========

** WHITE information - Unlimited distribution  **

** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions**

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2015-10134

Minor updates may be made without re-distribution to the sites

Credit
======

Andrea Manzi noted that STORM is affected by this vulnerability

References
==========

[R 1] https://www.owasp.org/index.php/XML_External_Entity_(XXE)_Processing

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2015-10134]

2015-12-01 Andrea Manzi noted that STORM is affected by this vulnerability
2015-12-10 EGI SVG Risk Assessment completed
2015-12-10 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2016-01-22 Vulnerability fixed by the STORM developers
2016-06-08 Updated packages available in the EGI UMD 4
2016-06-16 Updated packages available in the EGI UMD 3
2016-06-20 Advisory/Alert sent to sites
2016-06-20 Public disclosure


On behalf of the EGI SVG,
```
