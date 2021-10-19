---
title: SVG:Advisory-SVG-2015-9065
---

```
** WHITE information - Unlimited distribution allowed                       **
** see https://wiki.egi.eu/wiki/EGI_CSIRT:TLP for distribution restrictions **

Title:   EGI SVG/CSIRT **Update** OpenSSL release on 9th July - CVE-2015-1793

Date:    2015-07-07
Updated: 2015-07-13


On 7th July we alerted sites to the announcement by OpenSSL [R 1]

OpenSSL has released the advisory concerning 'Alternative chains certificate
forgery (CVE-2015-1793)'  [R 2]

Most Linux releases (with some exceptions) do NOT contain a version of OpenSSL
containing this vulnerability.  It is probably not exploitable in EGI as it is
unlikely that any vulnerable versions of OpenSSL are installed but sites should
read through below and check.



RedHat and derivatives
----------------------------

Not vulnerable [R 3]

Debian
---------

Stable and oldstable releases are not vulnerable, only testing and unstable
releases are vulnerable  [R 4]

Ubuntu
------

1 version vulnerable and fixed [R 5]

Fedora
-------

Fedora 21 and 22 ARE affected [R 6], [R 7], [R 8]



Recommendations
===============

For most sites there is no need to take any specific action due to this
vulnerability.

Sites which install OpenSSL directly from the OpenSSL site or use vulnerable
versions of linux should update.

Sites should, of course, keep their systems up to date.


References
=========

[R 1] https://mta.openssl.org/pipermail/openssl-announce/2015-July/000037.html

[R 2] https://www.openssl.org/news/secadv_20150709.txt

[R 3] https://access.redhat.com/solutions/1523323

[R 4] https://security-tracker.debian.org/tracker/CVE-2015-1793

[R 5] http://people.canonical.com/~ubuntu-security/cve/2015/CVE-2015-1793.html

[R 6] https://bugzilla.redhat.com/show_bug.cgi?id=1238619:

[R 7] http://pkgs.fedoraproject.org/cgit/openssl.git/commit/?id=fc6854bd38f0a020118914e09bb7ef00964a9435

[R 8] https://bugzilla.redhat.com/show_bug.cgi?id=1166614

[R 9] National Vulnerability Database info https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2015-1793
```
