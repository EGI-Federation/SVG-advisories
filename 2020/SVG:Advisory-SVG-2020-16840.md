---
title: SVG:Advisory-SVG-2020-16840
permalink: /SVG:Advisory-SVG-2020-16840/
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] MODERATE risk - Cache Poisoning Squid
         Vulnerabilities  [EGI-SVG-2020-16840]

Date:    2020-09-16
Updated:

Affected software and risk
==========================

MODERATE risk vulnerabilities concerning Squid

Package : Squid, including Frontier Squid before version 4.13

The Squid project has publicly announced new vulnerabilities that can result in
Cache poisoning.


Actions required/recommended
============================

Sites are recommended to update relevant components as soon as it is convenient


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

Where Frontier Squid 4.13-1.1 is available in the EGI UMD for SL6 and Centos7
as part of UMD-4.11.3

https://repository.egi.eu/2020/09/15/release-umd-4-11-3/

Sites installing Squid from anywhere else should see information from their
provider.

NOTE: The squid will be out of service for about a minute during the upgrade.


Mitigation
==========

For sites that cannot upgrade in a timely manner, a temporary workaround for
the vulnerabilities is to add the option
        setoption("relaxed_header_parser", "off") to /etc/squid/customize.sh
        and reload the squid with
        service frontier-squid reload
This has been tested with CVMFS and Frontier but may impact other applications
using the squid.


Affected software details
=========================

All versions of squid and frontier-squid earlier than 4.13 are affected.


Background information
======================

Two announced vulnerabilities, one for request splitting [R 1] and one for
request smuggling [R 2] can both lead to cache poisoning.  Cache poisoning will
lead to only denial of service for CVMFS, but could potentially be more serious
for the Frontier application used by CMS and ATLAS, or for other applications
that might be using the squid.  Note that exposure to squids is usually limited
by access control to addresses within a local area network.


TLP and URL
===========

** WHITE information - Unlimited distribution
 - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2020-16840

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 4]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.


References
==========

[R 1] https://github.com/squid-cache/squid/security/advisories/GHSA-c7p8-xqhm-49wv

[R 2] https://github.com/squid-cache/squid/security/advisories/GHSA-3365-q9qx-f98m

[R 3] https://opensciencegrid.org/docs/data/frontier-squid

[R 4] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was alerted to this vulnerability by Dave Dykstra.

Information on these vulnerabilities contained in this advisory is based on the
corresponding OSG advisory for these vulnerabilities.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2020-16840]

2020-08-24 SVG alerted to this issue by Dave Dykstra
2020-08-25 Acknowledgement from the EGI SVG to the reporter
2020-08-25 Investigation of vulnerability and relevance to EGI carried out
2020-08-26 EGI SVG Risk Assessment completed
2020-09-03 SVG drafts advisory based on OSG announcement
2020-09-15 Updated packages available in the EGI UMD
2020-09-16 Advisory sent to sites

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 4]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.  The risk may also be higher or lower in other deployments depending
on how the software is used.

-----------------------------
This advisory is subject to the Creative commons license
https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/
Software Vulnerability Group must be credited.
-----------------------------

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
