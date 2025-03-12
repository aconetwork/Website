---
title: "Windows 11 proper install on KVM"
date: 2025-03-06T15:29:02+01:00
# publishDate: 2025-03-06T15:29:02+01:00
url: /linux-mint-login-screen-settings/
# image: images/2024-thumbs/linux-mint-login-screen-settings.jpg
categories: 
  - how to
  - AST
  - AFT
  - ART
  - WIT
  - health
tags: 
  - Windows
  - Linux
  - Ubuntu
  - Android
  - What is that
  - Hardware
showtoc: false  # Table of content: Hide (false) or show (true)
draft: true  # Draft: Show (false) or hide (true)
language: "English"
---

https://www.youtube.com/watch?v=7tqKBy9r9b4

<disk type="file" device="disk">
  <driver name="qemu" type="qcow2" cache="none" discard="unmap"/>
  <source file="/media/aco/LinuxData/VirtualMachines/win10.qcow2"/>
  <target dev="vda" bus="virtio"/>
  <alias name="virtio-disk1"/>
  <address type="pci" domain="0x0000" bus="0x04" slot="0x00" function="0x0"/>
</disk>

## Walkthrough Video
<!--
{{< youtube "" >}}
-->