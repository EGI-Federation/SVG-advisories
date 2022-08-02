---
title: Advisory-SVG-2022-17581
permalink: /Advisory-SVG-2022-17581
published: false
---

## Advisory-SVG-2022-17581

```
Title:   EGI SVG 'ALERT' [TLP:WHITE]  CRITICAL risk - xcache image 
         vulnerability and image purge 

Date:    2022-02-21
Updated: 2022-08-02

CRITICAL risk vulnerability concerning xcache in version built by OSG

Package    :  xcache built by OSG
CVE ID     : 
Bug ID     : 
CVSS Score : 


Below is an announcement which OSG sent concerning xcache container 
images pulled from OSG DockerHub and OSG Harbor prior to Feb 16, 2022.  
It is not clear whether EGI has sites making use of these images, 
but the potential impact is high.  Sites using xcache for other purposes
may with to check.

The information below is forwarded from OSG. 

EGI SVG is not aware of any other versions of xcache being vulnerable.


Information from OSG.
=====================


A CRITICAL security flaw was detected in OSG XCache images published in 
DockerHub [1] and OSG's Harbor [2] which could compromise the integrity 
and confidentiality of data on other containers for all varieties of
XCache and XRootD standalone.

To mitigate this flaw, the OSG software team has pushed new images to 
DockerHub and will be purging all images prior to February 16, 2022.

Show quoted text

You will need to update to the latest image and restart all affected 
containers by the end of Feb 17, 2022.  Containers running images 
older than 2/16/22 are considered vulnerable and may no longer 
function as expected.

To download the latest image:

docker pull opensciencegrid/<IMAGE NAME>:release

Where <IMAGE NAME> is one of [1]:
atlas-xcache
cms-xcache
stash-cache
stash-origin
xcache
xrootd-standalone

Show quoted text
[1]
https://hub.docker.com/r/opensciencegrid/atlas-xcache
https://hub.docker.com/r/opensciencegrid/cms-xcache
https://hub.docker.com/r/opensciencegrid/stash-cache
https://hub.docker.com/r/opensciencegrid/stash-origin
https://hub.docker.com/r/opensciencegrid/xcache
https://hub.docker.com/r/opensciencegrid/xroot-standalone

[2]
https://hub.opensciencegrid.org/harbor/projects/4/repositories/atlas-xcache
https://hub.opensciencegrid.org/harbor/projects/4/repositories/cms-xcache
https://hub.opensciencegrid.org/harbor/projects/4/repositories/stash-cache
https://hub.opensciencegrid.org/harbor/projects/4/repositories/stash-origin
https://hub.opensciencegrid.org/harbor/projects/4/repositories/xcache
https://hub.opensciencegrid.org/harbor/projects/4/repositories/xrootd-standalone

If you have any questions, please contact security@opensciencegrid.org

Sincerely,
OSG Security Team


TLP and URL
===========
** WHITE information - Unlimited distribution
 - see https://go.egi.eu/tlp for
   distribution restrictions **
   
URL: https://advisories.egi.eu/Advisory-SVG-2022-17581
Minor updates may be made without re-distribution to the sites

Comments
========
Comments or questions should be sent to svg-rat  at  mailman.egi.eu
If you find or become aware of another vulnerability which is relevant to EGI
you may report it by e-mail to
report-vulnerability at egi.eu
the EGI Software Vulnerability Group will take a look according to the
procedure defined in [R 99]

References
==========

[R 99] https://documents.egi.eu/public/ShowDocument?docid=3867

Credit
======
SVG was alerted to this vulnerability by Josh Drake of the OSG Security Team

Timeline  
========
Yyyy-mm-dd  [EGI-SVG-2022-17581] 

2022-02-17 SVG alerted to this issue by Josh Drake of the OSG Security Team
2022-02-18 Acknowledgement from the EGI SVG to the reporter
2022-02-18 Decided on an 'Alert' forwarding this OSG information in case 
           some EGI sites are using the affected version of xcache
2022-02-21 Alert sent to sites
2022-08-02 Alert placed on advisories.egi.eu web page

Context
=======
This advisory has been prepared as part of the effort to fulfil EGI SVG's
purpose "To minimize the risk to the EGI infrastructure arising from software
vulnerabilities"
The risk is that assessed by the group, according to the EGI SVG issue handling
procedure [R 99] in the context of how the software is used in the EGI
infrastructure. It is the opinion of the group, we do not guarantee it to be
correct. The risk may also be higher or lower in other deployments depending on
how the software is used.

-----------------------------
This advisory is subject to the Creative commons licence 
https://creativecommons.org/licenses/by/4.0/ 
and the EGI https://www.egi.eu/ Software Vulnerability Group must be credited. 
-----------------------------

On behalf of the EGI SVG,
```
