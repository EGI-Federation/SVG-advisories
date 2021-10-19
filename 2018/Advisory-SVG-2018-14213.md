---
title: SVG:Advisory-SVG-2018-14213
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] 'CRITICAL' risk.
         Singularity can be tricked to create directories and files outside the
         container.


Date:    2018-03-29
Updated: 2018-05-23 - [TLP:WHITE] and fixed in later versions.


Affected software and risk
========================

'CRITICAL' risk vulnerability concerning singularity

Package : Singularity
CVE ID  : Not assigned yet

A vulnerability has been reported where Singularity can create arbitrary
directories and files outside the container.  If Singularity is deployed setuid
root, such files and directories can be created anywhere and with root
ownership.  Existing files cannot be overwritten, though.

At least all versions from 2.4.2 onwards are affected, this includes the latest
versions recommended by WLCG and OSG.

Actions required/recommended
============================

**UPDATE 2018-05-23**

This is fixed in version 2.5.0, which also fixes another critical
vulnerability:--
https://wiki.egi.eu/wiki/Advisory-SVG-2018-14311


Mitigation
==========

Sites running singularity are urged to disable OverlayFS by replacing the
`enable overlay` setting in `/etc/singularity/singularity.conf` to read `enable
overlay = no`.


Further information
==================

The mitigation will effectively disable all creation of mount points for bound
directories and files in the container, so anything you intend to bind into the
image needs pre-created mountpoints in the image.

It is thought that this mitigation does not affect the way singularity is used
by CMS.

As soon as a patched version is available, this advisory will be updated.


TLP and URL
===========

** WHITE information - Unlimited distribution
  - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL  https://wiki.egi.eu/wiki/Advisory-SVG-2018-14213

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]

Note that this has been updated and the latest version approved by the
Operations Management Board in November 2017

References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was found by Lars Viklund from Umeå University in Sweden,
who also provided the mitigation instructions.  EGI SVG was alerted by Ake
Sandgren.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2018-14213]

2018-03-28 Vulnerability was found by  Lars Viklund, HPC2N, Umeå University
2018-03-28 Acknowledgement from the EGI SVG to the reporter
2018-03-28 Investigation of vulnerability and relevance to EGI carried out by
           (as appropriate)
2018-03-29 EGI SVG Risk Assessment completed
2018-03-29 Initial Advisory sent to sites - suggesting mitigation
2018-05-23 Advisory made public, vulnerability fixed in later versions


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

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```
