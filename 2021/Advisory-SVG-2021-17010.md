---
title: Advisory-SVG-2021-17010
---

```
Title:   EGI SVG 'ADVISORY' [TLP:AMBER] HIGH risk VOMS-Admin vulnerability
         [EGI-SVG-2020-17010]

Date:    2021-06-08
Updated:


Affected software and risk
==========================

HIGH risk vulnerability affecting VOMS-Admin

Packages : VOMS-Admin and Apache Struts
CVE ID   : (Struts CVE) CVE-2020-17530

A serious vulnerability has been found in Apache Struts [R 1] [R 2] on which
VOMS-Admin is dependent.
So far no way has been found to exploit this vulnerability via VOMS-Admin.
VOMS-Admin has nonetheless been updated to use the Struts version in which this
vulnerability has been eliminated.

Actions required/recommended
============================

Sites running VOMS-Admin should update to voms-admin-server 3.8.1 (which uses
Struts 2.5.26) as soon as they reasonably can if they have not done so already.

There is the possibility that this vulnerability could be raised to 'Critical'
if a way were to be found to exploit this vulnerability in the context of
VOMS-Admin, in which case sites would be required to update urgently.

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

(although at present this is not available)

The updated version of the RPM is at:--

http://repository.egi.eu/sw/production/umd/4/centos7/x86_64/updates/


Affected software details
=========================

Apache Struts 2.5.25 is found to contain a serious vulnerability.

voms-admin-server 3.8.1 has been fixed to use Struts 2.5.26 which does not
contain this vulnerability.

Earlier versions may be vulnerable.


More information
================

The version of Apache Struts used by voms-admin-server 3.8.0 contains a serious
vulnerability.

The VOMS team have produced a new version (3.8.1) which uses Apache Struts
2.5.26 which does not contain this vulnerability, therefore sites are
recommended to update to voms-admin-server 3.8.1.

So far, no way has been found to exploit this vulnerability when using
VOMS-Admin.


TLP and URL
===========

** AMBER information - Limited distribution
 - see https://go.egi.eu/tlp for distribution restrictions **

This advisory will be placed on the wiki on or after 2021-06-22

URL:   https://advisories.egi.eu/2021/Advisory-SVG-2021-17010

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

[R 1] https://nvd.nist.gov/vuln/detail/CVE-2020-17530

[R 2] https://cwiki.apache.org/confluence/display/WW/S2-061

[R 3] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was alerted to the Struts vulnerability by David Crooks, Andrea Ceccanti
confirmed that VOMS-Admin uses Struts.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2021-17010]

2020-12-15 SVG alerted to the Struts vulnerability by David Crooks.
2021-12-15 Acknowledgement from the EGI SVG to the reporter
2021-12-15 Andrea Ceccanti confirmed that VOMS-Admin relies on Struts and
           involved in the investigation
2021-12--- No means of exploiting via VOMS-Admin found
2021-02-22 EGI SVG Risk Assessment completed - assessed as 'HIGH' because
           serious, but lacking exploit
2021-02-22 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2021-04-28 Updated packages available in the EGI UMD
2021-06-07 SVG checking open issues, found that this had been fixed.
2021-06-08 Advisory sent to sites

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 3] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.  The risk may also be higher or lower in other deployments depending
on how the software is used.

-----------------------------
Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group
------------------------------

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
