---
title: Speculative Execution Vulnerabilities
permalink: /Speculative_Execution_Vulnerabilities
---

## Speculative Execution Vulnerabilities

This provides information that may be useful to sites concerning the various
speculative execution vulnerabilities concerning Intel chips and other
processors.

See also
[EGI SVG Information on Meltdown and Spectre Vulnerabilities](./Meltdown_and_Spectre_Vulnerabilities.md)
and its related advisory
[Advisory-SVG-CVE-2017-5753](./2017/Advisory-SVG-CVE-2017-5753.md) which was
compiled in January and early February 2018.

EGI SVG has at present (14th September 2018) issued 3 advisories related to
Speculative Execution Vulnerabilities:

- [Advisory-SVG-CVE-2017-5753](./2017/Advisory-SVG-CVE-2017-5753.md) in January
  2018,
- [Advisory-SVG-CVE-2018-3639](../2018/Advisory-SVG-CVE-2018-3639.md) in May
  2018 and
- [Advisory-SVG-CVE-2018-3620](../2018/Advisory-SVG-CVE-2018-3620.md) in
  August 2018.

[Intel information](https://www.intel.com/content/www/us/en/architecture-and-technology/facts-about-side-channel-analysis-and-intel-products.html)
The important thing is that sites carry out recommended updates, including if
appropriate their kernel versions. In some cases this may result in reduced
performance, but the update should not be omitted because of this.

[Wikipedia:
Spectre]<https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))
provides some information on the variants, the recommended changes concern
windows.

| Date         | CVE           | Exploit Name           | Public vulnerability name         | EGI SVG Advisory                                                               | EGI SVG Risk | Comments/Other Links                                                                                                                                                         |
| ------------ | ------------- | ---------------------- | --------------------------------- | ------------------------------------------------------------------------------ | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| January 2018 | CVE-2017-5753 | Spectre(Variant 1)     | Bounds Check Bypass (BCB)         | [Advisory-SVG-CVE-2017-5753](./2017/Advisory-SVG-CVE-2017-5753.md)             | Critical     | [RedHat: Speculative Execution](https://access.redhat.com/security/vulnerabilities/speculativeexecution)                                                                     |
| January 2018 | CVE-2017-5715 | Spectre(Variant 2)     | Branch Target Injection (BTI)     | [Advisory-SVG-CVE-2017-5753](./2017/Advisory-SVG-CVE-2017-5753.md)             | Critical     | see link for CVE-2017-3753                                                                                                                                                   |
| January 2018 | CVE-2017-5754 | Meltdown (Variant 3)   | Rogue Data Cache Load (RDCL)      | [Advisory-SVG-CVE-2017-5753](./2017/Advisory-SVG-CVE-2017-5753.md)             | Critical     | see link for CVE-2017-3753                                                                                                                                                   |
| May 2018     | CVE-2018-3640 | SpectreNG(Variant 3a)  | Rogue System Register Read (RSRE) | [Advisory-SVG-CVE-2018-3639](../2018/Advisory-SVG-CVE-2018-3639.md)            | High         | [TA18-141A](https://www.us-cert.gov/ncas/alerts/TA18-141A)                                                                                                                   |
| May 2018     | CVE-2018-3639 | SpectreNG(Variant 4)   | Speculative Store Bypass (SSB)    | [Advisory-SVG-CVE-2018-3639](../2018/Advisory-SVG-CVE-2018-3639.md)            | High         | [RedHat: SSBD](https://access.redhat.com/security/vulnerabilities/ssbd)                                                                                                      |
| June 2018    | CVE-2018-3665 |                        | Lazy FP state restore             | None                                                                           | Moderate     | [INTEL SA 00145](https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-00145.html) [CVE-2018-3665](https://access.redhat.com/security/cve/cve-2018-3665) |
| July 2018    | CVE-2018-3693 | SpectreNG(Variant 1.1) | Bounds Check Bypass Store (BCBS)  | Covered by [Advisory-SVG-CVE-2018-3620](../2018/Advisory-SVG-CVE-2018-3620.md) | None         |                                                                                                                                                                              |
| August 2018  | CVE-2018-3620 | L1TF                   | OS, SMM related aspects           | [Advisory-SVG-CVE-2018-3620][../2018/advisory-svg-cve-2018-3620.md]            | High         | [Kernerl.org: L1TF](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/l1tf.html) [RedHat: L1TF](https://access.redhat.com/security/vulnerabilities/L1TF)            |
| August 2018  | CVE-2018-3646 | L1TF                   | Virtualization related aspects    | [Advisory-SVG-CVE-2018-3620](../2018/Advisory-SVG-CVE-2018-3620.md)            | High         | see links for CVE-2018-3620                                                                                                                                                  |
| August 2018  | CVE-2018-3615 | L1TF                   | SGX related aspects               | [Advisory-SVG-CVE-2018-3620](../2018/Advisory-SVG-CVE-2018-3620.md)            |              | see links for CVE-2018-3620. RHEL 7 is not vulnerable but other Linux distributions, such as Debian, are.                                                                    |
