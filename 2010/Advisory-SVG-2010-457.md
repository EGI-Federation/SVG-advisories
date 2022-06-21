---
title: Advisory-SVG-2010-457
---

```
** WHITE information - Unlimited distribution allowed **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI CSIRT ADVISORY [EGI-ADV-20101028]
EGI SVG   ADVISORY [EGI-SVG-2010-457]

This advisory was originally sent to specific sites by CSIRT which needed to
take action.

As it is now past the TD, SVG is making it public.

Title: World writeable directory in vdt_globus_data_server RPM
Date:     28th October 2010
Updated : 9th January 2012
URL:      https://wiki.egi.eu/wiki/Advisory-SVG-2010-457

Introduction
============

Updated 9th January 2012:

This advisory is simply being placed on the SVG wiki, as it is past the TD.
Affected sites are likely to have already taken action.

Original from CSIRT on 28th October 2010:

When the vdt_globus_data_server RPM is installed a world writeable directory is
created.

The EGI CSIRT team recommends that affected sites carry out the mitigation
below.



Details
=======

When the vdt_globus_data_server RPM is installed it creates a world writeable
directory:

    /opt/globus/var/log

On an lcg-CE node the permissions of the directory may subsequently have been
adjusted to 755 by any of 3 other RPMs that own the same directory:

    globus-gass-cache-marshal
    globus-gma
    globus-job-manager-marshal

No gLite service needs the directory to be world writeable.

Risk Category
=============

The risk is estimated to be 'Low', but sites are advised to apply the simple
mitigation detailed below.


Affected Software
=================

vdt_globus_data_server VDT1.10.1x86_64_rhap_5-4 and all earlier versions.

gLite 3.2 update 19 (5th Oct 2010), earlier and possibly later versions.

gLite 3.1 update 66 (8th Aug 2010), earlier and possibly later versions.

At the time of this advisory there is no RPM that fixes the vulnerability.

Mitigation
==========

Sites should run the following command on all machines that have the
vdt_globus_data_server RPM installed:


    chmod 755 /opt/globus/var/log


Component Installation information
==================================

Patch not available, mitigating action is recommended.

Updated (9th January 2012) Unlikely any sites continue to have this problem.

Recommendations
===============

Sites affected should carry out actions in Mitigation.


Other information
=================

In gLite 3.2 the RPM is used by the following node types:

    CREAM
    SE_dpm_mysql
    SE_dpm_disk
    VOBOX

In gLite 3.1 the RPM is used by the following node types:

    CREAM
    SE_dpm_mysql
    SE_dpm_disk
    WMS
    lcg-CE

Updated 9th January 2012 - Publicly disclosed as past Target Date and won't
fix.


Credit
======

This vulnerability was reported by Jan Iven from CERN


Timeline
========

Yyyy-mm-dd

2010-10-21 Vulnerability reported by Jan Iven from CERN
2010-10-21 Acknowledgement from the EGI SVG to the reporter
2010-10-28 CSIRT issued advisory to affected sites.
2012-01-09 Public disclosure as past TD.
```
