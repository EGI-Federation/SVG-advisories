---
title: SVG:Advisory-SVG-2014-7430
permalink: /SVG:Advisory-SVG-2014-7430/
---

```

Title:   EGI SVG Advisory [TLP:WHITE] 'Low' Risk - Panda Pilot factory payload
         verification [EGI-SVG-2014-7430]


Date:    2016-05-25
Updated:


Affected Software and Risk
==========================

'Low' Risk Vulnerability concerning Panda Pilot factory payload verification

Actions Required/Recommended
============================

No action is recommended - this is for information only

Affected software
=================

Panda software installed via means other than via CVMFS.

More Information
================

The PanDA (Production and Distributed Analysis System) is a framework developed
by the LHC ATLAS experiment to handle pilot jobs in a distributed computing
environment. [R 1]

A vulnerability has been found where Panda does not carry out any verification
of software tarballs.

Panda download their jobwrapper code tarballs over HTTP with no suitable
verification that it hasn't been tampered with (and then execute the contained
code).  In principle this opens the door to DNS and MITM attacks, which are
unlikely in our environment.

Panda is migrating to use software installation from the CVMFS repository,
which is considered to be an acceptable means of installation across the
project. The move to installation via CVMFS is considered to be a satisfactory
solution.

Risk category
=============

This issue has been assessed as 'Low' Risk by the EGI SVG Risk Assessment Team.

Mitigation
==========

Installation via CVMFS

Recommendations
===============

No action is recommended. Sites are simply being informed that this 'Low' risk
vulnerability exists.

TLP and URL
===========

** WHITE information - Unlimited distribution                               **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-7430

Minor updates may be made without re-distribution to the sites

Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London.

Timeline
========
Yyyy-mm-dd

2014-09-16 Vulnerability reported by Simon Fayer from SVG
2014-09-16 Software providers responded and involved in investigation
2014-11-07 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2015--     Migrating to CVMFS
2016-05-25 Advisory sent to sites
2016-05-25 Advisory placed on public wiki
```
