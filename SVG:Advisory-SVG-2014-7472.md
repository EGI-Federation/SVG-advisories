---
title: SVG:Advisory-SVG-2014-7472
permalink: /SVG:Advisory-SVG-2014-7472/
---

    ** WHITE information - unlimited distribution                               **

    ** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **


    EGI SVG   ADVISORY [EGI-SVG-2014-7472]

    Title:       EGI SVG Advisory 'High' RISK - Users have possibility of introducing rogue VMs -
                EGI Federated Cloud sites using Openstack [EGI-SVG-2014-7472]

    Date:        2014-10-28
    Updated:



    URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2014-7472

    Introduction
    ============

    It has been demonstrated that it is possible for an authenticated user to create VM images that appear as the
    trusted VMs in the AppDB for any given VO in some OpenStack sites.

    This is due to a configuration problem, and sites running Openstack are being recommended to ensure they are
    configured correctly so that this cannot occur.


    Details
    =======

    It has been demonstrated that it is possible for an authenticated user to create VM images that appear as the
    trusted VMs in the AppDB for any given VO in OpenStack sites.

    A user with enough privileges to create images at a given site can create an image with the appropriate metadata
    information so it appears as a trusted image to the AppDB without any administrator approval or without any
    real/trusted image being available at the site.  Any malicious VM image could be uploaded with the data instead
    of the trusted ones and obtain valuable and private user information.

    This issue is only exploitable if: user is allowed to create images in OpenStack and the metadata properties
    are not protected (default behaviour).


    Risk category
    =============

    This issue has been assessed as 'High' risk for those sites affected by the EGI SVG Risk Assessment Team.


    Affected software
    =================

    OpenStack.


    Mitigation
    ==========

    Sites using OpenStack in the EGI Federated cloud should prevent setting of metadata using instructions in [R 3]

    Further information on configuring sites is attached.


    Component installation information
    ==================================

    N/A.  This is a configuration issue.


    Recommendations
    ===============

    Initially, sites are recommended to carry out the mitigations above.


    Other information
    =================

    This, of course, does not fully solve the problem. It should not be possible for sites to provide images into the AppDB,
    regardless of site configuration, without the appropriate endorsement.  Ensuring only appropriate endorsed images are
    in the AppDB should not be purely dependent on site configuration.  Further mechanisms will need to be put place to
    ensure that all images in the AppDB can be trusted.


    Credit
    ======

    This vulnerability was reported by Enol Fernandez

    Configuration information provided by Alvaro Garcia.


    References
    ==========


    [R 1] http://docs.openstack.org/havana/config-reference/content/glance-property-protection.html


    Timeline
    ========
    Yyyy-mm-dd

    2014-09-24 Vulnerability reported by Enol Fernandez
    2014-09-24 Acknowledgement from the EGI SVG to the reporter
    2014-10-21 EGI SVG discusses and investigates. (delay due to other critical issues)
    2014-10-22 Assessment by the EGI Software Vulnerability Group
    2014-10-22 Agreed configuration problem, advisory drafted.
    2014-10-27 Configuration information provided by Alvaro Garcia
    2014-10-28 Advisory sent to sites
    2014-11-12 Public disclosure