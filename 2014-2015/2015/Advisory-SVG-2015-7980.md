---
title: Advisory-SVG-2015-7980
permalink: /Advisory-SVG-2015-7980
---

## Advisory-SVG-2015-7980

```
** White information - unlimited distribution                               **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG ADVISORY [EGI-SVG-2015-7980]

Title:   EGI SVG Advisory "Moderate" risk - DPM Wiki instructs insecure
         configuration if configured 'memcached' [SVG EGI-SVG-2015-7980]

Date:    2015-01-14
Updated:


URL:         https://advisories.egi.eu/2015/Advisory-SVG-2015-7980

Introduction
============

Some instructions on the Wiki for DPM configuration instructed sites to
configure insecurely if the DMLite memcache plugin is used. [R 1]

At least one site has been found to have this insecure configuration. Therefore
this advisory is to instruct sites who use DPM and configure 'memcached' to
check their configuration and modify if necessary.

These instructions have since been fixed.

Details
=======

On the DPM wiki there are instructions to configue the DPM cluster using the
DMLite memcache plugin. [R 1]

If the instructions in the section entitled 'The memcached daemon' were
followed the memcached is accessible from the whole world. For many sites
firewalling may prevent the exploitation of this vulnerability, although that
was not the case for at least 1 site.

It is not clear how many sites in the EGI infrastructure are vulnerable, but
since any that followed the wiki instructions are vulnerable we must assume
that it is not an isolated problem.

In this case the information which may be obtained is not considered
particularly sensitive, hence the risk category.


Risk category
=============

This issue has been assessed as 'Moderate' risk by the EGI SVG Risk Assessment
Team for sites configured insecurely

Affected software
=================

DPM

This was a problem with the configuration instructions NOT a problem with the
software itself.


Mitigation
==========

The instructions should state:--

 [root@lxfsra04a04 log]# cat /etc/sysconfig/memcached  PORT="11211"
 USER="memcached"
 MAXCONN="8192"
 CACHESIZE="2048"
 OPTIONS="-l 127.0.0.1 -U 11211 -t 4"

- it's the OPTIONS that was previously incorrect.

Recommendations
===============

Sites who use DPM should check and modify their configuration if necessary as
soon as possible.


Credit
======

This vulnerability was reported by David Groep from Nikhef.


References
==========

[R 1]   https://svnweb.cern.ch/trac/lcgdm/wiki/Dpm/Admin/TuningHints

Timeline
========

Yyyy-mm-dd

2015-01-09 Vulnerability reported by David Groep from Nikhef
2015-01-12 Acknowledgement from the EGI SVG to the reporter
2015-01-12 Advisory drafted.
2015-01-13 Risk assessment agreed
2015-01-13 Wiki fixed
2015-01-14 Advisory sent to sites
2015-01-14 Public disclosure
```
