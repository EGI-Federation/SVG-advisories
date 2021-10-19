---
title: SVG:Advisory-SVG-2016-11363
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'Moderate' risk Two Perfsonar
         Vulnerabilities announced by the Perfsonar team [EGI-SVG-2016-11363]

Date:    2016-07-15
Updated:


Affected software and risk
==========================

2 vulnerabilities have been announced by the Perfsonar team see [R 1]

Package : Perfsonar

One vulnerability concerns remote unauthenticated file access, the other
concerns privilege escalation.  In this case has been assessed as 'Moderate'
risk.

Actions required/recommended
============================

Sites are recommended to update relevant components as soon as is convenient.


Affected software details
=========================

Affected packages:

* libperfsonar* < 3.5.1.8
* perfsonar-toolkit* < 3.5.1.4
* perfsonar-oppd-bwctl* < 3.5.1.1


More information
================

Information on this vulnerability is public.

It is considered that the information exposed is not especially sensitive,
hence a lower risk than would be expected is assigned to this issue allowing
unauthenticated file access than would normally be the case.


As announced by Perfsonar:

Updated perfSONAR packages were published this morning to address security
concerns. A special thanks to Luke Young for taking the time to find, document
and provide a few patches for the items detailed below.  The updates address
the following issues:

1.It was possible to generate a carefully crafted SOAP message that goes to the
OPPD service that would allow an unauthenticated user to read arbitrary files
from the filesystem as the 'perfsonar' user.  This was done by exploiting a
feature of LibXML that processes external entities. The ability to do so has
since been disabled.

2.The second issue allowed someone logged-in to the host via SSH as an
unprivileged user to escalate to root privileges using a combination of the
Toolkit’s ConfigManager and BWCTL’s posthook feature.  ConfigManager did not
actually need access to the BWCTL config file anymore, so access to this file
(and thus the posthook feature) has been removed.

If auto-updates are enabled, the updates will install automatically. It is also
possible to run “yum update libperfsonar* perfsonar-toolkit* perfsonar-oppd*”
to get the changes manually on RedHat and "apt-get update && apt-get upgrade
libperfsonar* perfsonar-toolkit* perfsonar-oppd*” on Debian.


Mitigation
==========

N/A.

Component installation information
==================================

See the Perfsonar site [R 1]


TLP and URL
===========

** WHITE information - Unlimited distribution - see
https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2016-11363

Minor updates may be made without re-distribution to the sites

Credit
======

SVG was alerted to this vulnerability by Mischa Salle who is a member of SVG

References
==========

[R 1] http://www.perfsonar.net/#20160707-security

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========

Yyyy-mm-dd

2016-07-11 SVG alerted to this issue by Mischa Salle
2016-07-11 Acknowledgement from the EGI SVG to the reporter
2016-07-14 EGI SVG Risk Assessment completed
2016-07-11 Updated packages available <in the EGI UMD/other location>
2016-07-15 Advisory/Alert sent to sites
2016-07-15 Public disclosure

On behalf of the EGI SVG,
```
