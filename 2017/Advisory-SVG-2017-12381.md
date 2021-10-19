---
title: SVG:Advisory-SVG-2017-12381
---

```
Title:   EGI SVG Advisory [TLP:WHITE] Up to 'High' risk - Singularity container
         escape vulnerability [EGI-SVG-2017-12381]

Date:    2017-02-17
Updated:


Affected software and risk
==========================

Up to HIGH risk vulnerability concerning Singularity container escape.

Package : Singularity
CVE ID  : N/A
Bug ID  : N/A

If unprivileged users are allowed to launch their own containers through
Singularity, it would be possible for a malicious user to create and manipulate
specifically crafted raw devices within containers they own, and then gain
access outside their own container.


Actions required/recommended
============================

Sites running Singularity must update as soon as possible.


Affected software details
=========================

This is fixed in Singularity Version 2.2.1

Earlier versions are vulnerable.


More information
================

See [R 1]

We rate this as 'up to High risk' as the actual risk depends on the type of use
and local site configuration.

When singularity containers are run via batch systems, which we think is likely
to be a typical implementation in EGI, the vulnerability cannot be exploited.

The configurations that allow individual users to upload and execute
singularity containers are vulnerable and must be updated urgently.


Component installation information
==================================

Fixed version is available from [R 1]

TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2017-12381

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 2]


References
==========

[R 1] https://github.com/singularityware/singularity/releases/tag/2.2.1

[R 2] https://documents.egi.eu/public/ShowDocument?docid=2538

Credit
======

This vulnerability was discovered by Mattias Wadenstein

And

SVG was alerted to this vulnerability by Jeny Teheran from Fermilab.

Testing also carried out by Barbara Krasovec

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-12381]

2017-02-03 SVG alerted to this issue by Jeny Teheran.
2017-02-06 Acknowledgement from the EGI SVG to the reporter
2017-02-06 Investigation of vulnerability and relevance to EGI carried out,
           including testing by Barbara Krasovec
2017-02-15 Singularity 2.2.1 security release
2017-02-15 EGI SVG meeting, agreed on 'Up to High' and advisory/alert necessary
2017-02-17 Advisory/Alert sent to sites



Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 2] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group
```
