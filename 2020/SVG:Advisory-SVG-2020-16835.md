---
title: SVG:Advisory-SVG-2020-16835
permalink: /SVG:Advisory-SVG-2020-16835/
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] MODERATE risk - Disk Pool Manager (DPM)
         logging may contain sensitive information [EGI-SVG-2020-16835]

Date:    2020-09-03
Updated:


Affected software and risk
==========================

'MODERATE' risk vulnerability concerning Disk Pool manager (DPM) [R 1] logging

Package : DPM

It has been found that DPM may write highly sensitive information into log
files, including passwords, at higher LogLevel values which normally are used
for debugging purposes only.


Actions required/recommended
============================

Sites which run DPM should check their logging level, see [R 2] and ensure that
for routine operations the LogLevel is set to 1 or 0.  Such logs will not
contain sensitive information.

If sites are running at a higher LogLevel (e.g. for debugging purposes) they
should take extra care of these logs, in particular if they need to share them
for some reason, e.g. with DPM experts. Do not send such logs to mailing lists
and do not attach them to GGUS tickets, unless all sensitive information has
first been removed.

Sites will normally wish to run their DPM logging at no higher than LogLevel 1
anyway, as higher levels tend to use a lot of disk space and may lower the
performance.


More information
================

Future DPM versions may exclude highly sensitive information at all LogLevel
values.


TLP and URL
===========

** WHITE information - Unlimited distribution
- see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2020-16835

Minor updates may be made without re-distribution to the sites

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 3]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.


References
==========

[R 1] https://lcgdm.web.cern.ch/dpm

[R 2] https://twiki.cern.ch/twiki/bin/view/DPM/DpmSetupTuningHints#Hint_Doublecheck_the_DMLite_log

[R 3] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was reported by Robert Currie

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2020-16835]

2020-08-24 Vulnerability reported by Robert Currie
2020-08-24 Acknowledgement from the EGI SVG to the reporter
2020-08-24 Software providers responded and involved in investigation
2020-08-25 Investigation of vulnerability and relevance to EGI carried out.
2020-08-26 EGI SVG Risk Assessment completed
2020-08-26 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2020-09-03 Advisory sent to sites


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 3] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

-----------------------------
This advisory is subject to the Creative commons license
https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/
Software Vulnerability Group must be credited.
-----------------------------


Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
