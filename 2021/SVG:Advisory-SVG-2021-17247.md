---
title: SVG:Advisory-SVG-2021-17247
permalink: /SVG:Advisory-SVG-2021-17247/
---

```
Title:   EGI SVG 'ADVISORY' **UPDATE** [TLP:WHITE] HIGH risk - Squid
         Vulnerability  [EGI-SVG-2021-17247]

Date:    2021-05-12
Updated: 2021-06-03


Update 2021-06-03
=================

EGI UMD 4 has been updated with frontier-squid-4.15-1.2 that fixes the
vulnerability.


Affected software and risk
==========================

HIGH risk vulnerability concerning Squid

Package : Squid, including Frontier Squid [R 3] before version 4.15

The Squid project has publicly announced [R 1] new vulnerabilities, one of
which is deemed HIGH risk, viz. CVE-2020-25097 [R 2], because it may allow
services to be exposed that are not directly accessible from the client host.
The other ones only concern potential denial of service and hence are deemed
low risk.


Actions required/recommended
============================

Sites are recommended to update relevant components or apply the mitigation
detailed below as soon as possible.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using frontier-squid from the EGI UMD 4 should see:

    http://repository.egi.eu/sw/production/umd/4/centos7/x86_64/updates/

The fixed version is frontier-squid-4.15-1.2.


Sites installing Squid from anywhere else should see information from their
provider.

Fixed versions (squid-3.5.20-17.el7_9.6) are available for RHEL 7 [R 5], CentOS
7 [R 6], SL 7 [R 7].


Mitigation
==========

For sites that cannot upgrade in a timely manner, temporary workarounds for the
high-risk vulnerability are provided here.

If frontier-squid is used, update customize.sh with the following line and
either reload or restart frontier-squid:

    setoption("uri_whitespace", "deny")



If a plain squid is used instead, set the "uri_whitespace" directive in
squid.conf to either:

    uri_whitespace deny

or

    uri_whitespace encode

and restart the squid service.


Affected software details
=========================

All versions of squid and frontier-squid earlier than 4.15 are affected.


Additional information
======================

Note that exposure of squid services should usually be limited by access
control to addresses within a local area network.


TLP and URL
===========

** WHITE information - Unlimited distribution
 - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2021-17247

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

[R 1] http://lists.squid-cache.org/pipermail/squid-announce/2021-May/000127.html

[R 2] https://github.com/squid-cache/squid/security/advisories/GHSA-jvf6-h9gj-pmj6

[R 3] https://twiki.cern.ch/twiki/bin/view/Frontier/InstallSquid

[R 4] https://documents.egi.eu/public/ShowDocument?docid=3145

[R 5] https://access.redhat.com/errata/RHSA-2021:1135

[R 6] https://lists.centos.org/pipermail/centos-announce/2021-April/048302.html

[R 7] https://listserv.fnal.gov/scripts/wa.exe?A2=ind2104&L=SCIENTIFIC-LINUX-ERRATA&P=1049


Credit
======

SVG was alerted to this vulnerability by Dave Dykstra.

Information on these vulnerabilities contained in this advisory is based on the
corresponding OSG advisory for these vulnerabilities.


Timeline
========

Yyyy-mm-dd  [EGI-SVG-2021-17247]

2021-05-10 SVG alerted to this issue by Dave Dykstra (FNAL)
2021-05-10 Acknowledgement from the EGI SVG to the reporter
2021-05-10 Investigation of vulnerability and relevance to EGI carried out
2021-05-11 EGI SVG Risk Assessment completed
2021-05-11 SVG drafts advisory based on OSG announcement
2021-05-12 Advisory sent to sites
2021-06-03 Update sent to sites


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 4]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

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
