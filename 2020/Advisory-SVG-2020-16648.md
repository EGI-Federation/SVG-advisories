---
title: Advisory-SVG-2020-16648
---

```
Title:   EGI SVG 'ADVISORY' [TLP:WHITE] Singularity and unprivileged user
         namespaces  [EGI-SVG-2020-16648]

Date:    2020-05-06
Updated: 2020-05-12

Affected software and risk
======================

Here we provide an important recommendation.

Package : Singularity

Red Hat Enterprise Linux 7 supports a kernel feature called unprivileged user
namespaces that enables Singularity to run completely unprivileged.
There is a significantly lower risk of future vulnerabilities if Singularity
runs unprivileged, compared to the default setup of Singularity which has
setuid root enabled.

Actions required/recommended
============================

Sites are asked to enable unprivileged user namespaces on their worker nodes.
Where possible, and when there is a convenient opportunity, sites should
additionally either remove the Singularity rpm or change its configuration to
run unprivileged. This depends on what kinds of Singularity workflows a site
allows to be used by VOs that are supported by the site. No LHC experiment
requires Singularity rpms to be installed anymore. In principle some other VO
might expect Singularity rpms to installed and also might require it to have
setuid allowed for particular workflows.

Detailed recipes for the configuration changes are provided below.

Component installation information
==================================

See OSG information below.

More information
================

While EGI SVG does not normally send advisories unless a specific vulnerability
has been found, our partners in OSG now recommend sites change their
Singularity configuration and EGI SVG considers it appropriate to do the same
at this time.

**UPDATE 2020-05-12**

Decided to change to [WHITE] earlier than previously stated to help publicize
encouraging a change to a more secure configuration when there is no
vulnerability to potentially protect from future vulnerabilities.

OSG Information
================

Dear OSG Security Contacts,

Red Hat Enterprise Linux 7 supports a kernel feature called unprivileged user
namespaces that enables singularity to run completely unprivileged.  All OSG
VOs (including WLCG VOs) that use singularity are now configured to run
singularity unprivileged out of CVMFS when they can.  OSG security believes
this to be a significantly lower risk than having singularity installed with
setuid root enabled.  We recommend that sites enable unprivileged user
namespaces on their RHEL 7 worker nodes if they haven't, and remove singularity
rpms if there is no non-OSG requirement to keep them.

IMPACTED VERSIONS:

RHEL 7.6 and later are affected.
RHEL 8 has unprivileged user namespaces enabled by default.
RHEL 6 cannot enable unprivileged user namespaces.

WHAT ARE THE VULNERABILITIES:

There are no known current exploits with setuid root singularity, but there
have been in the past.
Setuid root programs are notoriously difficult to secure, and there are likely
to be more exploits discovered in the future.

WHAT YOU SHOULD DO:

On RHEL 7 worker nodes, enable unprivileged user namespaces by following the
instructions on the OSG singularity installation page [1].
 Then, if you have no requirement to keep the rpm installed for non-OSG
 purposes, remove singularity rpms from your worker nodes.
 If your singularity installation is version 2, instead remove
 singularity-runtime rpms.  If you have to keep the singularity rpm installed,
 consider setting the configuration 'allow setuid = no'.  More information on
 making that choice is available [2].

Note that if there were local changes to singularity.conf, VOs will no longer
be using them.  Extra local bind paths can be added to jobs through the
SINGULARITY_BINDPATH environment variable.

REFERENCES

[1] https://opensciencegrid.org/docs/worker-node/install-singularity/#enabling-unprivileged-singularity
[2] https://opensciencegrid.org/docs/worker-node/install-singularity/#choosing-unprivileged-vs-privileged-singularity

TLP and URL
===========

** WHITE information - Unlimited  distribution
 - see https://go.egi.eu/tlp for distribution restrictions **
URL:   https://advisories.egi.eu/2020/Advisory-SVG-2020-16648

Minor updates may be made without re-distribution to the sites

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 3]

Note that this is undergoing revision to fully handle vulnerabilities in the
EOSC-hub era.

References
==========

See references in OSG information

[R 3] https://documents.egi.eu/public/ShowDocument?docid=3145

Credit
======

SVG was informed of the plan to request sites to enable unprivileged namespaces
when running singularity by Dave Dykstra.

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2020-16648]

2020-04-28 EGI SVG informed of OSG's plan to request sites to enable
           unprivileged namespaces when running singularity by Dave Dykstra
2020-04-30 Acknowledgement from the EGI SVG
2020-05-04 EGI SVG drafted advisory for EGI sites ready for when OSG make
           announcement
2020-05-06 Advisory sent to sites
2020-05-12 Changed to [WHITE] Advisory placed on wiki.

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 3]  in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct.  The risk may also be higher or lower in other deployments depending
on how the software is used.

-----------------------------
This advisory is subject to the Creative commons license
https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/
Software Vulnerability Group must be credited.
-----------------------------

Note that the SVG issue handling procedure is currently under review, to take
account of the increasing inhomogeneity of the EGI infrastructure and the
services in the EOSC-hub catalogue.

On behalf of the EGI SVG,
```
