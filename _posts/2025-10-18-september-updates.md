---
layout: post
title: "September'25 Updates"
description: "App Manager development update: delayed release for v4.1.0, ADB backup integration, and a new kind of firewall for Android"
date: 2025-10-18T12:53:00-07:00
tags: app_manager
comment_id: 9
---

This month (October) has been a busy month for me (I mean more than usual). I've had certain timeline set up for the next release, but due to my busy-ness, I don't think I will be able to meet my goals for the next release any time soon.

Last time I've announced that I was working on ADB-based backups, and last month, I was able to integrate it fully into the existing backup model. This required a major rewrite of the backup/restore feature, but I think it would be beneficial to the large number of ADB users that App Manager has.

Recently, somebody has created [a feature request on GitHub](https://github.com/MuntashirAkon/AppManager/issues/1754) regarding a ADB-based network firewall implementation. From Android 13, it is possible to utilize the Berkeley Packet Filter (BPF) to cut network connections from an application. You can also do this using ADB shell or terminal with root:

```sh
cmd connectivity set-package-networking-enabled [true|false] [package-name]
```

The underlying implementation fetches the UID of the package name and then add the UID and rule to a BPF map for filtering the packets for the UID (for shared applications, multiple applications packages may be blocked as they share the same UID). But the issue with BPF rules is that the rules do not persist across reboot. This means you'd need to reapply the rules after restarting your device which is inconvenient. A possible solution to the problem, of course, is reapplying the rules on reboot, which again, is not convenient since ADB mode is also lost after a reboot. So, to effectively implement this feature, we need to find a way to monitor Wi-Fi connections on reboot and connect to wireless debugging automatically once the device is connected to Wi-Fi. I've already implemented a prototype last night, and it's working correctly on my test device (Pixel 9). On Android TV, ADB over TCP persists across reboots, so we may also able to do something similar on Android TVs too. After the feature becomes stable enough, I think it would be possible to implement BPF-based firewall for devices that support it that would persist across reboots.

IP tables based blocking and VPN-based packet filtering remain the most used filtering technology in Android due to the availability of many open source firewall tools (and closed source ones most of which are just clones of the former). However, these sort of blocking, as I've argued before, are not very effective, and from Android 12, their effectiveness has been further reduced. This has happened because Android 12 has integrated eBPF (extended BPF), and since then the internals of the AOSP has been modified to use eBPF instead of the traditional IP tables approach. If you don't know about BPF, let me explain it in simple words: BPF is a kernel-level packet filtering mechanism that has the ability to decide which packet (any data transmitted from or to the internet has to go through a few layers, packet is one of them) goes to where or which packets it needs to drop. This allows a system whitelisted program in Android to directly send/receive packets without going through the typical route used by ip tables or VPNs. This means that the vendor can arbitrarily allow their vendor (and system) apps to bypass ip tables and VPNs which is not good thing for user privacy since for these applications, all the protections (for example, anti-censorship protections) become useless. This is where the BPF rules may help. The underlying implementation of the above mentioned command modifies the BFP map albeit temporarily overriding the existing UID rules if already present. This effectively allows us to temporarily override the rules even for the whitelisted apps. But in some cases, the rules may be refreshed even without a reboot. I'm still currently investing the implementation, so I don't have the exact details.

Finally, for the APK updater, I've already created a backend for it. But there are still a lot of challenges, such as effective handling of extensions and errors, what to display to the user, implementing the update policies, and so on. This will take some time and probably available for testing at the first quarter of 2026.

> **Note:** You may have to enable the **chain3** first before you can block networking for an app. To enable chain3, run this command:
> ```sh
> cmd connectivity set-chain3-enabled true
> ```
> This is only an on/off switch. The configurations are in the BPF map regardless of this option. Therefore, they are applied immediately when you enable chain3.
