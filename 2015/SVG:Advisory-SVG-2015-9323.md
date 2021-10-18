---
title: SVG:Advisory-SVG-2015-9323
permalink: /SVG:Advisory-SVG-2015-9323/
---

    Title:       **UPDATE - re-introduction** EGI SVG Advisory [TLP:WHITE] "Moderate" RISK - dCache  [EGI-SVG-2015-9323]

    Date:        2015-08-24
    Updated:     2015-09-10, 2017-08-22

    Affected software and risk
    ==========================

    MODERATE risk vulnerability concerning dCache

    Package :dCache

    The dCache team has reported that an old vulnerbility from 2015 concerning the "gridftp
    door", and in the "kerberos ftp door" of dCache has been re-introduced.
    No other component is affected.


    Actions required/recommended
    ============================

    Sites running dCache should check whether they are running a vulnerable version, see
    "Affected software details" below. If they are running a vulnerable version update in due course.

    Sites running dCache may update nodes hosting either a gridftp door or kerberos-ftp door directly
    from the dCache site if they wish.

    **UPDATE 2017-08-11** fixed version is in the UMD 4


    More information
    =================

    A vulnerability has been found in the "gridftp door", and in the "kerberos ftp door"
    of dCache. No other component is affected.

    Fixed versions are available on the dCache site. [R 1]

    Upgrading all dCache nodes that host either a gridftp or kerberos-ftp door is necessary
    and sufficient to fix the vulnerability.


    Affected software details
    =========================

    FIXED versions of dCache:

       3.0.11 (& later)  note version 3.0.25 is now in UMD-4
       2.16.30 (& later)
       2.15.33 (& later)
       2.14.45 (& later)

    VULNERABLE versions of dCache:

       3.0.0 .. 3.0.10
       2.16.0 .. 2.16.29
       2.15.0 .. 2.15.32
       2.14.0 .. 2.14.44


    Mitigation
    ==========

    N/A


    Component installation information
    ==================================

    The official repository for the distribution of grid middleware for EGI sites is
    repository.egi.eu which contains the EGI Unified Middleware Distribution (UMD).


    Sites using the EGI UMD 4 should see:

    http://repository.egi.eu/category/umd_releases/distribution/umd-4/

    This update is in EGI UMD 4.5.0


    Updates are also available on the dCache site [R 1]

    Please note the EMI repositories are no longer maintained and may no longer be used.

    Credit
    ======

    This vulnerability was reported by Paul Millar of the dCache team.

    TLP and URL
    ===========

    ** WHITE information - Unlimited distribution                               **

    ** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

    URL:         https://wiki.egi.eu/wiki/SVG:Advisory-SVG-2015-9323



    Comments
    ========

    Comments or questions should be sent to svg-rat  at  mailman.egi.eu

    If you find or become aware of another vulnerability which is relevant to EGI you may

    report it by e-mail to

    report-vulnerability at egi.eu

    the EGI Software Vulnerability Group will take a look according to the procedure defined in [R 2]


    References
    ==========

    [R 1] https://www.dcache.org/

    [R 2] https://documents.egi.eu/public/ShowDocument?docid=2538



    Timeline
    ========
    Yyyy-mm-dd

    2015-08-18 Vulnerability reported by Paul Millar of the dCache team,
               stating they had found and fixed vulnerability but not released the patch
    2015-08-18 Acknowledgement from the EGI SVG to the reporter
    2015-08-20 Assessment by the EGI Software Vulnerability Group reported to the software providers
    2015-08-24 Updated packages available from dCache site - binary release only
    2015-08-24 Advisory sent to sites
    2015-09-10 Update available in UMD
    2015-09-10 Advisory updated.
    2017-03-17 Paul Millar from the dCache team informed SVG that vulnerability has
               been re-introduced and fixed
    2017-03-20 dCache team informed some sites using dCache
    2017-08-10 Updated package in UMD.
    2017-08-22 Advisory updated, sent to sites, and placed on the wiki



    On behalf of the EGI SVG,