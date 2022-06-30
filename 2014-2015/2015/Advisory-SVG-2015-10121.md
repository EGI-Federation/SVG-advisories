---
title: Advisory-SVG-2015-10121
permalink: /Advisory-SVG-2015-10121
---

## Advisory-SVG-2015-10121

```
Title:   EGI SVG Advisory [TLP:White] 'Low' risk dCache WebDAV interface XXE
         vulnerability [EGI-SVG-2015-10121]

Date:    2016-06-20
Updated:

Affected Software and Risk
==========================

LOW risk XXE vulnerability concerning dCache WebDAV interface

Package : dCache

Actions Required/Recommended
============================

Sites are recommended to update relevant components in due course.

Affected software Details.
==========================

dCache versions affected:
 2.10.45 or earlier,
 2.11.36 or earlier,
 2.12.25 or earlier,
 2.13.13 or earlier,
 2.14.1 or earlier.

dCache versions not affected:
 2.10.46 or later,
 2.11.37 or later,
 2.12.26 or later,
 2.13.14 or later,
 2.14.2 or later,
 2.15.0 or later


More information
================

WebDAV is a protocol, based on HTTP, that makes use of XML as a
machine-readable format.  The XML External Entity (XXE) processing feature of
XML make services that use it, like WebDAV, potentially vulnerable to attacks.

An XXE problem was identified with the Milton library. dCache uses this library
to process WebDAV requests.

More information on the XML External Entity Vulnerability is available at [R 1]

Details from the dCache team:--

We've been notified of a vulnerability in dCache WebDAV interface.

Background:

WebDAV is a protocol, based on HTTP, that makes use of XML as a
machine-readable format. The XML External Entity (XXE) processing
feature of XML make services that use it, like WebDAV, potentially
vulnerable to attacks.

The problem:

An XXE problem was identified with the Milton library. dCache uses this
library to process WebDAV requests.

The following has been announced to the milton library users mailing list:

 Milton Security Vulnerability Notice

 A security vulnerability has been discovered in Milton and a
 fixed update is available.

 This email is being sent from milton.io to customers who
 have registered or previously submitted a contact request
 through the milton website. If you're not the technical
 contact please pass this message on as appropriate.

 Details of the security vulnerability

 The XML parser used in within the Milton framework allows
 general entities to be parsed, which allows remote files
 to be loaded. This means that XML requests such as PROPFIND
 and REPORT can include DOCTYPE delcarations which
 reference external entities and the parse will attempt to
 retrieve them.

 This was previously patched for external entities, but this
 new vulnerability has been discovered which affected
 general entities

 https://www.owasp.org/index.php/XML_External_Entity_(XXE)_Processing


http://www.brainbell.com/tutors/XML/XML_Book_B/External_Parsed_General_Entities.htm

 This leads to the following issues:

 Port scan

 XML DOCTYPE definitions and entities (external / parameter) may
 be abused to scan the internal network where the
 vulnerable application is located. An attacker may supply
 a protocol, an IP address followed by the port to scan. E.g.:
 http://10.11.12.13 [lookup IP][Add IP]:1204

 While creating a DOM the vulnerable parser will resolve the
 given URL. Depending on the response times and behaviour of
 the application using Milton it might be guessed which ports
 on the specified host are open. This may as well be abused to
 determine, which ports aren’t blocked by the outgoing
 firewall.

 Server Side Request Forgery

 XML DOCTYPE definitions and entities (external / parameter) may
 be abused to trigger requests on other systems, which may not
 be directly reachable by the attacker but are reachable by
 the vulnerable application. This means that an adversary
 might attack internal systems where no access would have
 been possible without the SSRF vulnerability.

 XML External Entity Attacks

 XML External Entities allow the XML Parser to include
 external resources. These resources may reside
 on the local system or the network.

 Resolution

 Milton 2.7.0.3 [lookup IP][Add IP] has been release hardens the configuration
 of the parsers so they will not attempt to retrieve remote resources. You
 should apply this release to your affected systems as soon as possible.


The next cycle of dCache releases will update the milton library to the
recommended version. We can do this "silently" to allow us to prepare a
reasonable advisory.

Here is our assessment of the vulnerabilities:

Both the port scan and the "XML External Entity (XXE)" attacks requires
the server to "echo" part of the request in the response. The current
mechanisms to achieve this is via user-controlled properties (i.e.,
arbitrary metadata), which dCache does not support. Unless some other
mechanism is found, dCache is NOT vulnerable to port-scan or XXE attacks.

The "Server Side Request Forgery" attack is possible, but the response
will not be accessible to the attacker. This could be used to attempt a
Denial-of-Service attack on services accessible from dCache WebDAV door
or trigger some activity, but cannot be used to obtain protected
information.

Mitigation
==========

N/A

Component installation information
==================================

The official repository for the distribution of grid middleware for EGI sites
is repository.egi.eu which contains the EGI Unified Middleware Distribution
(UMD).


Sites using the EGI UMD 4 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-4/

dCache version 2.13.28 is available in UMD-4.1.0

http://repository.egi.eu/2016/05/27/release-umd-4-1-0/

Sites using the EGI UMD 3 should see:

http://repository.egi.eu/category/umd_releases/distribution/umd-3/

dCache version 2.10.56 is available in UMD-3.14.2


Sites who wish to install directly from the dCache site, which includes all
patched versions  should see:

https://www.dcache.org/downloads/IAgree.shtml


TLP and URL
===========

** WHITE information - Unlimited distribution  **

** see https://go.egi.eu/tlp for distribution restrictions**

URL:   https://advisories.egi.eu/2015/Advisory-SVG-2015-10121

Minor updates may be made without re-distribution to the sites

Credit
======

This vulnerability was reported by Paul Miller from dCache

References
==========

[R 1] https://www.owasp.org/index.php/XML_External_Entity_(XXE)_Processing

Comments
========

Comments or questions should be sent to svg-rat  at  mailman.egi.eu

If you find or become aware of a vulnerability which is relevant to EGI you may
report it by e-mail to

report-vulnerability at egi.eu

the EGI Software Vulnerability Group will take a look.


Timeline
========
Yyyy-mm-dd  [EGI-SVG-2015-10121]

2015-12-01 Vulnerability reported by Paul Miller
2015-12-01 Acknowledgement from the EGI SVG to the reporter
2015-12-10 EGI SVG Risk Assessment completed
2015-12-10 Assessment by the EGI Software Vulnerability Group reported to the
           software providers
2016-06-08 Updated packages available at dCache sites and in UMD 4
2016-06-16 Updated packages available in UMD 3
2016-06-20 Advisory/Alert sent to sites
2016-06-20 Public disclosure


On behalf of the EGI SVG,
```
