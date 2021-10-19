---
title: SVG:Advisory-SVG-2018-14145
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] HIGH risk vulnerability in Singularity
         2.3.2 allowing escape from the container [EGI-SVG-2018-14145]

Date:    2018-03-05
Updated: 2018-03-19 changed to [TLP:WHITE]


Affected software and risk
==========================

HIGH risk vulnerability concerning Singularity

Package : Singularity
CVE ID  : N/A

There is a vulnerability in Singularity allowing processes to escape from the
container.
They then would have access to parts of the host file systems that were assumed
to be shielded.

**NOTE** This is a separate issue from our "ALERT - image mounting via
Singularity [EGI-SVG-2018-13999]" which is also being sent to sites to
recommend configuration checks/changes for all versions of singularity.

Actions required/recommended
============================

Sites running singularity-2.3.2 should update to singularity-2.4.2 as soon as
possible.

It is available from the WLCG rpm repository [R 1].


Affected software details
=========================

Singularity 2.3.2

Earlier and later versions of Singularity are not affected.


More information
================

Note that there are some command line incompatibilities with version 2.3.2,
mostly in the commands related to managing images.


Component installation information
==================================

On hosts where the singularity rpm is installed, a simple rpm update should
normally be sufficient.

If the original configuration file was modified, it may have to be adjusted
after the update.


TLP and URL
===========

** WHITE information - Unimited distribution
  - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

This advisory will be placed on the wiki on or after 2018-03-19

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2018-14145

Minor updates may be made without re-distribution to the sites

Other issue concerning singularity where an ALERT was issued:--

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2018-13999

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 2]

Note that this has been updated and the latest version approved by the
Operations Management Board in November 2017


References
==========

[R 1]  http://linuxsoft.cern.ch/wlcg/

[R 2]  https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was alerted to this vulnerability by Dave Dykstra from OSG

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2018-14145]

2018-02-26 SVG alerted to this issue by Dave Dykstra from OSG
2018-02-26 Acknowledgement from the EGI SVG to the reporter
2018-02-26 Investigation of vulnerability and relevance to EGI carried out by
           SVG
2018-02-27 EGI SVG Risk Assessment completed
2018-03-05 Advisory/Alert sent to sites
2018-03-19 Changed to TLP:WHITE and placed on the EGI SVG wiki


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 2] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.
The risk may also be higher or lower in other deployments depending on how the
software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```
