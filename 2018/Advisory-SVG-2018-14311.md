---
title: SVG:Advisory-SVG-2018-14311
---

````
Title:   EGI SVG 'ADVISORY’ [TLP:WHITE] ‘CRITICAL’ risk. Local privilege
         escalation using singularity [EGI-SVG-2018-14311]

Date:    2018-04-30
Updated: 2018-05-21 **changed to TLP:WHITE and placed on wiki**

Affected software and risk
==========================

'CRITICAL' risk vulnerability concerning singularity

Package : Singularity
CVE ID  : Not assigned yet

Multiple vulnerabilities have been reported concerning Singularity, where for
example Singularity can create arbitrary directories and files outside the
container.
If Singularity is deployed setuid root (the _default_ configuration), such
files and directories can be created anywhere and with root ownership, which
implies a trivial local root exploit and hence affects any user on the same
host.

At least all versions from 2.4.2 and prior to 2.5.0 are affected.

Actions required/recommended
============================

Sites are strongly requested to do **one** of the following:
- update to 2.5.0-1.1, released in the WLCG repository at 15:45 CEST on April
  30th
- remove the singularity and singularity-runtime packages
- disable the setuid-bit of all the singularity binaries which will effectively
  disable singularity on most deployments:

```chmod u-s /usr/libexec/singularity/bin/*-suid```

Mitigation
==========

There is no known mitigation other than updating, removing or disabling
Singularity.


Additional information
====================

As CMS strongly relies on singularity, disabling singularity can strongly
affect CMS workflows.

Please note that two issues have already been found in singularity 2.5.0, which
may affect certain workflows:
- Incompatibility with NFS (root_squash):
https://github.com/singularityware/singularity/pull/1491
- Incompatibility with SSSD:
https://github.com/singularityware/singularity/pull/1490

TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2018-14311

Minor updates may be made without re-distribution to the sites.

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

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2018-14311]

2018-04-27 SVG alerted to this issue by Dave Dykstra
2018-04-27 Singularity team released update to vulnerability late Friday and
           announced publicly
2018-04-30 Acknowledgement from the EGI SVG to the reporter
2018-04-30 EGI SVG Risk Assessment completed
2018-04-30 Emergency Advisory sent by Security officer on duty
2018-05-21 Advisory placed on wiki

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
Vincent Brillault
EGI Security Officer on duty
````
