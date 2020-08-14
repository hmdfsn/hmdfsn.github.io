---
layout: page
permalink: /projects/
title: Research Projects
tags: [code]
modified: 3-10-2014
comments: false
---


* [**Software Supply Chain Security**](https://github.com/in-toto/in-toto)<br>
_in-toto_: The first framework that cryptographically ensures the integrity of the software supply chain from the moment it is developed until end users install it. in-toto is a CNCF project and is already integrated into a dozen products and open source projects (e.g., Debian, Datadog, Cloud-Native) that are used by millions of users daily.<br>
More details in our [***USENIX Security 2019***](https://www.usenix.org/conference/usenixsecurity19/presentation/torres-arias) paper.

* [**Source Code Integrity**](https://github.com/le-git-imate/le-git-imate)<br>
_le-git-imate_: A security mechanism to add verifiability to untrusted web-based Git servers by pioneering true GPG-signed Git commits in the browser. le-git-imate is already implemented on top of GitHub and GitLab and is general enough to be integrated with similar services such as Facebook Phabricator or Atlassian Jira.<br>
More details in our [***JCS 2020***](https://content.iospress.com/articles/journal-of-computer-security/jcs191371) and [***AsiaCSS 2018***](https://dl.acm.org/doi/abs/10.1145/3196494.3196523) papers.

* [**Verifiable Code Review Process**](https://github.com/safereview/safereview)<br>
_SafeReview_: A security mechanism that can be applied on top of an untrusted Git-based code review system (such as GitHub and Gerrit) to ensure the integrity of the code review process and provide verifiable guarantees that the code review process followed.<br>
The corresponding paper is submitted to a conference.

* [**Policy Checker**](https://github.com/safereview/policychecker)<br>
Toolbox to automatically check if a given set of code reviews matches the code review policy. It helps to interpret the code review policy and to check a given set of code reviews against the policy.

* **Hypervisor-Based Rootkit Detection**<br>
_TINC_: A hypervisor-based kernel rootkit detection method by analyzing kernel system calls, VMCS registers, and kernel data structures. TINC first analyzes system calls and VMCS registers. It then evaluates sensitive fields and kernel data structures. Finally, the intra-structure relations will be evaluated to detect stealthy malware.
<!--More details in our [***ISCISC 2012***](#) paper.-->

* **Hypervisor-Based Operating System**<br>
Commodity operating systems are normally based on a monolithic kernel with millions of lines of code. Reachable kernel code from untrusted applications (i.e. via APIs),  buggy drivers (networking and USB stacks) provides a huge attack surface. Indeed, when one successful kernel rootkit breaks the security of the system, it can bypass any security mechanisms (e.g. SELinux and LXC) and compromise the entire system. To address such issues, we advocated the principle of "Security by Isolation" proposed by [Qubes OS](https://www.qubes-os.org/) and explored ways to improve the reliability of a hypervisor-based OS. Our main focus was to provide (1) isolated lightweight virtual machines (VMs) for any device driver, (2) secure data transfer between VMs, (3) inter and intra mandatory access control on VMs, (4) secure dual-homed host using lightweight network VMs.

