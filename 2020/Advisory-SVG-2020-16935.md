---
title: Advisory-SVG-2020-16935
permalink: /Advisory-SVG-2020-16935
---

## Advisory-SVG-2020-16935

```
Title:   EGI SVG 'ADVISORY' **UPDATE** [TLP:WHITE] CRITICAL risk DPM
         vulnerability allowing file deletion [EGI-SVG-2020-16935]

Date:    2020-11-06
Updated: 2021-03-23


Affected software and risk
==========================

CRITICAL risk vulnerability concerning DPM 1.14.0 and 1.14.1

Package : DPM

A vulnerability in DPM 1.14.0 and 1.14.1 allows users to delete other users'
files.
This vulnerability is not present in versions of DPM prior to 1.14.0.

Actions required/recommended
============================

Sites who have installed DPM 1.14.0 or 1.14.1 should take urgent action.

DPM version 1.14.2, which contains a fix for this vulnerability, is available
from EPEL for RHEL/SL/CentOS 7.

It is sufficient for sites just to upgrade the head nodes to address this
vulnerability.

Component installation information
==================================

Sites installing DPM from EPEL should see

https://fedoraproject.org/wiki/EPEL

https://dl.fedoraproject.org/pub/epel/7/x86_64/Packages/d/

Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

Note that at present DPM 1.13.0 is the version in the EGI UMD.

Also note sites should have already migrated from SL6 and its derivatives.


Mitigation
==========

We are not currently aware of any mitigating action.


Affected software details
=========================

This vulnerability affects only DPM versions 1.14.0 and 1.14.1. It is fixed in
DPM 1.14.2.

Earlier versions of DPM are not affected.

Other Information
=================

** UPDATE 2021-03-23 **

Previously there were problems with the configuration required by CMS.

This has been resolved. This was fixed with xrootd 5.0.3-2 rebuild.

When the advisory was sent to sites, it additionally referred to RedHat 6 and
its derivatives, since this is past its end of life and sites should no longer
be using it this has been removed.

TLP and URL
===========

** WHITE information - Unlimited distribution
 - see https://go.egi.eu/tlp for distribution restrictions **

URL:   https://advisories.egi.eu/Advisory-SVG-2020-16935

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was reported to SVG by Matt Doidge


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2020-16935]

2020-10-29 Vulnerability reported by Matt Doidge
2020-10-29 Acknowledgement from the EGI SVG to the reporter
2020------ Software providers responded and involved in investigation
2020------ Investigation of vulnerability and relevance to EGI carried out
2020-11-02 Fixed version in EPEL testing for RH7 and derivatives
2020-11--- Discussion on situation, clarification of affected versions, and
           actions to take.
2020-11-04 EGI SVG Risk Assessment completed
2020-11-05 Further discussions on what to recommend to sites
2020-11-06 Initial Advisory sent to sites
2021-03-23 Advisory placed on SVG wiki after checking issue with CMS fully resolved.

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.


-----------------------------
This advisory is subject to the Creative commons licence
https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/
Software Vulnerability Group must be credited.
-----------------------------

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
