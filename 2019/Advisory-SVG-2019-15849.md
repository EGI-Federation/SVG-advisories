---
title: Advisory-SVG-2019-15849
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] HIGH risk Frontier-Squid-4
         vulnerability [EGI-SVG-2019-15849]

Date:    2019-07-26
Updated: 2019-11-11 TLP changed to white and placed on wiki


Affected software and risk
==========================

HIGH risk Frontier-Squid vulnerability

Package : frontier-squid-4.*

See OSG security team information provided below.


Actions required/recommended
============================

Sites running frontier-squid-4.* should upgrade at least to
frontier-squid-4.4-2.1, available in UMD-4 both for CentOS 7 and SL6.
 Further details are provided below.


OSG security team information
=============================

The frontier-squid package has a publicly announced security vulnerability that
can potentially enable remote code execution from any IP address that access
control allows to use the squid.  All sites that have frontier-squid-4.*
versions should upgrade urgently, especially those that have squids that can be
used from the internet.

IMPACTED VERSIONS:

frontier-squid-4.*

WHAT ARE THE VULNERABILITIES:

Due to incorrect buffer management, squid is vulnerable to a heap overflow and
possible remote code execution attack when processing HTTP Authentication
credentials. This happens when squid is asked to proxy ftp, which it allows by
default.

WHAT YOU SHOULD DO:

If you have frontier-squid-4.* installed, upgrade to a version where the
vulnerability is removed.
OSG has released frontier-squid-4.4-2.1 which only adds a patch for this
problem to version 4.4-1.1.
Upstream had previously released 4.6 versions which are also vulnerable. The
upstream frontier-squid-4.8-1.1 version fixes this problem in addition to
including other features and bug fixes. So upgrade to either version OSG
frontier-squid-4.4-2.1 or upstream 4.8-1.1.

REFERENCES

[1]. http://www.squid-cache.org/Advisories/SQUID-2019_5.txt
[2]. http://frontier.cern.ch/dist/rpms/frontier-squidRELEASE_NOTES


Further information for EGI sites
=================================

The vulnerability in frontier-squid-4.* originates from squid-4.*, which is
unlikely to be in use at EGI sites, because the squid versions that come with
CentOS 7 and SL6 are still in the 3.* series, which do not have the
vulnerability.

Sites running squid-4.* should either upgrade or downgrade to a version that
does not have the vulnerability (see [1]), or change to frontier-squid-4.4-2.1
or 4.8-1.1.


TLP and URL
===========

** AMBER information - Limited distribution
- see https://go.egi.eu/tlp for distribution restrictions **

URL:   https://advisories.egi.eu/2019/Advisory-SVG-2019-15849

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 3]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.


References
==========

[R 3] https://documents.egi.eu/public/ShowDocument?docid=3145


Credit
======

SVG was alerted to this vulnerability by David Dykstra from FNAL / OSG.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2019-15849]

2019-07-17 SVG alerted to this issue by David Dykstra
2019-07-17 Acknowledgement from the EGI SVG to the reporter
2019-07-18 Decision to wait for pending updates of the OSG and UMD
           repositories.
2019-07-25 OSG prepared announcement of the vulnerability with actions to take.
2019-07-26 SVG informed sites as 'AMBER', incorporating the OSG information.
2019-11-11 TLP changed to [WHITE] and placed on SVG public wiki

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 3]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.
The risk may also be higher or lower in other deployments depending on how the
software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
