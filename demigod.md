---
layout: page_without_header
title: Demigod Emulating Kernel Rootkits
permalink: /demigod/
---

<h1>Demigod: Emulating Kernel Rootkits</h1>

Kernel rootkit is considered the most dangerous malware that may infect computers. Operating at ring 0, the highest privilege level in the system, this super malware has unrestricted power to control the whole machine, thus can defeat all the defensive & monitoring mechanisms. Unfortunately, dynamic analysis solutions for kernel rootkits are severely lacking; indeed, most existing dynamic tools are just built for userspace code (ring 3), but not for Operating System (OS) level. This limitation forces security researchers to turn to static analysis, which however proved to be very tricky & time consuming.

This research proposes a novel approach to deal with kernel rootkits. We introduce **Demigod**, a framework to emulate OS environments, so kernel rootkits can be run in software emulators, all in ring 3. From this sandbox, we can safely monitor, trace, debug or perform all kinds of dynamic analysis with this advanced malware.

Emulating complicated OS such as Windows, MacOS & Linux is a challenging task. We will present all the technical issues we had to deal with, including how we built our own loader and dynamic linker, how to emulate the OS environment, essential kernel components and system APIs to allow rootkits to work.

Designed & implemented as a cross-platform-architecture engine, **Demigod** can emulate Windows, MacOS & Linux on X86/Arm/Aarch64/Mips. On top of our framework, we built some advanced tools to analyze kernel rootkits, including some automated solutions, providing the malware analyst new weapons to ease their labor work.

**Demigod** is based on [Qiling emulator](https://qiling.io). More details on our project will be presented at [Blackhat USA 2020](https://blackhat.com/us-20/briefings/schedule/#demigod-the-art-of-emulating-kernel-rootkits-20009).

-------
### Authors

- [Nguyen Anh Quynh](https://twitter.com/capstone_engine)
- [Nguyen Hong Quang](https://twitter.com/quangnh89)
- [Do Minh Tuan](https://twitter.com/tuanit96)

