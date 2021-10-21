---
title: Meltdown and Spectre Vulnerabilities
---

## Purpose of this page

To provide more detailed information about the Meltdown and Spectre
vulnerabilities, to complement the advisory,
[SVG:Advisory-SVG-CVE-2017-5753](./2017/Advisory-SVG-CVE-2017-5753.md).

This was compiled in January and early February 2018

Information including more recent
[SVG Speculative execution vulnerabilities](./Speculative_Execution_Vulnerabilities.md)

## What are they?

These are vulnerabilities in the design of the chip hardware, and cannot be
fully resolved by patching operating systems. However patches are available
which mitigate these problems.

- Meltdown (CVE-2017-5754) affects most Intel chips.
- Spectre (CVE-2017-5753 and CVE-2017-5715) affects a wide range of chips.

For more details, see [Meltdown attack](https://meltdownattack.com/),
[Spectre attack](https://spectreattack.com/) and
[Project zero: Reading privileged memory with side](https://googleprojectzero.blogspot.dk/2018/01/reading-privileged-memory-with-side.html)

## How to mitigate these vulnerabilities

Each CVE can be mitigated via different ways:

- Meltdown (CVE-2017-5754) can be mitigated via
  [Kernel Page Table Isolation](https://en.wikipedia.org/wiki/Kernel_page-table_isolation),
  which is enabled by default in latest linux kernels
- Spectre Variant 1 (CVE-2017-5753) has to be mitigated in each software which
  can be vulnerable. The latest linux kernel contains fixes to protect itself
  (does not protect other software).
- Spectre Variant 2 (CVE-2017-5715) can be (at least partially) mitigated via at
  least two different approach:
  - Using new Intel-specific MSR, added via a microcode update, to control
    indirect branch restricted speculation (IBRS): Both a kernel and a microcode
    update are required. In addition, in case of virtualization, an update of
    the virtualization software (e.g. qemu & virt) is required to expose the new
    MSR to the VM.
  - Using "retpoline", a new software construct that can mitigate, on most CPUs,
    the vulnerability

### RedHat

As of Feb 2nd 2018, RedHat has
[offered new kernel updates that can mitigate Meltdown (CVE-2017-5754), Spectre Variant 1 (CVE-2017-5753) and Spectre Variant 2 (CVE-2017-5715)](https://access.redhat.com/security/vulnerabilities/speculativeexecution).

However, due to instability issues, it has
[removed the microcode updates required for Spectre Variant 2 (CVE-2017-5715)](https://access.redhat.com/errata/RHSA-2018:0093).
Until Intel releases stable microcode or RedHat switches to 'retpoline', no
mitigation for Spectre Variant 2 (CVE-2017-5715) is safely usable.

It is currently possible to mitigate Meltdown (CVE-2017-5754) and Spectre
Variant 1 (CVE-2017-5753) by:

- On RHEL7: Updating the kernel to 3.10.0-693.11.6.el7, see
  [RHSA-2018:0007](https://access.redhat.com/errata/RHSA-2018:0007)
- On RHEL6: Updating the kernel to 2.6.32-696.18.7.el6, see
  [RHSA-2018:0008](https://access.redhat.com/errata/RHSA-2018:0008)

### Centos

Centos is following RedHat (see above).

It is currently possible to mitigate Meltdown (CVE-2017-5754) and Spectre
Variant 1 (CVE-2017-5753) by:

- On Centos 7: Updating the kernel to 3.10.0-693.11.6.el7, see
  [CESA-2018:0007](https://lists.centos.org/pipermail/centos-announce/2018-January/022696.html)
- On Centos 6: Updating the kernel to 2.6.32-696.18.7.el6, see
  [CESA-2018:0008](https://lists.centos.org/pipermail/centos-announce/2018-January/022701.html)

### Scientific Linux

Scientific Linux is following RedHat (see above).

It is currently possible to mitigate Meltdown (CVE-2017-5754) and Spectre
Variant 1 (CVE-2017-5753) by:

- On SL7: Updating the kernel to 3.10.0-693.11.6.el7, see
  [SLSA-2018:0007-1](https://www.scientificlinux.org/category/sl-errata/slsa-20180007-1/)
- On SL6: Updating the kernel to 2.6.32-696.18.7.el6, see
  [SLSA-2018:0008-1](https://www.scientificlinux.org/category/sl-errata/slsa-20180008-1/)

Additional details as well as information on other systems and platforms can be
found in the next section.

## More Information

### Relevant Advisories

#### CERN

CERN has compiled information which is useful for many EGI sites:

- [CERN: spectre - meltdown](https://security.web.cern.ch/security/advisories/spectre-meltdown/spectre-meltdown.shtml)

#### Intel

Intel has initially, on January 8th,
[released new microcodes](https://downloadcenter.intel.com/download/27431/Linux-Processor-Microcode-Data-File)
to complement the IBRS kernel patchset. However, these new microcodes are in
fact **unstable** and Intel has since then recommended to stop deploying them.

Intel latest recommendation can be found in their advisory,
[INTEL-SA-00088](https://security-center.intel.com/advisory.aspx?intelid=INTEL-SA-00088&languageid=en-fr)

More updates and information:

- [Jan 3rd: Initial response](https://newsroom.intel.com/news/intel-responds-to-security-research-findings/)
- [Jan 4th](https://newsroom.intel.com/news-releases/intel-issues-updates-protect-systems-security-exploits/)
- [Jan 9th: Microcode released](https://newsroom.intel.com/news/intel-offers-security-issue-update/)
- [Jan 10th: performance impact analysis](https://newsroom.intel.com/editorials/intel-security-issue-update-initial-performance-data-results-client-systems/)
- [Jan 11th: Microcode unstability reported](https://newsroom.intel.com/news/intel-security-issue-update-addressing-reboot-issues/)
- [Jan 17th](https://newsroom.intel.com/news/firmware-updates-and-initial-performance-data-for-data-center-systems/)
- [Jan 22th: Instabilities causes found for 2 Intel series](https://newsroom.intel.com/news/root-cause-of-reboot-issue-identified-updated-guidance-for-customers-and-partners/)

### Linux Distributions

#### RedHat

**Important! [as of 17th January]**

RedHat has issued new microcode_ctl packages to rollback the latest updates, see
[RHSA-2018:0093](https://access.redhat.com/errata/RHSA-2018:0093).

RedHat description:

- [RedHat: speculative execution](https://access.redhat.com/security/vulnerabilities/speculativeexecution)
- [RedHat: 3307751](https://access.redhat.com/articles/3307751)

RedHat CVE info:

- [CVE-2017-5754](https://access.redhat.com/security/cve/CVE-2017-5754)
- [CVE-2017-5753](https://access.redhat.com/security/cve/CVE-2017-5753)
- [CVE-2017-5715](https://access.redhat.com/security/cve/CVE-2017-5715)

#### CentOS

**Important! [as of 17th January]**

Centos seems to be following Redhat in the revert of the microcode_ctl package,
see
[the disclaimer in the sources of the last package](https://git.centos.org/rpms/microcode_ctl/blob/c7/f/SOURCES/06-2d-07_disclaimer)

CentOS 7:

- kernel Security Update:
  [CESA-2018:0007](https://lists.centos.org/pipermail/centos-announce/2018-January/022696.html)
- microcode_ctl Security Update:
  [CESA-2018:0012](https://lists.centos.org/pipermail/centos-announce/2018-January/022697.html)
  also needs dracut BugFix Update for AMD:
  [CEBA-2018:0042](https://lists.centos.org/pipermail/centos-announce/2018-January/022708.html)
- linux-firmware Security Update:
  [CESA-2018:0014](https://lists.centos.org/pipermail/centos-announce/2018-January/022698.html)
- qemu-kvm Security Update:
  [CESA-2018:0023](https://lists.centos.org/pipermail/centos-announce/2018-January/022705.html)
- libvirt Security Update:
  [CESA-2018:0029](https://lists.centos.org/pipermail/centos-announce/2018-January/022704.html)

CentOS 6:

- kernel Security Update:
  [CESA-2018:0008](https://lists.centos.org/pipermail/centos-announce/2018-January/022701.html)
- microcode_ctl Security Update:
  [CESA-2018:0013](https://lists.centos.org/pipermail/centos-announce/2018-January/022700.html)
- qemu-kvm Security Update:
  [CESA-2018:0024](https://lists.centos.org/pipermail/centos-announce/2018-January/022702.html)
- libvirt Security Update:
  [CESA-2018:0030](https://lists.centos.org/pipermail/centos-announce/2018-January/022703.html)

See further in the centos-announce
[Security mails for January](https://lists.centos.org/pipermail/centos-announce/2018-January/date.html)

#### Scientific Linux

**Important! [as of 18th January]**

Scientific Linux is following RedHat in the revert of the microcode_ctl package,
see
[SLSA 2018:0093-1](https://www.scientificlinux.org/category/sl-errata/slsa-20180093-1/)

- SL6:
  [SLSA 2018:0008-1](https://www.scientificlinux.org/category/sl-errata/slsa-20180008-1/)
- SL7:
  [SLASA 2018:0007-1](https://www.scientificlinux.org/category/sl-errata/slsa-20180007-1/)

- SL6:
  - qemu-kvm:
    [SLSA 2018:0024-1](http://scientificlinux.org/category/sl-errata/slsa-20180024-1/)
  - libvirt:
    [SLSA 2018:0030-1](http://scientificlinux.org/category/sl-errata/slsa-20180030-1/)
- SL7:
  - qemu-kvm:
    [SLSA 2018:0023-1](http://scientificlinux.org/category/sl-errata/slsa-20180023-1/)
  - libvirt:
    [SLSA 2018:0029-1](http://scientificlinux.org/category/sl-errata/slsa-20180029-1/)

#### Ubuntu

[Ubuntu: Spectre and Meltdown](https://wiki.ubuntu.com/SecurityTeam/KnowledgeBase/SpectreAndMeltdown)

#### Debian

- [CVE-2017-5715](https://security-tracker.debian.org/tracker/CVE-2017-5715)
- [CVE-2017-5753](https://security-tracker.debian.org/tracker/CVE-2017-5753)
- [CVE-2017-5754](https://security-tracker.debian.org/tracker/CVE-2017-5754)

### System Vendors

#### Supermicro

[Supermicro: SA 00088](https://www.supermicro.com/support/security_Intel-SA-00088.cfm)

#### Dell

**Important! [as of 23rd January]**

Dell is advising that all customers and partners should not deploy the BIOS
update for the Spectre vulnerability at this time due to Intel’s advisory
acknowledging reboot issues and unpredictable system behaviour.

[DELL: support for meltdown and spectre](http://www.dell.com/support/contents/uk/en/ukbsdt1/article/product-support/self-support-knowledgebase/software-and-downloads/support-for-meltdown-and-spectre)

[DELL: side channel vulnerabilities](https://www.dell.com/support/kbdoc/en-us/000178106/microprocessor-side-channel-vulnerabilities-cve-2017-5715-cve-2017-5753-cve-2017-5754-impact-on-dell-emc-servers-storage-and-networking)

Note this is changing rather frequently

#### HPE

[as of January 23]

HPE has updated their advisory to note that "Marked impacted products with TBD
for System ROM updates per Intel's guidance on microcode issues" - so following
suit with DELL.

[HPE: hpesbhf03805en_us](https://support.hpe.com/hpesc/public/docDisplay?docLocale=en_US&docId=emr_na-hpesbhf03805en_us)

#### Lenovo

[as of January 23]

Lenovo security advisory

### Hypervisors

[Lenovn: LEN 18282](https://support.lenovo.com/gb/en/solutions/len-18282)

#### Xen

- [XEN: advisory 254](https://xenbits.xen.org/xsa/advisory-254.html)
- [XEN: Spectre meltdown FAQ](https://blog.xenproject.org/2018/01/04/xen-project-spectremeltdown-faq/)
- [XEN: Meltdown and Spectre technical FAQ](https://wiki.xenproject.org/wiki/Xen_Project_Meltdown_and_Spectre_Technical_FAQ)
- [XEN: Respond to Meltdown and Spectre](https://wiki.xenproject.org/wiki/Respond_to_Meltdown_and_Spectre)

#### QEMU-KVM

In order to protect hypervisors from malicious VMs, the kernel, microcode and
QEMU must be updated:

[QEMU: spectre](https://www.qemu.org/2018/01/04/spectre/)
