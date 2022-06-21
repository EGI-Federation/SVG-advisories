---
title: Advisory-SVG-2016-10837
---

```
Title:   EGI SVG Advisory [TLP:WHITE] 'High' risk Configuration issue
         concerning dCache [EGI-SVG-2016-10837]

Date:    2016-05-25
Updated:

Affected Software and Risk
==========================

'HIGH' risk configuration issue concerning dCache

Package :dCache

Actions Required/Recommended
============================

Sites running dCache should check the configuration of the firewalls against
information in [R 1] and modify if necessary.  Sites may also follow the
instructions below.

Affected software Details.
==========================

This is not a software vulnerability, but some sites running dCache have been
found to have an insecure configuration (and have already been informed) but we
recommend that all sites running dCache check.

A badly configured site could allow the execution of arbitrary commands.

Component installation information
==================================

N/A

TLP and URL
===========

** WHITE information - Unlimited distribution                               **
** See https://go.egi.eu/tlp for distribution restrictions **

URL:   https://advisories.egi.eu/2016/Advisory-SVG-2016-10837

Minor updates may be made without re-distribution to the sites

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Full description and instructions provided by dCache
====================================================

Executive summary:

Sites that have not correctly configured a server-local firewall restricting
UDP and TCP port 11111 traffic on the server hosting dCacheDomain are allowing
an attacker to execute arbitrary commands within the dCache cluster (e.g.,
delete all data) and, by extension, run arbitrary shell commands on any server
within the dCache cluster, as whichever user dCache is running under.

VULNERABILITY #1

Description:

    The dCache "LocationManager" component is responsible for
    establishing the network topology for the internal dCache
    communication.  One central "broker" server (by default, whichever
    server hosts dCacheDomain) listens for incoming UDP communication.
    This is on port 11111 by default.  All nodes within a dCache
    cluster must be able to communicate with this LocationManager.  It
    responds with information instructing a domain on how to connect
    to the rest of the dCache cluster.

    By allowing non-dCache servers to access UDP port 11111, an
    attacker is able to issue queries and commands to LocationManager.
    Careful control of these requests will allow the LocationManager
    to overwrite files on that node's local filesystem and execute
    arbitrary commands on the node running LocationManager.  The
    attacker can adjust LocationManager configuration so that domains
    that connect subsequently will relay traffic from the attacker;
    allowing her to execute arbitrary commands within dCache (e.g.,
    delete all data) and execute arbitrary shell commands on any
    server within the dCache cluster.

    Please note that site-level firewalls are only a partial solution.
    Most sites that deploy dCache also allow users from throughout the
    world to submit jobs to their HTC cluster facility.  Network
    connections from such worker nodes will likely bypass site-level
    firewalls.

    Please further note that, because UDP is a connectionless
    protocol, there is the risk of a UDP reflection attack.  If
    firewall rules fail to exclude traffic from a server running
    another UDP service (e.g., ntp, tftp) then an attacker could send
    requests to that UDP service with a faked source IP address: that
    of the server running LocationManager.  If the response from that
    server, which it will send to LocationManager, is a valid
    LocationManager command, the attacker will have successfully
    bypassed the firewall rules that forbid direct communication.


Test for vulnerability:

    Running the following command from a non-dCache-cluster machine
    checks for this vulnerability on machine hosting dCacheDomain
    ("dcache-node.example.org" here) :

        echo "ls setup" | nc -q1 -u dcache-node.example.org 11111

    Typical output if vulnerable:

        paul@sparkplug:~$ echo "ls setup" | nc -u localhost 11111
        #
        # This setup was created by the LocationManager at Mon Mar 14 10:29:36
        # CET 2016
        #
        define dCacheDomain
        listen dCacheDomain
        define *
        defaultroute * dCacheDomain
        connect * dCacheDomain
        paul@sparkplug:~$

    Typical output if not vulnerable:

        paul@sparkplug:~$ echo "ls setup" | nc -u localhost 11111
        paul@sparkplug:~$


Limiting factors:

    Commands are only executed on nodes within the dCache cluster.

    By default, RPM- and deb- based dCache deployments run as the
    unprivileged user "dcache", limiting the damage on the server.


Mitigation:

    The admin configures a machine-local firewall (e.g., iptables) so
    that it only accepts UDP port 11111 traffic from machines within
    the dCache cluster.

    A valid configuration to allow three machines to communicate with
    LocationManager while preventing attempts from all other machines:

        iptables -A INPUT -p udp --dport 11111 -s 203.0.113.10 -j ACCEPT
        iptables -A INPUT -p udp --dport 11111 -s 203.0.113.11 -j ACCEPT
        iptables -A INPUT -p udp --dport 11111 -s 203.0.113.12 -j ACCEPT
        iptables -A INPUT -p udp --dport 11111 -j REJECT

    A configuration that allows members of a subnet to access
    LocationManager while preventing attempts from all other machines:

        iptables -A INPUT -p udp --dport 11111 -s 203.0.113.0/24 -j ACCEPT
        iptables -A INPUT -p udp --dport 11111 -j REJECT


VULNERABILITY #2

Description:

    Domains pass messages between themselves using TCP connections.
    By default, these TCP connections use port 11111.

    By allowing non-dCache nodes to connect to TCP port 11111, an
    attacker can issue arbitrary internal dCache commands on any node
    within the dCache cluster; this includes the ability to delete any
    data stored in dCache.  Additionally, these dCache commands allow
    the attacker to issue arbitrary external shell commands on the
    servers.

    Please note that site-level firewalls that block port 11111 are
    only a partial solution.  Most sites that deploy dCache also allow
    users from throughout the world to submit jobs to their HTC
    cluster facility.  Network connections from such worker nodes will
    likely bypass site-level firewalls.

Test for vulnerability:

    Running the following command from a non-dCache-cluster machine
    checks for this vulnerability on machine hosting dCacheDomain
    ("dcache-node.example.org" here) :

        echo "" | nc -q1 core.dcache-cluster.example.org 11111

    Typical output if vulnerable:

        paul@sparkplug:~$ echo "" | nc localhost 11111
        ..sr dmg.cells.nucleus.CellDomainInfo.g$5.L
                _domainNametLjava/lang/String;_versionq~xpt
                        dCacheDomaint2.15.2-SNAPSHOT
        paul@sparkplug:~$

    Typical output if not vulnerable:

        paul@sparkplug:~$ echo "" | nc localhost 11111
        paul@sparkplug:~$


Limiting factors:

    The attacker can only run commands as whichever user the dCache
    JVM is running.  By default, RPM- and deb- based dCache
    deployments run as the unprivileged user "dcache", limited the
    operations that the attacker can undertake.


Mitigation:

    The admin configures a local firewall (e.g., iptables) on the
    machine running dCacheDomain so that it only allows TCP port 11111
    connections from machines within the dCache cluster.

    A valid configuration to allow three machines to join the dCache
    cluster while preventing attempts from all other machines:

        iptables -A INPUT -p tcp --dport 11111 -s 203.0.113.10 -j ACCEPT
        iptables -A INPUT -p tcp --dport 11111 -s 203.0.113.11 -j ACCEPT
        iptables -A INPUT -p tcp --dport 11111 -s 203.0.113.12 -j ACCEPT
        iptables -A INPUT -p tcp --dport 11111 -j REJECT

    A configuration that allows members of a subnet to join the
    dCache cluster while preventing attempts from all other machines:

        iptables -A INPUT -p tcp --dport 11111 -s 203.0.113.0/24 -j ACCEPT
        iptables -A INPUT -p tcp --dport 11111 -j REJECT

Credit
======

SVG was alerted to this problem by Paul Millar from the dCache team

References
==========

[R 1] https://www.dcache.org/manuals/Book-2.10/start/in-securing.shtml

Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-10837]

2016-04-07 SVG alerted to this issue by Paul Millar and information available
2016-04-07 Acknowledgement from the EGI SVG to the reporter
2016-04-21 EGI SVG Risk Assessment completed
2016-      Further discussion on how to approach this.
2016-05-09 Sites known to be vulnerable ticketed by CSIRT
2016-05-25 All sites running dCache are recommended to check their
           configuration
2016-06-08 Advisory placed on Wiki
```
