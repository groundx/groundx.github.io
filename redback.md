---
layout: page_without_header
title: Redback Advanced Static Binary Injection
permalink: /redback/
---

<h1>Redback: Advanced Static Binary Injection</h1>

<p align="center">
<img width="200" src="/images/redback.png">
</p>

Static binary injection is a technique to permanently insert external code to an executable file, in order to observe or modify target behavior at run-time. From an attacker's perspective, this is helpful to enable persistent infection. For the defense side, this plays a crucial step in binary instrumentation. Unfortunately, good injection tools are seriously lacking: firstly, existing tools only support some limited platforms or CPU architectures. Secondly, they all restrict the injected code to be written in low-level assembly, which significantly raises the cost of development and maintenance.

It is highly complicated to implement a good static injection tool, which in essential requires to build an advanced static linker to properly link target binary with external code, so the output executable can be legitimately executed on modern systems with many mitigation techniques enabled by default. Considering that we wish to inject code built from high-level languages such as C/C++, the task is much more challenging.

This work provides a comprehensive overview on how static code injection is done on all platforms (Windows, MacOS, Linux, BSD). We will present all the technical issues we had to overcome, including understanding different executable file formats, how to expand the original binary to accommodate new code, data and meta-data coming from external binary, and how our static linker leverage the OS dynamic linker to do heavy lifting job for us.

We implemented all the ideas in a new solution named Redback. Our tool can inject code built from high-level languages like C/C++ into target executable of all platfoms (Windows, MacOS, Linux, BSD are confirmed). Redback also works cross-architecture (with support for ARM, ARM64, Mips, PPC, X86), and can handle multiple executable formats (PE/PE+, MachO & ELF).

More details on our project will be presented at [Blackhat Asia 2020](https://www.blackhat.com/asia-20/briefings/schedule/index.html#redback-advanced-static-binary-injection-18660).

-------
### Update

The tool will be released after our talk at **Blackhat Asia 2020**. Keep checking this page for more announcements.

-------
### Authors

- [Nguyen Anh Quynh](https://twitter.com/capstone_engine)
- [Do Minh Tuan](https://twitter.com/tuanit96)

