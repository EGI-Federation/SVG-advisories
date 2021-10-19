---
title: SVG:Advisory-SVG-2017-12931
---

```
Title:   EGI SVG Advisory/Alert [TLP:WHITE] Attacks on Hadoop installations
         - sites should check they are securely configured [EGI-SVG-2017-12391]

Date:    2017-02-13
Updated:


Affected software and risk
==========================

Attacks are being carried out on Hadoop installations which are not securely
configured.

Package : Hadoop
CVE ID  : N/A
Bug ID  : N/A

The OSG Security team has received a report of "drive-by" attacks on various
open source products, including Hadoop.  Attackers are looking for unsecured
HDFS (Hadoop Distributed File System) instances where they can perform
unauthorized malicious activities, such as modify or delete all accessible data
at the site.

Actions required/recommended
============================

Sites running Hadoop should check that their sites are securely configured.

(Based on alert from OSG)

WHAT YOU SHOULD DO?

- Ensure that Hadoop instances, and all services, are kept up to date with the
  latest supported software versions.

- Remove off-site access from the Hadoop end-points: NameNodes, Backup
  NameNodes and Secondary NameNodes.

- Make sure the Hadoop end-points at your site are only accessible from the
  services that need access.


See Apache hadoop HDFS Permissions Guide [R 1]


TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions  **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2017-12931

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

[R 1] https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-hdfs/HdfsPermissionsGuide.html#The_Web_Server

[R 2] https://documents.egi.eu/public/ShowDocument?docid=2538

Credit
======

OSG security alert issued by Jeny Teheran, this is based on the OSG alert.

EGI SVG was alerted to this by Romain Wartel.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-12391]

2017-02-09 OSG alert sent by Jeny Teheran
2017-02-10 SVG alerted to this issue by Romain Wartel
2017-02-10 EGI SVG decided to alert sites, as several EGI sites use Hadoop.
2017-02-10 OSG confrimed that the alert was 'White' information.
2017-02-13 Advisory/Alert sent to sites and placed on wiki



Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 2]  in the context of how the software is used in the EGI
infrastructure.
It is the opinion of the group, we do not guarantee it to be correct. The risk
may also be higher or lower in other deployments depending on how the software
is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group


On behalf of the EGI SVG,
```
