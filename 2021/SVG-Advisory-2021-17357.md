---
title: Advisory-SVG-2021-17357
permalink: /Advisory-SVG-2021-17357
published: false
---

## Advisory-SVG-2021-17357

```
Title:       EGI SVG 'ADVISORY' [TLP:WHITE] MODERATE risk vulnerability 
             in dCache concerning access control [EGI-SVG-2021-17357]  

Date:        2021-10-21
Updated:     

Affected software and risk
==========================

MODERATE risk vulnerability concerning dCache

Package : dCache

A vulnerability has been found in dCache where a group ACL might apply to a 
user with the same numeric id. This may in some rare circumstances allow a 
user to gain access to restricted resources. 

Actions required/recommended
============================

Sites are recommended to update relevant components as soon as it is 
convenient.

Component installation information
==================================

The official repository for the distribution of grid middleware for 
EGI sites is repository.egi.eu which contains the EGI Unified
Middleware Distribution (UMD).

https://repository.egi.eu/

The fixed version of dCache is not yet in the EGI UMD repository


Sites installing directly from dCache should see [R 1]. 


Affected software details
=========================

This has been resolved in dCache versions 6.2.31, 7.0.20, 7.1.11 and 7.2.1  

Earlier versions may be vulnerable. 

More information
================

This information has been provided by the dCache team:

There is a vulnerability whereby the group flag on ACLs is lost when set 
through dcache admin commands.

dCache supports two ways of setting ACLs - one setting the nfs4_setfacl 
command and the other setting the dCache admin command. 

Though they are very similar, they have a differences.

The admin interface uses the GROUP keyword to associate the Access Control 
Entry (ACE) with a user group, however in this case dCache associates the 
ACE with a user if additional 'g' (subject is a group) flag is not set. 
As a result, a user may get access to restricted resources.


TLP and URL
===========

** WHITE information - Unlimited distribution 
- see  https://confluence.egi.eu/display/EGIG/Traffic+Light+Protocol  
       for distribution restrictions **  

URL:   https://advisories.egi.eu/Advisory-SVG-2021-17357  

Minor updates may be made without re-distribution to the sites.


Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of another vulnerability which is relevant 
to EGI you may report it by e-mail to  

report-vulnerability at egi.eu
 
the EGI Software Vulnerability Group will take a look according to the 
procedure defined in [R 2]. 


References
==========

[R 1] https://www.dcache.org/

[R 2] https://documents.egi.eu/public/ShowDocument?docid=3867

Credit
======

This vulnerability was reported by Tigran Mkrtchyan of the dCache team


Timeline  
========
Yyyy-mm-dd  [EGI-SVG-2021-17357] 

2021-09-22 Vulnerability reported by Tigran Mkrtchyan
2021-09-24 Acknowledgement from the EGI SVG to the reporter 
2021-10-04 EGI SVG Risk Assessment completed
2021-10-05 Assessment by the EGI Software Vulnerability Group reported to 
           the software providers 
2021-10-20 Updated packages available from the dCache site
2021-10-21 Advisory sent to sites
2022-07-11 Advisory placed on advisories.egi.eu

Context
=======

This advisory has been prepared as part of the effort to fulfil EGI SVG's 
purpose   "To minimize the risk to the EGI infrastructure arising from 
software vulnerabilities"

The risk is that assessed by the group, according to the EGI SVG issue 
handling procedure [R 2]  in the context of how the software is used in the
EGI infrastructure. It is the opinion of the group, we do not guarantee it 
to be correct. The risk may also be higher or lower in other deployments 
depending on how the software is used.   

Others may re-use this information provided they:-

1) Respect the provided TLP classification
2) Credit the EGI https://www.egi.eu/ Software Vulnerability Group
