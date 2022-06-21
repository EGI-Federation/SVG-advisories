---
title: Advisory-SVG-2017-6074
---

```
Title: [HEADS-UP] Linux kernel root escalation vulnerability
       [EGI-SVG-2017-6074]

Date:  2017-02-23

TLP and URL
===========

WHITE information - Unlimited distribution
see https://go.egi.eu/tlp for distribution restrictions

URL:   https://advisories.egi.eu/2017/Advisory-SVG-2017-6074

Minor updates may be made without re-distribution to the sites

Affected software and risk
==========================

Root escalation vulnerability affecting the Linux kernel

Package : kernel
CVE ID  : CVE-2017-6074

A double-free vulnerability has been found in the linux kernel module 'dccp',
which might allow unprivileged local users to escalate their privileges.
This vulnerability is present in all recent versions of the linux kernel.

The most affected services are those that give shell access to unprivileged
users:

- Worker Nodes
- shared User Interface hosts
- ...

Actions required/recommended
============================

The publishing of an exploit is expected to make this a CRITICAL vulnerability.

Sites are therefore advised to deploy the proposed mitigation now and to
plan for a kernel update campaign (including reboot) within the time lines
stated in:

    https://go.egi.eu/sec03

Mitigation
==========

This vulnerability can be mitigated by disabling DCCP completely. On standard
distributions, where it's present as a kernel module, this can be achieved by
either:
- Adding a modprobe configuration file to disable dccp by running:

    ```
    echo "install dccp /bin/true" >> /etc/modprobe.d/CVE-2017-6074.conf
    ```

- Removing all DCCP kernel modules from /lib/modules

If the DCCP kernel module is already loaded (lsmod | grep dccp), a reboot
might be needed to unload the module (rmmod will fail if still in use). Please
note however that most systems don't load this module and a loaded module
should be investigated as it could be from an exploitation attempt.

For other systems, where DCCP is statically compiled in the kernel (use grep
CONFIG_IP_DCCP /boot/config-$(uname -r) or zgrep CONFIG_IP_DCCP
/proc/config.gz. 'm' means module, 'y' means compiled in the kernel directly),
these mitigations cannot be applied and a new kernel has to be built and
deployed.

Credit
======

This vulnerability was reported to EGI SVG by Tobias Dussa.

References
==========

[1] http://seclists.org/oss-sec/2017/q1/471

[2] https://access.redhat.com/security/cve/CVE-2017-6074

[3] https://access.redhat.com/errata/RHSA-2017:0293

[4] https://access.redhat.com/errata/RHSA-2017:0294

[5] https://security-tracker.debian.org/tracker/CVE-2017-6074

[6] https://people.canonical.com/~ubuntu-security/cve/2017/CVE-2017-6074.html

[7] https://access.redhat.com/security/vulnerabilities/2934281

Timeline
========

Yyyy-mm-dd  [EGI-SVG-2016-6074]

2017-02-22 Public disclosure, EGI SVG notified by Tobias Dussa
2017-02-23 Heads-up sent to sites
```
