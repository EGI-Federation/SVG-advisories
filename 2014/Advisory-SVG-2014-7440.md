---
title: SVG:Advisory-SVG-2014-7440
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'Low' Risk - Dirac Pilot factory payload
         verification [EGI-SVG-2014-7440]

Date:    2016-05-25
Updated:

Affected Software and Risk
==========================

'Low' risk vulnerability concerning DIRAC Pilot factory payload verification

Actions Required/Recommended
============================

No action is recommended - this is for information only

Introduction
============

A vulnerability has been found where Dirac does not carry out any verification
of software tarballs.

Since then Dirac has been migrating to use software installation from the CVMFS
repository, which is considered to be an acceptable means of installation
across the project.

Affected Software
=================

DIRAC software installed via means other than via CVMFS.

The DIRAC software is installed by pilots from CVMFS on the worker nodes where
CVMFS is available starting from version v6r15

More information
=================

DIRAC download their jobwrapper code tarballs over HTTP with no suitable
verification that it hasn't been tampered with (and then execute the contained
code).
In principle this opens the door to DNS and MITM attacks, which are unlikely in
our environment.

The move to installation via CVMFS is a satisfactory solution.

Risk category
=============

This issue has been assessed as 'Low' Risk by the EGI SVG Risk Assessment Team.


Affected software
=================

Dirac software installed via means other than via CVMFS.

Mitigation
==========

Installation via CVMFS.


Component installation information
==================================

See [R 1]


Recommendations
===============

No action is recommended. Sites are simply being informed that this 'Low' risk
vulnerability exists if the DIRAC software is installed other than via CVMFS.

TLP and URL
===========

** WHITE information - Unlimited distribution                               **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2014-7440

Minor updates may be made without re-distribution to the sites

Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London,
who is also a member of SVG.

References
==========

[R 1] https://github.com/DIRACGrid/DIRAC/wiki


Timeline
========
Yyyy-mm-dd

2014-09-16 Vulnerability reported by Simon Fayer from Imperial College
2014-09-16 Software providers responded and involved in investigation
2014-11-07 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2015-08-13 Informed that DIRAC migrating to CVMFS for most of it's software installation.
2016-05-25 Advisory sent to sites
2016-05-25 Advisory placed on public wiki


On behalf of the EGI SVG,
```
