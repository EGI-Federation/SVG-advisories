---
title: Advisory-SVG-2014-7749
---

```
** WHITE information - Unlimited distribution                               **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2014-7749]

Title:   EGI SVG Advisory 'High' risk  - Unicore command injection
         vulnerability [EGI-SVG-2014-7749]

Date:    2015-02-25
Updated:

This advisory will be placed on the wiki on or after 2015-03-11

URL:         https://advisories.egi.eu/2014/Advisory-SVG-2014-7749

Introduction
============

The UNICORE TSI service [R 1] was found to be vulnerable to a command injection
attack by an authenticated user. A further vulnerability was found in UNICORE/X

This is most serious in the deployment scenario where UNICORE/X and TSI are on
same host as it means that an authenticated user could gain control over the
TSI and have access to all user data.

This vulnerability has been fixed in the version of UNICORE available in EGI
UMD 3.


Details
=======

UNICORE TSI service [R 1] is prone to OS command injection attack. An attacker
can use a UNICORE client (URC or UCC) to inject arbitrary commands into the
UNICORE TSI host.
In some configurations (for example, as used in NGI_PL) user logins into the
TSI host and user command execution on the TSI host are not allowed, so this
scenario should be considered a privilege escalation.

In case that the TSI is operating on the same host as UNICORE/X, this attack
can be further escalated.  Since UNICORE/X uses an unprivileged listen port for
the communication with the TSI, an attacker with access to shell account can
wait until UNICORE/X will be restarted to bind to this port and pretending
being UNICORE/X he/she can submit job to target system with arbitrary user
identity.  The attacker has also a very direct option to shut down UNICORE/X:
using the Linux kernel OOM Killer [R 2].

There are two vulnerabilities then: in UNICORE/TSI(1) and UNICORE/X(2) that can
together lead to serious privilege escalation.

Risk category
=============

This issue has been assessed as 'High' risk by the EGI SVG Risk Assessment Team.


Affected software
=================

UNICORE/X UNICORE TSI prior to 7.2.0

This is fixed in version 7.2.0.  Earlier versions are likely to be vulnerable.

Mitigation
==========

Mitigation is possible, however it is easier and simpler to update relevant

components.


Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

Updated versions of UNICORE/X and UNICORE TSI are available in the UMD 3.11.0
http://repository.egi.eu/2015/02/16/release-umd-3-11-0/


Sites who wish to install directly from the EMI release should see:

http://www.eu-emi.eu/releases/emi-3-monte-bianco/updates/


Recommendations
===============

Sites are recommended to update relevant components, urgently if they run
UNICORE/X and TSI on same host.


Credit
======

This vulnerability was reported by Bartlomiej Balcerek


References
==========

[R 1] https://www.unicore.eu/documentation/manuals/unicore6/files/tsi/tsi-manual.pdf
[R 2] https://www.kernel.org/doc/gorman/html/understand/understand016.html

Timeline
========
Yyyy-mm-dd

2014-12-04 Vulnerability reported by Bartlomiej Balcerek
2014-12-04 Acknowledgement from the EGI SVG to the reporter
2014-12-04 Software providers responded and involved in investigation
2014-12-10 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2015-02-16 Updated packages available in the EGI UMD.
2015-02-25 Advisory sent to sites
2015-03-31 Public disclosure
```
