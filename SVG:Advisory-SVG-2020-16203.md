---
title: SVG:Advisory-SVG-2020-16203
permalink: /SVG:Advisory-SVG-2020-16203/
---

    Title:       EGI SVG 'ADVISORY' [TLP:WHITE] (up to critical) vulnerabilities concerning Squid [EGI-SVG-2020-16203]

    Date:        2020-02-11
    Updated:     2020-04-29

    Affected software and risk
    ==========================

    Various vulnerabilities concerning Squid

    Package : Squid, including Frontier Squid.

    Several vulnerabilities have been found in Squid, including one which may allow remote code execution.
    For more information see the OSG announcement below.

    Actions required/recommended
    ============================

    Sites running Squid or Frontier Squid should update as soon as possible.

    Component installation information
    ==================================

    The official repository for the distribution of grid middleware for EGI sites is
    repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).

    Sites installing Frontier Squid from the EGI UMD 4 repository should see:

    http://repository.egi.eu/category/umd_releases/distribution/umd-4/

    A fixed version of Frontier Squid,  frontier-squid-4.10.1-1 is available in UMD 4.9.2  both for CentOS 7 and SL6.

    http://repository.egi.eu/2020/02/10/release-umd-4-9-2/

    Sites installing Squid from anywhere else should see information from their provider.

    Note: Red Hat have not yet released updated squid packages that deal with these vulnerabilities.


    Affected software details
    =========================

    All versions of Squid prior to 4.10-1.1

    OSG information
    ===============

    Dear OSG Security Contacts,

    Security vulnerabilities have been publicly announced for squid.  OSG has released a version of frontier-squid with fixes for the vulnerabilities.
    All installations of squid should be upgraded.  OSG security considers the vulnerability affecting reverse proxy installations (such as CVMFS Stratum 1 servers)
    to be CRITICAL and the vulnerability affecting ordinary proxy installations to be MODERATE.

    IMPACTED VERSIONS:

    All versions of frontier-squid prior to 4.10-1.1

    WHAT ARE THE VULNERABILITIES:

    The first vulnerability [1] affects reverse proxy configurations, where squid forwards all traffic to a backend server using the http_port 'accel' or 'vhost' options.
    CVMFS Stratum 1 servers are affected.  Due to incorrect input validation, squid can interpret crafted HTTP requests in unexpected ways to access server resources
    prohibited by earlier security filters. Also, due to incorrect buffer management a remote client can cause a buffer overflow in a Squid acting as reverse-proxy.
    This can result in remote code execution.

    The second vulnerability [2] affects squid installations that allow proxying ftp, which is the default. Due to incorrect data management, squid is vulnerable
    to information disclosure when translating FTP server listings into HTTP responses.  The information may be anything from the heap area including information
    from other processes on the machine.  An exploit requires control of the destination server, so those installations that restrict the destination servers to a known
    list of trusted servers should not be affected, but OSG security still advises upgrading.

    WHAT YOU SHOULD DO:

    Upgrade reverse proxy installations to frontier-squid-4.10-1.1 as soon as possible, and schedule an upgrade for other installations.

    REFERENCES

    [1] http://www.squid-cache.org/Advisories/SQUID-2020_1.txt
    [2] http://www.squid-cache.org/Advisories/SQUID-2020_2.txt

    OSG Security Team

    TLP and URL
    ===========

    ** AMBER information - Limited distribution
     - see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

    This advisory will be placed on the wiki on or after 2020-02-25

    URL:   https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2020-16203

    Minor updates may be made without re-distribution to the sites


    Comments
    ========

    Comments or questions should be sent to svg-rat  at  mailman.egi.eu

    If you find or become aware of another vulnerability which is relevant to EGI you may report it by e-mail to

    report-vulnerability at egi.eu

    the EGI Software Vulnerability Group will take a look according to the procedure defined in [R 3]

    Note that this is undergoing revision to fully handle vulnerabilities in the EOSC-hub era.


    References
    ==========

    See references in OSG announcement


    [R 3] https://documents.egi.eu/public/ShowDocument?docid=3145

    Credit
    ======

    SVG was alerted to this vulnerability by Dave Dykstra from the OSG.


    Timeline
    ========
    Yyyy-mm-dd  [EGI-SVG-2020-16203]

    2020-02-03 SVG alerted to this issue by Dave Dykstra from the OSG.
    2020-02-04 Acknowledgement from the EGI SVG to the reporter
    2020-02-07 SVG drafts advisory based on OSG announcement
    2020-02-10 Updated packages available in the EGI UMD
    2020-02-11 Advisory sent to sites
    2020-04-29 Advisory made public and placed on the wiki.


    Context
    =======

    This advisory has been prepared as part of the effort to fulfil EGI SVG's purpose
    "To minimize the risk to the EGI infrastructure arising from software vulnerabilities"

    The risk is that assessed by the group, according to the EGI SVG issue handling procedure [R 3]  in the context of how the software is used in the EGI infrastructure.
    It is the opinion of the group, we do not guarantee it to be correct. The risk may also be higher or lower in other deployments depending on how the software is used.

    -----------------------------
    This advisory is subject to the Creative commons license https://creativecommons.org/licenses/by/4.0/ and the EGI https://www.egi.eu/ Software Vulnerability Group must be credited.
    -----------------------------

    Note that the SVG issue handling procedure is currently under review, to take account of the increasing inhomogeneity of the EGI infrastructure and the services in the EOSC-hub catalogue.

    On behalf of the EGI SVG,