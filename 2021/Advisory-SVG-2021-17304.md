---
title: SVG:Advisory-SVG-2021-17304
---

```
Title:   EGI SVG 'ADVISORY' **UPDATE** [TLP:WHITE] 'HIGH' risk - 2 HTCondor
         Security Vulnerabilities [EGI-SVG-2021-17304]

Date:    2021-07-29
Updated: 2021-08-03, 2021-09-07

Affected software and risk
==========================

2 vulnerabilities concerning HTCondor, one of which is HIGH risk.

Package : HTCondor

2 vulnerabilities in HTCondor [R 1] [R 2] have been found and fixed by the
HTCondor team, including one which may allow a user to run code as another user
and/or read the data accessible to that user's running jobs, this is considered
'HIGH' risk for the EGI infrastructure. The second vulnerability applies only
to sites that have enabled the use of SciTokens.

**UPDATE 2021-09-07**

Changed to [TLP:WHITE] and placed on the wiki.

**UPDATE 2021-08-03**

HTCONDOR-2021-0003 [R 1] was NOT fully resolved in the previous release
referred to in the advisory on 2021-07-29, therefore the HTCondor team have
released another version.

Actions required/recommended
============================

Sites running HTCondor are recommended to update as soon as they reasonably
can.

Component installation information
==================================

HTCondor may be downloaded from [R 3]

See 'more information' below from the HTCondor team and OSG.

Affected software details
=========================

**UPDATE 2021-08-03 **

HTCONDOR-2021-0003 [R 1] was NOT fully resolved in versions 8.8.14, 9.0.3,
9.1.1

These vulnerabilities are fixed in the following versions of HTCondor

  8.8.15, 9.0.4,  9.1.2


More information  - Provided by the HTCondor team/OSG
======================================================

**UPDATE 2021-08-03**

referring to HTCondor 8.8.14, 9.0.3, and 9.1.1.

Unfortunately, these releases did not fully mitigate the vulnerability
described in HTCONDOR-2021-0003.
An attacker with access to the SchedLog file in the HTCondor LOG directory is
still able to exploit this vulnerability.

We are now releasing HTCondor 8.8.15, 9.0.4, and 9.1.2 to fully address this
issue.


These releases contain important fixes for security issues.
Affected users should update as soon as possible.

More details on the security issues are in the Vulnerability Reports [R 1] [R
2]



From OSG:--

Two security vulnerabilities have been discovered in HTCondor,
HTCONDOR-2021-0003 [R 1] and HTCONDOR-2021-0004 [R 2], both of which allow
unprivileged users to perform unauthorized actions.

 The OSG Security team considers these vulnerabilities to be of HIGH severity
 and recommend updating HTCondor to the fixed version as soon as possible.

 ## IMPACTED VERSIONS:

 HTCONDOR-2021-0003 affects SchedD and Collector components in all versions of
 HTCondor.
 HTCONDOR-2021-0004 affects all daemons from version 9.0.0 and above.

 ## WHAT IS THE VULNERABILITY:

 HTCONDOR-2021-003 allows a user with read access to a SchedD or Collector to
 discover secrets that could allow them to control other user's jobs and/or
 read their data.

 HTCONDOR-2021-004 may allow users bearing a SciToken to be granted
 authorizations beyond what the token should allow.

 ## WHAT YOU SHOULD DO:

Update any HTCondor-CEs, HTCondor access points, and HTCondor central managers
to a fixed version of the software [R 3] (8.8.14, 9.0.3 or 9.1.1) as soon as
reasonably possible.

A workaround for HTCONDOR-2021-0004 can be implemented by not allowing
SciTokens as an authentication method until the patch can be applied. This
means overriding the list of authentication methods (which includes SciTokens
by default) by setting SEC_DEFAULT_AUTHENTICATION_METHODS to all the methods
you would actually like to use. To simply remove SciTokens, set it to
"FS,TOKEN,KERBEROS,GSI,SSL". [R 2]



TLP and URL
===========

** WHITE information - Unlimited distribution
- see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

URL:   https://wiki.egi.eu/wiki/Advisory-SVG-2021-17304

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 4]

Note that this is undergoing revision.


References
==========

[R 1] http://htcondor.org/security/vulnerabilities/HTCONDOR-2021-0003.html

[R 2] http://htcondor.org/security/vulnerabilities/HTCONDOR-2021-0004.html

[R 3] https://research.cs.wisc.edu/htcondor/downloads.html

[R 4] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

This vulnerability was reported by to SVG by Zach Miller of the HTCondor team


Timeline
========

Yyyy-mm-dd  [EGI-SVG-2021-17304]

2021-06-23 Vulnerability reported by Zach Miller of the HTCondor team, info
           shared with SVG
2021-06-24 Acknowledgement from the EGI SVG to the reporter
2021-07-28 Updated packages available
2021-07-28 EGI SVG Risk Assessment completed
2021-07-29 Advisory sent to sites
2021-08-03 Advisory updated due to new information from the HTCondor team,
           stating that 1 vulnerability had no fully resolved previously.
2021-09-07 Advisory placed on SVG wiki


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 4]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.  The risk may also be higher or lower in other deployments depending
on how the software is used.

-----------------------------
This advisory is subject to the Creative commons licence
https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/
Software Vulnerability Group must be credited.
-----------------------------

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure.

On behalf of the EGI SVG,
```
