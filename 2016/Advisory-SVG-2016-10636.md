---
title: Advisory-SVG-2016-10636
permalink: /Advisory-SVG-2016-10636
---

## Advisory-SVG-2016-10636

```

Title:   EGI SVG Advisory [TLP:WHITE] Moderate risk - OpenStack sites VM
         Management permissions - check [EGI-SVG-2016-10636]

Date:    2016-04-13
Updated: 2016-04-28 - Set to [TLP:WHITE] and placed on the wiki.


Affected Software and Risk
==========================

Some OpenStack sites have been found to have incorrect Management permissions.


Actions Required/Recommended
============================

Sites in the EGI Federated cloud should check they are correctly configured,
see [R 1].

Risk category
=============

This issue has been assessed as 'Moderate' by the EGI SVG Risk Assessment Team.

More information
================

Some cloud sites running OpenStack have been found to use the default
configuration where every group member can manage the VMs of the group. The EGI
installation manual for OpenStack includes a policy to avoid this behaviour [R
1], although it seems not to be applied everywhere.

This default configuration includes deleting other people's VMs (which is what
some people have suffered from) or changing their public IPs.

This issue is exploitable by all other members of the VO of which the VM
Operator is a member.

There was a concern that using the OpenStack APIs with this kind of permission
might allow a user to "rescue" someone else's VM [R 2] and thereby access the
original VM disks, and hence any credentials or other private data stored
there.  However, such abuse would be prevented by the OpenStack security
framework.

An incorrect configuration thus would allow denial of service and loss of
(transient) data.

We ask sites to check their configuration and modify if necessary.


URL/TLP
=======

** WHITE information - Unlimited distribution                               **
** See https://go.egi.eu/tlp for distribution restrictions **

URL:   https://advisories.egi.eu/Advisory-SVG-2016-10636

Minor updates may be made without re-distribution to the sites

Credit
======

SVG was alerted to this vulnerability by Enol Fernandez

References
==========

[1] https://wiki.egi.eu/wiki/MAN10#OpenStack_installation
[2] http://docs.openstack.org/cli-reference/nova.html#nova-rescue


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-10636]

2016-03-01 SVG alerted to this issue by Enol Fernandez
2016-03-01 Acknowledgement from the EGI SVG to the reporter
2016-03-01 Investigation of this problem began.
2016-03-23 At SVG meeting still not clear whether or not exploit more than
           deleting or re-starting VMs.
2016-04-13 Advisory/Alert sent to sites as 'Amber' to check configuration
2016-04-28 Advisory placed on Wiki
```
