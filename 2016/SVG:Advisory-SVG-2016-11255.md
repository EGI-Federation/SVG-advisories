---
title: SVG:Advisory-SVG-2016-11255
permalink: /SVG:Advisory-SVG-2016-11255/
---

```


Title:       EGI SVG Advisory [TLP:AMBER] Up to 'HIGH' risk DIRAC configuration -
             database passwords visible on Dirac interface [EGI-SVG-2016-11255]

Date:        2016-07-04
Updated:     2016-07-18


Affected software and risk
==========================

Up to 'HIGH' risk - Dirac database passwords visible on Dirac interface

Package :DIRAC

One site has been found where database passwords are visible on the dirac interface.
How widespread this problem is is not known, and how serious the risk is rather depends on
how each dirac site is configured and what users can access.

Actions required/recommended
============================

Sites running DIRAC should check using the Mitigation below whether their sites are vulnerable,
and carry out the actions described below if they are.

Affected software details
=========================

This problem was found for a site running v6r15 with WebApp v1r6p26 already installed.
It's not clear whether any specific versions are free from this problem.

Sites who have installed their software according to [R 1] which was updated 24th June 2016
should avoid this problem.

Mitigation
==========

This was provided by the DIRAC team.

Sites can check by:

- load the Configuration Manager application from the LHCb WebApp Portal
- hit "download" or "view as text" buttons
- grep for "Password"
- if you don't find any, be happy
- if you do, and it contains your DB password, keep reading

If affected sites should Fix by:

- log into your server machine(s)
- define in $DIRACROOT/etc/dirac.cfg the following:
LocalInstallation {
  Database
  {
    #User name used to connect the DB server
    User = thisIsAUser #this is by default "Dirac"
    #Password for database user acess. Must be set for SystemAdministrator Service to work
    Password = thisIsAPassword #the one used for mysql -uDirac -p
    #Password for root DB user. Must be set for SystemAdministrator Service to work
    RootUser = thisIsAAdminUser #either 'root' or 'admin'
    RootPwd = thisIsAAdminPassword
  }
}

- Restart the DIRAC components
- Remove the entry "Password" from the Configuration Manager App


More information
================

Original report:--

----------------

We noticed that our test dirac instance running v6r15 with WebApp
v1r6p26 displays a database password in the webinterface in plain text
to any user that has access to this dirac instance. We currently don't
see this problem on our v6r14 production dirac server which uses the
'old' dirac interface and not the WebApp.

A quick cross check with one of my LHCb colleagues confirms that they
are able to see the database passwords on the LHCb dirac instance's
webinterface without any elevated privileges, just as plain lhcb_user.

-----------------

Note that it is not clear how many sites are affected.

It has been stated by the DIRAC team that sites who install following the instructions
at [R 1] as updated on 24th June 2016 should avoid this problem.

Further investigations are on-going by the DIRAC team, including whether any improvements
are needed to the DIRAC WebApp code so this can't happen again.

----------------

Additional information added on 18th July 2016 provided by Ricardo Graciani:--


- access to the we interface is only provided to authenticated users that have presented
their authorised user certificated to the portal.
- DIRAC does not require users/operators to define DB passwords on the globally shared Configuration,
in fact DIRAC recommends not to do so and use local configuration files in those servers that need this information.

This is, from my point of view, an end-user issue.
If they are OK with using the globally shared configuration in the VO to store passwords, DIRAC can not prevent
them from doing so (in any case it is not publicly accesible). DIRAC does not require to do so.

In fact it allows to public fake information in this same way and then have local real values stored locally
that will be the ones used by the software.



Component installation information
==================================

Documentation on DIRAC installation is available at [R 1] which were updated on 24th June to avoid this problem.

See also [R 2]


TLP and URL
===========

** WHITE information - Unlimited distribution - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions                         **

URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2016-11255

Minor updates may be made without re-distribution to the sites

Credit
======

This vulnerability was reported by Daniela Bauer from Imperial College, London UK.

References
==========

[R 1] http://dirac.readthedocs.io/en/latest/AdministratorGuide/InstallingDIRACService/index.html

[R 2] https://github.com/DIRACGrid/DIRAC/wiki

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2016-11255]

2016-06-16 Vulnerability reported by Daniela Bauer
2016-06-17 Acknowledgement from the EGI SVG to the reporter
2016-06-21 Software providers responded and involved in investigation
2016-06--- Investigation of vulnerability carried out
2016-06-24 DIRAC updated documentation such that sites following new documentation should
           not be vulnerable.
2016-06-28 Instructions received for other sites to check if they are vulnerable
2016-06-29 Risk unclear.
2016-07-04 Advisory/Alert sent to sites suggesting checking their installations
2016-07-18 Public disclosure


On behalf of the EGI SVG,
```