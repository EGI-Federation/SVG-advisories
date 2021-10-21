---
title: Advisory-SVG-2012-4073
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2012-4073]

Title: Critical Risk - EMI-1 WMS proxy theft vulnerability - update and wider
       distribution.

Date:    2012-07-15
Updated: 2012-07-16, 2012-08-13, 2012-08-28


URL: https://wiki.egi.eu/wiki/Advisory-SVG-2012-4073

Introduction
============

This advisory is updated because the vulnerability is now fixed in the version
of WMS available in the EGI UMD.

A vulnerability has been found in the EMI-1 WMS, including the version
distributed in the EGI UMD, that allows an authorized user of a supported VO to
access proxies belonging to other authorized users who recently submitted jobs
to a vulnerable WMS instance.

This is in addition to the Vulnerability 4039.

Sites which have been found to be vulnerable have already been contacted
individually by the CSIRT team, so most sites are not currently vulnerable.

Previously sites which updated from gLite 3.1 to the EMI-1 WMS in the EGI UMD
as suggested in the advisory for 4039 would find themselves vulnerable to 4073.

Now this vulnerability has been fixed in the version of EMI-1 WMS in the EGI
UMD.


Details
=======

A vulnerability has been found in WMS which allows any authorized user of a
supported VO read access to proxies belonging to other authorized users.
This could allow an authorized user to impersonate another authorized user.

This is in addition to vulnerability 4039, which also allows proxy theft.

Sites vulnerable shortly after the vulnerability was discovered were contacted
directly by CSIRT and asked to take mitigating action.

This vulnerability has now been fixed in the version of the software available
in the EGI UMD.

Risk Category
=============

This issue has been assessed as "Critical/High" risk by the EGI SVG Risk
Assessment Team.

Affected Software
=================

This issue is fixed in UMD-1 WMS version 3.3.7 as distributed in the EGI UMD
release 1-8-1.

Note: the corresponding EMI-1 WMS version is 3.3.5-2 which was distributed
as part of EMI-1 Update 18.

Sites may establish whether or not they have a correct version by checking
for the presence of the rpm glite-wms-ice-3.3.5-4 (sic) or later.

Note: the glite-wms-ice daemon should be restarted after the update.

EMI/UMD-1 WMS version 3.3.5 and probably any earlier 3.3.x version, whether
distributed directly from EMI or from the EGI UMD, are vulnerable.

The (unsupported) gLite 3.1 WMS is not affected.

Mitigation
==========

This problem may be mitigated by entering the following command by a site
administrator with root access.

----------------------------------------------------------------------
chmod o-rwx /var/ice/persist_dir
----------------------------------------------------------------------


Component Installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

http://repository.egi.eu/category/umd_releases/distribution/umd_1/

This vulnerability is now fixed in the version available in this repository,
see http://repository.egi.eu/2012/08/24/release-umd-1-8-1/


Sites may install WMS from EMI-1 directly from the EMI site.

Update 18 contains a fixed version of WMS

http://www.eu-emi.eu/emi-1-kebnekaise-updates/-/asset_publisher/Ir6q/content/update-18-09-08-2012


Recommendations
===============

Sites which have installed or upgraded to the EGI UMD version of WMS prior to
24th August 2012 either need to upgrade again or carry out mitigation actions.

Other information
=================

The latest EMI-1 WMS which is not vulnerable is now available in the EGI UMD.


Credit
======

This vulnerability was reported by Maarten Litmaath.

References
==========


Timeline
========
Yyyy-mm-dd

2012-07-13 Vulnerability reported by Maarten Litmaath
2012-07-16 Acknowledgement from the EGI SVG to the reporter
2012-07-16 Software providers responded and involved in investigation
2012-07-16 Assessment by the EGI SVG reported to the software providers
2012-07-17 Advisory issued by CSIRT  only to vulnerable sites recommending
           mitigating action.
2012-08-09 Updated packages available in EMI-1 but not the EGI UMD
2012-08-13 CSIRT agrees that advisory should be sent to site security contacts
           as some sites are installing the vulnerable version of WMS
           when asked to migrate from unsupported software.
2012-08-24 Fixed version of WMS available in the EGI UMD.
2012-08-29 Public disclosure
```
