---
title: Advisory-SVG-2016-12231
---

```
Title:   EGI SVG Advisory [TLP:WHITE] OpenStack Nova Metadata leak - sites
         should check [EGI-SVG-2016-12231]

Date:    2017-01-11
Updated:

Affected software and risk
==========================

Vulnerability concerning OpenStack Nova Metadata information leak -
Vulnerability in actual software - but if configured as instructed should not
be exploitable

Package : OpenStack Nova
CVE ID  : (None at present)
Bug ID  : OpenStack 1563954

OpenStack Nova may allow metadata to be leaked, this is a problem if such
metadata contains sensitive information.
This is described in OpenStack Security Notice 0074 [R 1]


Actions required/recommended
============================

Nova metadata service should not be used for sensitive information as described
in [R 1]

Sites and Users who provide metadata which is used by OpenStack Nova should
check that they are not including any sensitive data.

Affected software details
=========================

See [R 1] [R 2]

More information
================

See [R 1] [R 2]

An attacker with access to a compute instance, i.e. a VM, in the cloud could
send a request to the metadata service.  Hence an authorized VM user, i.e. any
user able to perform an http request from a VM, might thus obtain sensitive
information if Nova happens to contain any.  This is independent of who started
a VM.

That scenario then may affect some of the Fed Cloud sites, as well as grid
sites that happen to provide resources through OpenStack.


Component installation information
==================================

N/A at present.


TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **
URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2016-12231

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


References
==========

[R 1] https://wiki.openstack.org/wiki/OSSN/OSSN-0074

[R 2] https://bugs.launchpad.net/nova/+bug/1563954

[R 3] https://documents.egi.eu/public/ShowDocument?docid=2538

Credit
======

SVG was alerted to this vulnerability by Baptiste Grenier


Timeline
========

Yyyy-mm-dd  [EGI-SVG-2016-12231]

2016-12-19 SVG alerted to this issue by Baptiste Grenier
2016-12-19 Acknowledgement from the EGI SVG to the reporter
2016-12-20 Investigation of vulnerability and relevance to EGI carried out by
           various  SVG members
2016-12-21 Concluded that an alert should be sent, suggesting sites check
2017-01-11 Advisory/Alert sent to sites


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

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group
```
