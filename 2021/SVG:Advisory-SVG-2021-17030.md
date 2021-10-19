---
title: SVG:Advisory-SVG-2021-17030
permalink: /SVG:Advisory-SVG-2021-17030/
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] CRITICAL risk - 2 HTCondor
         Vulnerabilities affecting a limited number of versions.
         [EGI-SVG-2021-17030]

Date:    2021-01-15
Updated: 2021-03-22

Affected software and risk
==========================

2 CRITICAL risk vulnerabilities concerning HTCondor

Package : HTCondor

2 vulnerabilities have been found concerning HTCondor, affecting a limited
number of versions.
One may allow any authenticated user to impersonate any other user on the
Condor system, and potentially reconfigure the HTCondor daemons.  The other may
allow any authenticated user to  overwrite any file.


Actions required/recommended
============================

Any site running HTCondor versions 8.9.2 through 8.9.10 should consider taking
action.

There are 3 options, install the 8.8.X stable series, update prior to the
public release using the instructions below, or carry out the mitigation below
until the fix is released publicly.

Releases 8.8.X (STABLE SERIES) are NOT vulnerable.

Mitigation
==========

From the HTCondor team:--

For the impersonation vulnerability affecting HTCondor 8.9.2 through 8.9.10
(inclusive):--

If you do not need to use IDTOKENS, you can disable that authentication method
by specifying a list of authentication mechanisms that does not include it.

On Linux, you would want to set, e.g., (removing any other methods you did not
want to use):
SEC_DEFAULT_AUTHENTICATION_METHODS = FS,PASSWORD,SSL,GSI,KERBEROS,MUNGE

On Windows, you would want to set, e.g., (removing any other methods you did
not want to use):
SEC_DEFAULT_AUTHENTICATION_METHODS = NTSSPI,PASSWORD,SSL,KERBEROS

You should also check your configuration for other places you may have
explicitly set the list of methods:
condor_config_val -dump AUTHENTICATION_METHODS
After making any changes, you will need to run
condor_reconfig

For the File overwrite Vulnerability:--

Do not enable the condor_credd if you are not depending on it.


Component installation information
==================================

From the HTCondor team:--

If you decide to install v8.9.11 ahead of the public release on January 27, you
will need to add an additional repository to your system as detailed below.

After January 27, the v8.9.11 release will be in the usual public HTCondor
repositories, so you can upgrade in your usual manner.

Use the repo that matches your system:

    (cd /etc/yum.repos.d; wget "repo URL")

Enterprise Linux 7:

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/repo/8.9/el7/private/htcondor-v8911.repo

Enterprise Linux 8:

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/repo/8.9/el8/private/htcondor-v8911.repo

Amazon Linux 2:

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/repo/8.9/amzn2/private/htcondor-v8911.repo

If you are installing on a Debian/Ubuntu use the security repository in
addition to the regular repository.

Use the repo that matches your system:

    (cd /etc/apt/sources.list.d; wget "repo URL")

Debian 9 (stretch):

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/debian/8.9-private/htcondor-v8911-stretch.list

Debian 10 (buster):

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/debian/8.9-private/htcondor-v8911-buster.list

Ubuntu 16 (xenial):

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/ubuntu/8.9-private/htcondor-v8911-xenial.list

Ubuntu 18 (bionic):

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/ubuntu/8.9-private/htcondor-v8911-bionic.list

Ubuntu 20 (focal):

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/ubuntu/8.9-private/htcondor-v8911-focal.list

Tarballs can be picked up at:

https://v8911:GsktumXnevC8SwGE@research.cs.wisc.edu/htcondor/tarball/8.9/8.9.11/private/

Affected software details
=========================

Impersonation vulnerability in HTCondor 8.9.2 through 8.9.10 (inclusive)

File overwrite vulnerability in HTCondor 8.9.7 through 8.9.10 (inclusive)

Both these issues are fixed in HTCondor version 8.9.11.

Releases 8.8.X STABLE SERIES are NOT vulnerable.


More information
================

These vulnerabilities are NOT publicly known about and the HTCondor team is not
aware of any site where either have been exploited yet.


TLP and URL
===========

** WHITE information - Unlimited distribution
 - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2021-17030

Minor updates may be made without re-distribution to the sites.


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was alerted to this vulnerability by Zach Miller from the HTCondor Team

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2021-17030]

2021-01-13 SVG alerted to this issue by Zach Miller from the HTCondor Team.
2021-01-14 Acknowledgement from the EGI SVG to the reporter
2021-01-14 EGI SVG Risk Assessment completed
2021-01-15 Advisory sent to sites
2021-03-22 Advisory placed on SVG Wiki

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

-----------------------------
This advisory is subject to the Creative commons licence
https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/
Software Vulnerability Group must be credited.
-----------------------------


Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
