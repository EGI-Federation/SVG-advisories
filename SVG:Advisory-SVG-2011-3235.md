---
title: SVG:Advisory-SVG-2011-3235
permalink: /SVG:Advisory-SVG-2011-3235/
---

```

** WHITE information - Unlimited distribution allowed                       **

** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


EGI SVG   ADVISORY [EGI-SVG-2011-3235]

Title:       BDII Predictable passwords
Date:        2012-04-02
Updated:

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-3235

Introduction
============

It has been found that the BDII [R1] password is predictable when installing
the EMI top level BDII.

This has now been resolved.

Details
=======

A previous vulnerability in BDII was found for which the EGI issued an advisory at
[R 2] and it was stated that it only applied to gLite 3.2

However, this was found to also partially apply to the EMI version of BDII.
The BDII password is predictable and not changed to a random value.

This has now been resolved in EMI and in the EGI UMD.


Risk Category
=============

This issue was not individually assessed as it was a partial failure to
resolve issue described at https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-1414


Affected Software
=================

This vulnerability was found in BDII 5.2.5-2

The problem is fixed in BDII 5.2.7 released as part of EMI-1 Update 13 and is
available in UMD 1.6.0



Mitigation
==========

No Mitigation is recommended.


Component Installation information
==================================


Release UMD-1.6.0

http://repository.egi.eu/2012/04/02/release-umd-1-6-0/


The official repository for the distribution of grid middleware for EGI sites is
repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).


http://repository.egi.eu/category/umd_releases/distribution/umd_1


Recommendations
===============

Sites are recommended to update relevant components.


Credit
======

This vulnerability was reported by Lukasz Flis


References
==========


[R 1] https://twiki.cern.ch/twiki/bin/view/EGEE/BDII

[R 2] https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-1414

[R 3] http://repository.egi.eu/category/umd_releases/distribution/umd_1/

[R 4] http://www.eu-emi.eu/emi-1-kebnekaise

[R 5] http://repository.egi.eu/2012/04/02/release-umd-1-6-0/


Timeline
========
Yyyy-mm-dd

2011-11-30 Possible Vulnerability discussed in e-mail by Lukasz Flis
2011-12-08 Vulnerability entered into SVG issue handling process and investigation
           under way
2011-12-09 Software providers responded and involved in investigation
2012-01-10 Established that there is definitely a problem
2012-04-04 Updated packages available EGI UMD
2012-04-04 Public disclosure
```