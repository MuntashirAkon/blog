---
layout: post
title: "June'25 Updates"
description: "App Manager development update: No release last month due to lack of significant changes; successful collaboration with IzzySoft made debug releases reproducible, with stable releases to follow from v4.0.5; highly anticipated 'Finder' feature nearing launch with phased rollout to ensure reliability without beta testing; plans shifted from building a full app store to implementing a privacy-focused update functionality aligned with Android principles, designed to suit diverse user threat models."
date: 2025-07-06T13:49:00-07:00
tags: app_manager
---

There hasn't been a release last month because there were no significant changes to the project that requires a new release. Last month, I along with IzzySoft have tried to make App Manager reproducible and has largely been successful. All the debug releases are now reproducible, and the stable releases too shall be reproducible from the next release (v4.0.5).

The highly anticipated "Finder" feature is nearing completion, and I think, I can launch it at the end of this month or the next. This feature required some thorough planning in order to make it future-proof and usable for most users (and much more usable for advanced users). Initially, only a handful of features will be enabled for the stable releases, and gradually all the anticipated features will be released. The reason for this kind of rolling release is because we no longer have the beta testing system that we used to have, yet a certain level of confidence is required in order to release a feature like this. Similar to profiles, the possibilities with this feature is endless, some of which may remain unknown for some time. There are also a few small but exciting improvements that are coming up (which shall be revealed in due time) in the upcoming releases.

Regarding the app store functionality, I've given it a thought and concluded that rolling out an entire app store is time consuming and largely unnecessary for the time being. Instead, we can launch an update functionality instead. The update functionality, unlike F-Droid or Obtainium, will adhere to the Android principles at the same time offering a level of privacy and security that will be suitable for a wide range of individuals (as always, in developing App Manager, I've always focused on offering a diversified threat model so that it can accommodate most users). You can find some information regarding the design at this link: <https://github.com/MuntashirAkon/AppManager/issues/464>. However, there are a few changes to the original design which will be revealed as I begin working on it.

That's all. Thanks for reading.
