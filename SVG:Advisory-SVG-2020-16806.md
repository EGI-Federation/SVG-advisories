---
title: SVG:Advisory-SVG-2020-16806
permalink: /SVG:Advisory-SVG-2020-16806/
---

Title:       EGI SVG 'ADVISORY' [TLP:WHITE] LOW risk vulnerability in dCache macaroon bearer token validation [EGI-SVG-2020-16806]

Date:        2020-08-17
Updated:


Affected software and risk
==========================

LOW risk vulnerability concerning dCache macaroon bearer token validation

Package : dCache

The macaroons are bearer tokens, that can contain a number of restrictions, like READ-ONLY, VALID-UNTIL, LIMITED-TO-IP.
The result of IP based verification is not respected when it is combined with other restrictions.

For more information see [R 1].


Actions required/recommended
============================

Sites are recommended to update relevant components as soon as it is convenient.

Sites may update either from the UMD or from the dCache site [R 1]


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites is
repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

A fixed version dCache - 5.2.26 is available in the UMD for both SL6 and CentOS7 in UMD-4.11.2

http://repository.egi.eu/2020/08/14/release-umd-4-11-2/

Sites installing directly from dCache should see [R 1].


More Information
================

The macaroon based tokens are used by quite a small number of sites and IP restrictions are used even less.
Few sites are likely to be affected by this vulnerability.

Affected software details
=========================

This is fixed in dcache versions  5.2.26, 6.0.20, 6.1.9 and 6.2.1.

Previous supported versions  5.2.x, 6.0.x, 6.1.x and 6.2.x are all affected.

Versions 5.1.x are affected, but these have not been patched as the dCache team is not aware of any production instances using them.

Versions before 5.1.0 are not affected.

TLP and URL
===========

** WHITE information - Unlimited distribution
  - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions***

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2020-16806

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the procedure defined in [R 2]

Note that this is undergoing revision to fully handle vulnerabilities in the EOSC-hub era.


References
==========

[R 1] https://www.dcache.org/

[R 2] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was reported to SVG by Tigran Mkrtchyan from the dCache team, who have already produced a fix.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2020-16806]

2020-08-04 Vulnerability reported by Tigran Mkrtchyan from the dCache team.
2020-08-04 Acknowledgement from the EGI SVG to the reporter
2020-08-04 Investigation of vulnerability and relevance to EGI carried out by (as appropriate)
2020-08-05 EGI SVG Risk Assessment completed
2020-08-05 Assessment by the EGI Software Vulnerability Group reported to the software providers
2020-08-07 Updated packages available at the dCache site
2020-08-14 Updated packages updated in the EGI UMD
2020-08-17 Advisory sent to sites


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's purpose
"To minimize the risk to the EGI infrastructure arising from software vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling procedure [R 2]
 in the context of how the software is used in the EGI infrastructure. It is the opinion of the group, we do not guarantee it to be correct.
The risk may also be higher or lower in other deployments depending on how the software is used.

This advisory is subject to the Creative commons license https://creativecommons.org/licenses/by/4.0/ and
the EGI https://www.egi.eu/ Software Vulnerability Group must be credited.


Note that the SVG issue handling procedure is currently under review, to take account of the increasing inhomogeneity
of the EGI infrastructure and the services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
