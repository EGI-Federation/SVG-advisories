---
title: Advisory-SVG-2011-1414
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG  ADVISORY [EGI-SVG-2011-1414]

Title:   Moderate Risk: BDII file permission and passwords
Date:    2011-03-09
Updated: 2011-10-21, 2011-11-15


URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2011-1414

Introduction
============

This advisory is being issued because a vulnerability in BDII [R1] has been
found which may allow an authorized user to gain password information from a
BDII configuration file.

This problem has been reported to the EGI Software Vulnerability Group (SVG).

Only gLite 3.2 services are affected.


Details
=======

The Berkeley Database Information Index (BDII) is used to provide information
on services and resources in the EGI Grid environment.

One of the configuration files which contains passwords for the database has
been found to have the wrong file permissions by default, and it is possible
that authorized users may be able to read this and modify the Information
Service database.  Also, on configuration of the BDII the site administrator is
not forced to change the password from the default.  If the password is known
and a given BDII is accessible, its contents can be modified remotely.

The affected gLite 3.2 services include the top-level BDII, the site BDII and
every service with a resource BDII.  That is, every service containing the bdii
rpm.


Risk Category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team (RAT).


Affected Software
=================

glite-yaim-core <= 4.0.14-1

For BDII version 5.0.x, versions earlier than 5.0.10 are affected,
the problem was resolved in 5.0.10.

For BDII version 5.1.x, versions earlier than 5.1.23 are affected,
the problem was resolved in 5.1.23.

Affected versions are only present in gLite 3.2.

EMI and the EGI UMD contain newer, non-vulnerable versions of BDII.

In ARC the BDII is managed differently and was found not to be vulnerable.

BDII version 4 is not affected. The implication is that services using gLite
3.1 are not affected.




Component Installation information
==================================

On each affected gLite 3.2 Security Update 01 should be installed as described
here:

    http://glite.cern.ch/security_updates

    http://glite.cern.ch/R3.2/sl5_x86_64/updates/

It refers to the following patch:

    https://savannah.cern.ch/patch/index.php?5110

It provides a YAIM post-configuration function for the BDII that fixes the
vulnerability.

This solution was preferred over a (lengthy) certification of the affected
services with newer versions of glite-yaim-core and the BDII, given the limited
remaining life time of the majority of the affected gLite 3.2 services.


Services installed from the EGI UMD [R 2] are not affected.


Services installed directly from EMI are not affected.


ARC services are not affected.


Recommendations
===============

Sites running gLite 3.2 services should install gLite 3.2 Security Update 01 as
above.

Services installed from the EGI UMD [R 2] are not affected.

Services installed directly from EMI are not affected.

ARC services are not affected.


Credit
======

This vulnerability was reported by Simon Fayer. It was later found and reported
independently by Lukasz Flis and reported by Adam Smutnicki.


References
==========

[R1] https://twiki.cern.ch/twiki/bin/view/EGEE/BDII

[R2] http://repository.egi.eu/category/umd_releases/distribution/umd_1/



Timeline
========
Yyyy-mm-dd

2011-02-28 Vulnerability reported by Simon Fayer
2011-03-01 Acknowledgement from the EGI SVG to the reporter
2011-03-01 Software providers contacted
2011-03-02 Software providers responded and involved in investigation
2011-03-07 Assessment by the EGI Software Vulnerability Group reported to the
           software providers.
2011-03-?? Problem fixed by software providers in BDII
2011-07-12 Unclear which versions of which production services are still
           affected
2011-10-06 Issue reported again by Lukasz Flis and Adam Smutnicki
2011-10-21 Advisory updated after clarification of which versions of which
           production services are still affected. Decision to produce patch
           to fix vulnerable gLite 3.2 sites.
2011-11-15 Advisory updated with release details.
2011-11-15 Public disclosure


On behalf of the EGI SVG,
```
