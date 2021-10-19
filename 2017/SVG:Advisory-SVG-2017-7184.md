---
title: SVG:Advisory-SVG-2017-7184
---

```
Title:   EGI SVG ALERT [TLP:WHITE] Up to 'CRITICAL' risk, kernel exploit
         CVE-2017-7184 and others [EGI-SVG-CVE-2017-7184]

Date:    2017-10-27
Updated:

Affected software and risk
==========================

Vulnerability concerning the linux kernel, which may be up to 'CRITICAL' for a
small number of configurations.

Package : linux kernel
CVE ID  : CVE-2017-7184, CVE-2017-1000111 and CVE-2017-1000112

A local root exploit vulnerability was reported some time ago concerning the
linux kernel.
In some configurations recent developments make this more serious than
concluded back in April.  [R 1] [R 2]

Actions required/recommended
============================

The vulnerability is likely to be exploitable on Worker Nodes where a kernel
option is enabled to allow the use of unprivileged user namespaces, e.g. to
allow containers to make use of.

Sites enabling that feature are urged to update the kernel and reboot their
Worker Nodes urgently.

If any site is affected by these vulnerabilities, or is aware of any further
problems with these vulnerabilities, please inform SVG by e-mail to svg-rat at
mailman.egi.eu

Affected software details
=========================

RedHat 7 and its derivatives, Ubuntu, Debian.

RedHat 6 and its derivatives are not affected.

More information
================

This was first reported back in April 2017, but at that point in time did not
pose a risk for the EGI infrastructure.

Since then things have changed. RedHat has started to allow unprivileged user
namespaces to be configured. In this case the vulnerability is exploitable and
kernel patches have been issued.

A public exploit for one of the vulnerabilities has also been released [R 3].
SVG has not tested it hence it is not confirmed whether it works.

SVG now considers it to be up to 'CRITICAL' risk in certain configurations,
which are likely to be rare in EGI at this time.

Sites running all linux versions derived from RedHat 7.4 and setting the kernel
boot parameter to enable unprivileged user namespaces will be impacted.

Such a configuration may in fact be desirable for the Singularity container
manager that some VOs (e.g. the LHC experiments) intend to use in their jobs.



Mitigation
==========

The vulnerability is avoided if user namespaces are kept privileged, i.e. the
default behaviour.


Component installation information
==================================

Sites running RedHat should see [R 4]

Sites running CentOS should see [R 5]

Sites running Scientific Linux (SL7) should see [R 6]

Sites running Debian should see [R 7,8,9]

Sites running Ubuntu should see [R 10,11,12]



TLP and URL
===========

** WHITE information - Unlimited distribution -
see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-CVE-2017-7184

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 13]


References
==========

[R 1] https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2017-7184

[R 2] https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-7184

[R 3] https://github.com/snorez/exploits/blob/master/cve-2017-7184

[R 4] https://access.redhat.com/errata/RHSA-2017:2930

[R 5] https://lists.centos.org/pipermail/centos-announce/2017-October/022605.html

[R 6] https://www.scientificlinux.org/category/sl-errata/slsa-20172930-1

[R 7] https://security-tracker.debian.org/tracker/CVE-2017-7184
[R 8] https://security-tracker.debian.org/tracker/CVE-2017-1000111
[R 9] https://security-tracker.debian.org/tracker/CVE-2017-1000112

[R 10] http://people.canonical.com/~ubuntu-security/cve/2017/CVE-2017-7184.html
[R 11] http://people.canonical.com/~ubuntu-security/cve/2017/CVE-2017-1000111.html
[R 12] http://people.canonical.com/~ubuntu-security/cve/2017/CVE-2017-1000112.html


[R 13] https://documents.egi.eu/public/ShowDocument?docid=2538

Credit
======

SVG was alerted to this vulnerability by Mischa Salle.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-CVE-2017-7184]

2017-04-04 SVG alerted to this issue by Mischa Salle
2017-04-05 Acknowledgement from the EGI SVG to the reporter
2017-04-28 Issue closed as 'No action' as no fixes for RedHat and SVG didn't
           think it relevant
2017-10-25 Issue re-opened due to fix in RedHat and further information
           available
2017-10-27 EGI SVG Risk Assessment completed
2017-10-27 Alert sent to sites


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 13] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```
