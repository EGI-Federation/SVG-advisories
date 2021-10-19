---
title: SVG:Advisory-SVG-2011-1569
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

Title:        Critical Vulnerability detected in dCache Admin Web Interface
Date:        date  2011-03-30

Updated:      2011-04-08, 2011-04-19


This advisory will be placed on the public wiki in due course

URL:         https://wiki.egi.eu/wiki/EGI_CSIRT:Alerts/dCache-2011-03-30
URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2011-1569

Introduction
============

A vulnerability has been found in the dCache Admin Web Interface software which
is part of the

dCache distribution.
dCache is one of the Mass Storage Systems commonly used in EGI production
environment [R1]


Details
=======

A specially constructed http request, sent to the dCache admin web interface,
allows unauthenticated remote users to read arbitrary files on the host where
the dCache server httpdDomain is running, with 'root' privileges. The access is
read-only. Creating, modifying or executing files is not possible. The
pnfs/Chimera-file system is not affected.


Risk Category
=============

This issue has been assessed as 'Critical' risk by the EGI CSIRT and EGI SVG
Risk Assessment Team


Affected Software
=================

Components : dCache server
Subcomponent : httpdDomain
Service : dCache Admin Web Server
Since : since ever

Releases : all supported dCache server releases *prior* to:
   1.9.5-25
   1.9.10-7
   1.9.11-4

Note that the version released/to be released in EMI is not affected.
Information available at [R2]

Component Installation information
==================================

Currently software updates are available  from the dcache web-site [R1] -
instructions are available in [R 2].

Sites using
1.9.5  should update to  1.9.5.25 and above (e.g. those installed from gLite)
1.9.10 should update to  1.9.10-7 and above
1.9.11 should update to  1.9.11-4 and above

EMI - Will include 1.9.5 -25 therefore a fixed version will be in EMI.

Note, it is only necessary to  upgrade the node running the httpdDomain.

Updated 2011-04-07:

Updated version is now available in gLite for gLite 3.2/

gLite 3.2:

Release details may be found at


http://glite.cern.ch/R3.2/sl5_x86_64/updates/27/


Mitigation
==========

1. Only allow access to the dCache admin web interface (Port 2288) to
dedicated trusted hosts, using appropriate local firewall settings.

2. Run the httpdDomain as non-root where possible.

3. Run an apache webserver in front of the dCache admin interface with access
control enabled, which will completely block unauthorized access to the dCache
admin web server.

Detailed information on how to implement 2. and 3. are available in [R2]


Recommendations
===============

In addition, on the hosts that have been running the admin interface exposed
to the Internet it is recommended to change all passwords, keys, etc on that
machine, and carefully check the logs for signs of intrusions like unexpected
logins, etc.


Requirements
============

Update the affected dCache component or apply  the mitigation steps stated
above.


Other information
=================
As a basic security best practice, it is strongly recommended to restrict
access to the admin web interface with a firewall also after the security
upgrade.

EGI-CSIRT will enforce 7-day deadline, failing to act the deadline might lead
to site suspension.

All affected resources must either update the affected dCache component or apply
the mitigation actions stated above, by:

       ***2011-04-07 22:00 CEST (20:00 GMT)***

Updated 2011-04-07

Updated version of the software is now available from gLite. Sites should
update their nodes supporting httpdDomain as soon as possible, if they have not
done so already.

Updating to the latest release is the only way to full resolve the
vulnerabilities, sites can either upgrade (preferred) or take the mitigation
measures now and upgrade later.


Credits
======

This vulnerability was reported by Patrick Furhmann (dCache).


References
==========

[R1] http://www.dcache.org/
[R2] http://trac.dcache.org/projects/dcache/wiki/ProtectionOfUnsecuredWebAdminInterface


Timeline
========

2011-03-23  Vulnerability reported by Patrick Fuhrmann (dCache).
2011-03-25  Vulnerability Assessed as 'Critical' by the EGI SVG RAT and EGI-
CSIRT.
2011-03-25  Assessment by the EGI Software Vulnerability Group reported to
            the software  providers and packaging team.
2011-03-30  EGI-CSIRT advisory issued asking sites to either carry out
            mitigating action, or to upgrade from the dCache web page.
2011-04-07  Updated Version available in gLite.
2011-04-08  Sites informed by CSIRT of availability of updated version in gLite.
2011-04-19  Public disclosure by release of advisory on web.
```
