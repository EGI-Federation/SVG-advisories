---
title: SVG:Advisory-SVG-2013-6116
permalink: /SVG:Advisory-SVG-2013-6116/
---

```

** WHITE information - Unlimited distribution allowed
**
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions
**

EGI SVG   ADVISORY [EGI-SVG-2013-6116]

Title:       EGI SVG Advisory 'High' RISK - Vulnerabilities in STORM [EGI-SVG-2013-6116]
Date:        2013-02-21
Updated:     <date  yyyy-mm-dd>

This advisory will be placed on the wiki in approx 2 weeks, on or after 7th March 2014.

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2013-6116

Introduction
============

5 vulnerabilities were found in STORM.


These have been fixed in the versions of STORM available in the EGI UMD-3 and EMI-3
repositories.

4 of these 5 vulnerabilities are also present in the version of STORM available in
EGI UMD-2 and EMI-2 versions.  These have NOT been fixed and will not be fixed.

Sites deploying STORM should install the latest version of STORM available in EGI UMD-3
and EMI-3 repositories

Sites have been requested to migrate away from the UMD-2 and EMI-2 versions of STORM anyway
as they are not SHA-2 compliant.


Details
=======

StoRM (STOrage Resource Manager) [R 1] has been found to contain various vulnerabilities.

1) File permission problem which affects at random 25% of installations.

2) A vulnerability which allows file system traversal

3) Another vulnerability which may allow escape from intended VO file area.

4) An insecure backend to the STORM Storage element

5) An SQL injection vulnerability.

These vulnerabilities are confirmed as present in the version available in EGI UMD-3 and EMI-3.

All but 1) are also confirmed to be present in the version available in EGI UMD-2 and EMI-2.

The version of STORM in EGI UMD-2 and EMI-2 is not SHA-2 compliant hence sites have already
been asked to migrate away from this. Very few sites are still running STORM versions from
EGI UMD-2 or EMI-2.

Risk category
=============

The first 4 of these 5 issues have been assessed as 'High' risk by the EGI SVG Risk Assessment Team.
The last has been assessed as 'Moderate'.


Affected software
=================

This is fixed in version 1.11.3 of STORM available in EGI UMD-3 and EMI-3.

Earlier versions of STORM available in EGI UMD-3 and EMI-3 prior to version are affected.

The versions of STORM available in EGI UMD-2 and EMI-2 are affected by all but one of these
vulnerabilities and will not be fixed.


Mitigation
==========

None. Sites should migrate to the secure version.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites is repository.egi.eu
which contains the EGI Unified Middleware Distribution (UMD).


Sites installing from EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

This is fixed in the version of STORM in UMD-3.5.0

Sites who wish to install directly from the EMI release should see:

http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/

This is fixed in EMI3 Update 13



Recommendations
===============

Sites who have already installed STORM from EGI UMD-3 or EMI-3 are recommended to
update relevant components as soon as possible.

Any sites still running versions of STORM from EGI UMD-2 or EMI-2 are recommended
to migrate to EGI UMD-3 or EMI-3 as soon as possible.


Credit
======

These vulnerabilities were found and reported by Simon Fayer of Imperial College.


References
==========

[R 1] http://www.italiangrid.it/middleware/storm

Timeline
========
Yyyy-mm-dd

2013-09-30 Vulnerabilities reported by Simon Fayer
2013-09-30 Acknowledgement from the EGI SVG to the reporter
2013-10-01 Software providers contacted, responded and involved in investigation
2013-10-14 Assessment by the EGI Software Vulnerability Group reported to the software providers
2014-02-20 Updated packages available in the EGI UMD 3
2014-02-21 Advisory sent to sites.
2014-03-25 Public disclosure
```