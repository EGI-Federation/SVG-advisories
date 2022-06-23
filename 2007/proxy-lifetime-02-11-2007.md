---
title: EGI CSIRT Operation Notice proxy-lifetime-02-11-2007
permalink: /CSIRT_Op-notices/proxy-lifetime-02-11-2007
---

```
------------------------------------------------------------------------
          EGEE Operational Security Coordination Team operational notice

Proxy lifetime limits

Date:    November 2nd 2007
ID:      1
URL:     http://cern.ch/osct/op-notices/proxy-lifetime-02-11-2007.txt
------------------------------------------------------------------------

The short-lived credential is a key component of our security
infrastructure to enable security teams and the VOs to quickly
control the access of any malicious user to our infrastructure.

The standard gLite renewal mechanism can be used to support
long-term operations that need valid credentials throughout its
duration, and whose duration could exceed the maximum lifetime
agreed.  The proxy renewal functionality is available in the
glite WMS and FTS services.

In June 2006, during the JSPG meeting, it was agreed to limit the
proxy lifetime to 24 hours for all VOs, both at the authentication
and at the authorization level. The verbatim text from JSPG is
available at the end of this notice.

If a VO needs to TEMPORARY extend the proxy lifetime of its users,
the relevant VO manager(s) MUST send a documented request to the
OSCT (project-egee-security-support@cern.ch), including:

  - A detailed explanation of the technical difficulties that would
    justify a temporary extension of the proxy lifetime

  - A confirmation of the understanding and agreement from the VO
    that this temporary extension will be revoked after an agreed
    deadline

Once the request is approved by the OSCT, the VO manager(s) or the
OSCT MUST inform all sites about the change by sending an EGEE
broadcast to all the site administrators and managers and to the
LCG/EGEE security contacts.

-- JSPG decision on the proxy lifetimes

The text is cited by the minutes of the JSPG meeting held at
CERN at 22nd and 23rd June 2006 [1].

Abbreviations: AuthN = authentication, AuthZ = authorization.

Words SHOULD and MUST are to be interpreted as per RFC 2119 [2].

"Regarding the period of validity of AuthZ attributes in a VOMS
proxy certificate.  JSPG agrees that the maximum lifetime should
be 24 hours (from time of issue).  VO's SHOULD not issue AuthZ
attributes with lifetimes longer than this or MUST request approval
(from OSCT) if this needs to be exceeded.  OSCT needs to notify
sites if longer lifetimes are being used -- some may refuse to allow
this.

Regarding the period of validity of AuthN attributes in a Grid proxy
certificate.  JSPG agrees that the maximum lifetime should be 24
hours (from time of issues).  Users (or MyProxy) SHOULD not create
Grid proxy certificates with lifetimes longer than this except when
storing proxies in approved services like MyProxy.

JSPG agrees that sites SHOULD enforce these policy upper limits.
Grid middleware MUST provide the ability to do this."

-- References

1. JSPG meeting details,
   http://indico.cern.ch/conferenceDisplay.py?confId=a061803
   Meeting minutes,
   http://indico.cern.ch/getFile.py/access?resId=0&materialId=0&confId=a061803

2. RFC 2119, http://www.ietf.org/rfc/rfc2119.txt
```
