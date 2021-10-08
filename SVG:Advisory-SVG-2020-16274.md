---
title: SVG:Advisory-SVG-2020-16274
permalink: /SVG:Advisory-SVG-2020-16274/
---

```

Title:       EGI SVG 'ALERT' **UPDATE** [TLP:WHITE] CRITICAL risk vulnerability in IBM GPFS file system  [EGI-SVG-2020-16274]
Date:        2020-03-13
Updated:     2020-04-28, 2020-06-05

Affected software and risk
==========================
CRITICAL risk vulnerability concerning IBM GPFS

Package : GPFS
CVE ID  : N/A
Bug ID  :

A site of a peer infrastructure has identified a local privilege escalation vulnerability in IBM GPFS.
We are aware that there are some sites within EGI which use this software, hence the alert.

Actions required/recommended
============================

**UPDATE 2020-06-05**

Changed to [TLP:WHITE] and placed on the wiki

**UPDATE 2020-04-28**

IBM has released updates for this - See [R 2]

Sites should carry out updates as suggested by IBM Support if they have not done so already.


**ORIGINAL ALERT**

At the time of writing there is no full solution for this vulnerability.

At present sites are recommended to carry out the mitigating actions below.

Mitigation
==========

Update to the latest version (which we are told will fix some other vulnerabilities).

Remove SUID bit from /usr/lpp/mmfs/bin/*

Affected software details
=========================

We are fairly sure RPM package gpfs.base-4.2.3-20 is affected by a Local Privilege Escalation vulnerability.

All versions of GPFS 4.2.3 may be affected by a Local Privilege Escalation vulnerability.


TLP and URL
===========

** WHITE information - Unlimited distribution
 - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2020-16274

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the procedure defined in [R 1]

Note that this is undergoing revision to fully handle vulnerabilities in the EOSC-hub era.


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=3145

[R 2] https://www.ibm.com/support/pages/node/6151701

Credit
======

SVG was alerted to this vulnerability by Vincent Brillault (CERN), a member of SVG.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2020-16274]

2020-03-12 SVG alerted to this issue by Vincent Brillault
2020-03-13 EGI SVG Risk Assessment completed
2020-03-13 Alert sent to sites
2020-04-28 Update sent to sites
2020-06-05 Placed on SVG wiki

Context
=======

This alert has been prepared as part of the effort to fulfil EGI SVG's purpose
"To minimize the risk to the EGI infrastructure arising from software vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling procedure [R 1]
in the context of how the software is used in the EGI infrastructure. It is the opinion of the group,
we do not guarantee it to be correct. The risk may also be higher or lower in other deployments
 depending on how the software is used.

This advisory is subject to the Creative commons license https://creativecommons.org/licenses/by/4.0/
and the EGI https://www.egi.eu/ Software Vulnerability Group must be credited.

Note that the SVG issue handling procedure is currently under review, to take account of the increasing I
nhomogeneity of the EGI infrastructure and the services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```