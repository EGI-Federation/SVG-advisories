---
title: SVG:Advisory-SVG-2018-14117
permalink: /SVG:Advisory-SVG-2018-14117/
---

```

Title:       EGI SVG 'ALERT' [TLP:WHITE] data-channel encryption is not enforced in gridftp [EGI-SVG-2018-14117]

Date:        2018-03-28
Updated:     2018-07-20

Affected software and risk
==========================

Package : globus-url-copy, uberftp, globus-gridftp-server
CVE ID  : N/A

Applications and sites should be aware that requesting data-channel encryption (i.e. PROT E) when using gridftp
is no guarantee that this will actually be enabled.
This affects (at least) globus-url-copy and uberftp. Third-party transfers using a globus-gridftp-server are also affected,
which includes DPM.

This is considered 'Low' risk to the EGI infrastructure as a whole, but applications should be aware not to rely on
data-channel encryption.

**UPDATE 2018-07-20**

This is unlikely to be fixed

Actions required/recommended
============================

Anyone relying on encrypted transfers using gridftp should not rely on gridftp's data-channel encryption but instead
encrypt data before transmission.

If anyone becomes aware of any situation where this vulnerability has a significant impact on the EGI infrastructure
or any usage in EGI then please inform EGI SVG.

More information
================

Not all gridftp servers implement data-channel authentication (DCAU).
In case DCAU is not available, a number of gridftp tools also do not support data-channel encryption (PROT E).
These tools then silently fail-over to data protection level clear (PROT C).
Currently, dCache does not support DCAU, hence clients to dCache typically cannot use data-channel encryption.

For globus-url-copy, PROT E is requested using the -dcpriv commandline flag, for uberftp it is requested using the "prot E" command.
In case a third-party transfer is done from a globus-gridftp-server, the same silent failover occurs.

See [R 1] for the originally reported issue.

Note that the Globus Toolkit is no longer maintained by the Globus team, except for security patches, see [R 2]
However the Grid Community Forum [R 3] has produced an (open source) fork of the Globus toolkit,
called the Grid Community Toolkit (GCT).
The GCT packages will also replace the current globus-toolkit packages in EPEL and Debian but will be binary compatible.

The GCT may release an updated version of the globus-url-copy and globus-gridftp-server to partially address this issue,
but due to the variety of tools involved, a full fix is not possible.

TLP and URL
===========

** WHITE information - Unlimited distribution
- see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions**

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2018-14117

Minor updates may be made without re-distribution to the sites

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the procedure defined in [R 4]

Note that this has been updated and the latest version approved by the Operations Management Board in November 2017


References
==========

[R 1] https://github.com/globus/globus-toolkit/issues/121

[R 2] https://github.com/globus/globus-toolkit/blob/globus_6_branch/support-changes.md

[R 3] https://gridcf.org/

[R 4] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was alerted to this vulnerability by Mischa Salle who is a member of SVG.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2018-14117]

2018-02-21 SVG alerted to this issue by Mischa Salle
2018-02-22 Acknowledgement from the EGI SVG to the reporter
2018-02-22 EGI SVG Assessed as 'Low' risk concerning the EGI infrastructure
2018-03-20 Clear that it is unlikely to be fixed.
2018-03-20 Further discussion on issue
2018-03-20 Decided to send alert to VO managers and sites, saying not to rely on these tools encrypting data
2018-03-28 Alert sent to sites and VO managers
2018-07-20 Minor update stating unlikely to be fixed.


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's purpose
"To minimize the risk to the EGI infrastructure arising from software vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling procedure [R 3]
in the context of how the software is used in the EGI infrastructure. It is the opinion of the group,
we do not guarantee it to be correct. The risk may also be higher or lower in other deployments
depending on how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```