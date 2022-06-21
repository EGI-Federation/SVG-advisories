---
title: Advisory-SVG-2011-1474
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://go.egi.eu/tlp for distribution restrictions **

EGI SVG   ADVISORY [EGI-SVG-2011-1474]

Title:       'Low' RISK - gLExec - processes not properly cleaned up.
Date:        2012-05-09
Updated:     2012-11-15

URL:         https://wiki.egi.eu/wiki/Advisory-SVG-2011-1474

Introduction
============

A vulnerability has been found in gLExec allowing a malicious job to remain
executing, consume resources and possibly attack subsequent jobs.

gLExec Version 0.9 has been released as part of EMI 2, and released in
EGI UMD 2, which allows these problems to be mitigated by enabling sites to
write an epilogue script to clean up processes.

It is not possible to provide an epilogue script which is suitable for all
systems, but examples are available.



Details
=======

gLExec is an identity switching program which allows a job to execute under a
different identity. This identity is selected using the user provided X.509
credential, and one of the various mapping services used on the Grid.

A detailed vulnerability assessment of gLExec 0.8 was carried out by
Daniel Crowell from the  University of Wisconsin Vulnerability assessment
group [R 1] and this vulnerability was reported.

It was found that it is possible for a malicious user to produce code to fork a
new process and this could remain running after the batch system had concluded
that the job was no longer running. Such a job could consume resources, carry
out any action for which the user was authorized, and possibly if the identity
is re-used attack a subsequent job.

This cannot be fully resolved simply by producing another version of gLExec

alone, however in gLExec 0.9 provision has been made to allow sites to produce
an epilogue script to clean up processes. The exact contents of this script
will depend on the batch system and configuration of each site.



Risk category
=============

This issue has been assessed as 'Low' risk by the EGI SVG Risk Assessment Team.

The 'Low' risk category was largely due to similar problems being accepted
in the Grid environment for a number of years, See for example [R 2].



Affected software
=================

Versions of gLExec earlier than 0.9.0 are affected.

Better handles are provided in version 0.9.0 which ensure a more complete
cleanup

of processes after gLExec exits.

gLExec version 0.9.0 is released as part of EMI 2, which is also released in
EGI UMD 2.



Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites is
repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).

The EGI UMD 2 distribution is available from:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/



Recommendations
===============

Sites should be aware of the problem that processes could be left behind.

Sites should update in due course, as is convenient to them.

Sites should also include a suitable epilogue script, the choice depending
on the particular batch system configuration in use at the particular site
and the local site policy. Documentation is available in the man pages for
gLExec and in release notes on how to write a suitable epilogue script
[R 3], [R 4].

It is recommended that gLExec is executed in Linger mode with identity
switching turned on. This allows cleanup scripts to be effective. It is
important that sites do re-configure gLExec. Documentation [R 3] should be
referred to.



Further information
===================

In general gLExec now tries to cleanup the processes it has spawned by sending
first a SIGTERM followed by a SIGKILL if needed. However, it does not enforce
killing potentially daemonized processes.  Certain batch systems use tracking

group IDs (SGE, Condor) and an LCMAPS plugin which can preserve these is
available. Whether this plugin needs to be ran or not depends on your site.
The LCMAPS plugin is now by default installed on a gLExec-wn.

A similar problem occurs for gLExec in use with Condor.

Distribution of advisory delayed until solution available to sites installing
software from the EGI UMD, as SVG in contact with the developers and was aware
that progress was taking place.

Credit
======

This vulnerability was reported by Daniel Crowell of the University of
Wisconsin.


References
==========


[R 1] http://research.cs.wisc.edu/mist/includes/vuln.html

[R 2] http://www.gridpp.ac.uk/gsvg/advisories/advisory-9054.txt

[R 3] https://wiki.nikhef.nl/grid/GLExec

[R 4] https://wiki.nikhef.nl/grid/GLExec_Epilogue_Functionality



Timeline
========
Yyyy-mm-dd

2011-03-08 Vulnerability reported by Daniel Crowell
2011-03-08 Acknowledgement from the EGI SVG to the reporter
2011-03-08 Software providers responded and involved in investigation and
           discussion on how to resolve this.
2011-03-16 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2012-08-07 Updated packages available in the EGI UMD 2
2012-11-15 Confirmed correct packages in EGI UMD 2
2012-11-15 Public disclosure
```
