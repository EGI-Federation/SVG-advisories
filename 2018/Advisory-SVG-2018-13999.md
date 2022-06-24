---
title: Advisory-SVG-2018-13999
permalink: /Advisory-SVG-2018-13999
---

## Advisory-SVG-2018-13999

```

Title:   EGI SVG 'ALERT' [TLP:WHITE] - image mounting via Singularity
         [EGI-SVG-2018-13999]

Date:    2018-03-05
Updated: 2018-03-19 Changed to [TLP:WHITE]


Affected software and risk
==========================

Configuration issue concerning Singularity.

Package : Singularity
CVE ID  : N/A
Bug ID  :

Some potential problems have been found in Singularity, concerning certain
configurations.

**NOTE** This is a separate issue from our "ADVISORY  HIGH risk vulnerability
in Singularity 2.3.2 allowing escape from the container [EGI-SVG-2018-14145]
which is also being sent to sites concerning a vulnerability in a specific
version of singularity.


Actions required/recommended
============================

Sites running Singularity are recommended to check their configuration, and
disable unneeded features.

The default configuration of Singularity allows functionality that carries a
higher risk of attack; that functionality may not be needed for the use cases
that sites want to support.

By default the setuid (rpm) distribution of Singularity allows unprivileged
users to mount image files via loopback devices. This carries an inherently
higher exposure to potential kernel exploits, as discussed in [R 1].
There are no known public exploits at this time, but Linux kernel developers
are concerned enough to refuse allowing the capability in the kernel.
Singularity enables the capability via a setuid-root function.

Please refer to [R 2] for details concerning modifications of the configuration
file.

No specific exploit has been found and both EGI and OSG believe that any
discovered vulnerability would be patched by RedHat.

Sites may choose whether or not to protect against the potential vulnerability.

If anyone becomes aware of any situation where this has a significant impact on
the EGI infrastructure then please inform EGI SVG.

Affected software details
=========================

RedHat 6 & 7 and its derivatives are affected, and all versions of Singularity.

More information
================


TLP and URL
===========

** WHITE information - Unlimited distribution -
see https://go.egi.eu/tlp for distribution restrictions **

URL:   https://advisories.egi.eu/Advisory-SVG-2018-13999

Minor updates may be made without re-distribution to the sites

Advisory also issued concerning singularity:--

URL:  https://advisories.egi.eu/Advisory-SVG-2018-14145


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 3]

Note that this has been updated and the latest version approved by the
Operations Management Board in November 2017


References
==========

[R 1] https://lwn.net/Articles/652468/

[R 2] http://opensciencegrid.github.io/docs/worker-node/install-singularity/#limiting-image-types

[R 3] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======


SVG was alerted to this issue by OSG. Some of their information is used in this alert.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2018-13999]

2018-01-17 SVG alerted to this issue by OSG
2018-01-17 Acknowledgement from the EGI SVG to the reporter
2018-01-18 Investigation of vulnerability and relevance to EGI carried out by SVG
2018-02-08 EGI SVG Risk Assessment completed
2018-03-05 Advisory/Alert sent to sites
2018-03-19 Changed to [TLP:WHITE] and placed on the EGI SVG wiki


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 3] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.
The risk may also be higher or lower in other deployments depending on how the
software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```
