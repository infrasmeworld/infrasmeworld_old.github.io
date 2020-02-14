---
title: "Linux bootstrapping"
date: 2019-12-20
tags: [Linux, system internals]
header:
  image: "/images/bootstraping.png"
excerpt: "Linux, system internals"
---

## Introduction

When a machine is turned on, it first executes the boot code stored in ROM. That code then attempts to find out how to load kernel and start it. The kernel probes system hardware and spawns system init/systemd processes with PID 1.

1. Bios --> POST --> Boot device --> MBR
2. Reading boot loader from MBR
3. Loading and initialization of Kernel
4. Device detection and config
5. Creation of Kernel processes
6. Execution of startup scripts

