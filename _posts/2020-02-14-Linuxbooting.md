---
title: "Linux bootstrapping"
date: 2019-12-20
tags: [Linux, system internals]
header:
  image: "/images/bootstraping.png"
excerpt: "Linux, system internals"
---

## Introduction

A machine first executes the boot code stored in ROM when turned on. This code is then determining the way to load the Kernel and start it. Kernel then probes hardware components and spawns system init/systemd processes with PID 1.



1. Bios --> POST --> Boot device --> MBR
2. Reading boot loader from MBR
3. Loading and initialization of Kernel
4. Device detection and config
5. Creation of Kernel processes
6. Execution of startup scripts

There is no visible PID 0 under Linux, init is accompanied by server memory and kernel processes. These processes can be identified by brackets around their names in ps or top outputs and will have low numbered PIDs. Some process names will have a slash and a digit at the end such as [kblockd/0]. The number indicates the processor on which the thread is running in a Multiprocessor machine.

Some examples are,

[kjournald] : Perform file system journal updates commits to disk
[kswapd] : Performs swapping when physical memory is low.
[khubd] : Configure USB devices.

These can be considered as kernel portions dresses up like processes for architectural and scheduling reasons. Kernel's role in bootstrapping is completed once these processes are created. None of these basic operations handling processed have been created nor the system daemons are started. This is done by init/systemd.


# Single User Mode/Recovery Mode:

Single user mode can be accessed by passing a command-line flag by the Kernel. 

-----
kernel /vmlinuz ro root=LABEL=/ rhgb quiet single
-----

You will be prompted to enter your root password during the single-user user mode. Type <cntl D> to bypass the single-user mode and to proceed with the normal boot process. Sometimes only root partition will be mounted in single-user mode. Mount the required file systems manually to use applications/ programs that are not available under root partition.