---
title: SVG:Advisory-SVG-2013-5244
permalink: /SVG:Advisory-SVG-2013-5244/
---

```

** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions  **

EGI CSIRT ADVISORY [EGI-ADV-20130322]
EGI SVG   ADVISORY [EGI-SVG-2013-5244]

Title:       CREAM Axis2 configuration file permissions [EGI-ADV-20130322]

Date:        2013-03-22
Updated:     2013-04-09

URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2013-5244

Introduction
============

The default installation of glite-ce-yaim-cream-ce creates a configuration file which contains
Axis2 administration credentials. This file is created with insecure permissions.

This advisory is updated as the software has been fixed in both the EMI 2 distrubution
and the EGI UMD 2.

Details
=======

The file $CATALINA_HOME/webapps/ce-cream/WEB-INF/conf/axis2.xml contains userName and password
 parameters. The password is randomly generated when the CREAM RPM is installed. By default the
axis2.xml configuration file is world readable. An authenticated user could access this file
and subsequently use these credentials to administer the Axis service. Existing components could
be disabled or new components uploaded.

(Updated on 8th April 2013)

Updated RPMS are now available.

We strongly recommend sites update with the new version, especially if they have not already
carried out the mitigation action below.

This advisory continues to be distributed under the AMBER TLP restriction, and will be made
public in 2 weeks.


Risk Category
=============

This issue has been assessed as 'HIGH' risk by the EGI CSIRT and EGI SVG.


Affected Software
=================

This has been confirmed in the version of CREAM which ships with UMD/EMI2.

This is fixed in the following files:

CREAM 1.14.4, CEMon 1.14.1
glite-ce-common-java-1.14.2-1.sl*.noarch.rpm
glite-ce-cream-1.14.4-1.sl*.noarch.rpm
glite-ce-cream-es-1.14.4-1.sl*.noarch.rpm
glite-ce-monitor-1.14.1-1.sl*.noarch.rpm

This is fixed in EMI 2 Update 10 and UMD release 2.4.1


Mitigation
==========

The group ownership and permissions on this file should be changed to prevent
authenticated users gaining access to this file.

On SL5

chgrp tomcat /var/lib/tomcat5/webapps/ce-cream/WEB-INF/conf/axis2.xml
chmod 640 /var/lib/tomcat5/webapps/ce-cream/WEB-INF/conf/axis2.xml

On SL6

chgrp tomcat /var/lib/tomcat6/webapps/ce-cream/WEB-INF/conf/axis2.xml
chmod 640 /var/lib/tomcat6/webapps/ce-cream/WEB-INF/conf/axis2.xml

We also recommend you change your Axis2 password in the event it has already been
compromised.

Generate a new password using "openssl rand -base64 15" and modify the password parameter
in axis2.xml accordingly.


This issue also affects glite-ce-cream-es and glite-ce-monitor. Similar mitigations should
be performed on these files, if applicable.
The axis2.xml files are located at
$CATALINA_HOME/webapps/ce-cream-es/WEB-INF/conf/axis2.xml
and
$CATALINA_HOME/webapps/ce-monitor/WEB-INF/conf/axis2.xml


Component installation information
==================================

Updates are now available.

The official repository for the distribution of grid middleware for EGI sites is
repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).

Sites using the EGI UMD should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-2/

For information on this release see:

http://repository.egi.eu/2013/04/05/release-umd-2-4-1/

Sites installing directly from EMI should see:

http://www.eu-emi.eu/emi-2-matterhorn/updates/


Recommendations
===============

Sites are recommended to update to the latest version, urgently if they have not
already carried out the mitigation action above.


Credit
======

This vulnerability was reported by Simon Fayer from Imperial College, London


Timeline
=======
Yyyy-mm-dd

2013-03-19 Vulnerability reported by Simon Fayer
2013-03-19 Acknowledgement from the EGI SVG to the reporter
2013-03-20 Software providers responded and involved in investigation
2013-03-22 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2013-03-22 Mitigating action recommended to sites and sent as 'Amber'
2013-04-05 Updated packages available in the EGI UMD
2013-04-09 Updated advisory issued
2013-04-29 Public disclosure
```