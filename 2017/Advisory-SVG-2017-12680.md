---
title: Advisory-SVG-2017-12680
permalink: /Advisory-SVG-2017-12680
---

## Advisory-SVG-2017-12680

```
Title:       OpenStack Vulnerable Configuration problem [EGI-SVG-2017-1280]

Date:        2017-04-07
Updated:     2017-06-01  Changed to 'WHITE'

Affected software and risk
==========================

Vulnerable Configuration problem concerning OpenStack

Package :OpenStack
CVE ID  :N/A
Bug ID  :

Unprivileged access to VMs running in Openstack via unprotected VNC connection

Actions required/recommended
============================

Sites running OpenStack should urgently check if the management interfaces of
the compute nodes are accessible from outside, and carry out mitigation if
necessary.

Check all connections to compute nodes via ports 59xx

More information
================

Openstack does not provide any protection of VNC servers running on compute
nodes. Any client that has access to management network can connect to the
consoles of VMs running on compute node and obtains full access to VMs via the
console (e.g. by rebooting VMs to single-user mode).

Openstack versions: vulnerability depends on network configuration of the
installation, not the software itself.

Vulnerable configuration: compute nodes have management interfaces accessible
from clients outside of the management network and do not have firewalls

Safe configuration: management network is private or protected by firewalls

Openstack documentation emphasizes the separation of management network from
other networks (VM, data) and most of examples in the documentation have
management networks private, so the network configuration in the examples are
safe.  However, it is not explicitly required in a visible way that the
management networks must be protected (private networks, firewalls).
If the management interface of the compute node has a public IP address and is
not protected by firewalls, the system is in high risk because attackers can be
from anywhere in the world.

Exploitation of this vulnerability is extremely easy, it requires very little
effort and knowledge.  If the management IP address of the compute node is
accessible, simply use any VNC client to connect to the IP address via port
59xx to get to the console of VMs running on the compute node, reboot them to
single-user mode and have root access to the VMs.

By exploiting this vulnerability, attackers can get access only to VMs running
on compute nodes, not the host operating system on compute node or Openstack
installation.

This has already resulted in an incident in EGI.


Mitigation
==========

Ensure that the management network is private or protected by firewalls

Component installation information
==================================

N/A


TLP and URL
===========

** WHITE information - Unlimited distribution -
see https://go.egi.eu/tlp for distribution restrictions **

URL:   https://advisories.egi.eu/Advisory-SVG-2017-12680

Minor updates may be made without re-distribution to the sites


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 1]


References
==========

[R 1] https://documents.egi.eu/public/ShowDocument?docid=2538


Credit
======

This vulnerability was reported by Viet Tran, who also provided most of the
details for this alert.

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2017-12680]

2017-04-07 Vulnerability reported by Viet Tran
2017-04-07 Acknowledgement from the EGI SVG to the reporter
2017-04-07 Advisory/Alert sent to sites
2017-06-01 Changed to 'White' and placed on wiki.


Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 1] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

Others may re-use this information provided they:-

1) Respect the provided TLP classification

2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group



On behalf of the EGI SVG,
```
