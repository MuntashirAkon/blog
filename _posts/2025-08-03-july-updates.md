---
layout: post
title: "July'25 Updates"
description: "App Manager update: Introducing a new filter-based profile type leveraging Finder features in upcoming v4.1.0; ongoing migration of main page filters to this flexible system; progress on a unified updater framework designed to securely manage app updates from trusted sources with strict source assignment and customizable trust levels."
date: 2025-08-03T16:18:00-07:00
tags: app_manager
comment_id: 8
---

> In order to provide a convenient option for non-Telegram users to follow the updates, they will also be posted on my personal blog. Past updates will also be gradually added there. You can subscribe to my blog posts via RSS or follow my personal Mastodon/X account. Transparency reports will also be posted to App Manager's official Mastodon/X accounts. An archive of the reports will be maintained in a GitHub gist for now.

I think many testers already know this: I've implemented a new type of profile that allows filtering apps by the set of filters offered by the Finder feature. This feature is going to be very useful for recurrent activities like force-stopping all the user apps that are currently running. Again, the possibilities are endless. Although the regular apps-based profile is kind of a subset of this profile, I decided to implement them separately to keep the apps-based profile very simple and fast to execute (since filter-based profiles are inherently slower than apps-based profile). The feature will be available to stable users from v4.1.0 (release date not fixed yet). The filters in the main page are also being migrated to use the Finder-style filters so that the users can generate and use their own set of filters instead of the predefined ones. Finder itself along with this exclusive filtering options will be available to stable users in a future release.

I have done some progress on the updater implementation and can share some of the ideas to the readers for both transparency and scrutiny. But at first, let's take a look at the issues that we need to handle in order to implement a unified updater:
1. App Manager app itself has limited internet features, and we intend to keep it this way
2. It's necessary to enforce a static single source assignment, that is, once an installed app is assigned to a source, subsequent updates should also be sourced from that source
3. It's also necessary to establish the levels of trust and the priority of sources should be assigned based on the trust
4. It's crucial that the users can amend 2-3 depending on their threat model.

These are very challenging issues, and addressing them completely is nearly impossible. But I've designed a protocol and a framework to address those issues in an optimal way. In this protocol, App Manager effectively acts as an updater client that retrieves updates from the sources which are basically extensions to App Manager. The update process itself works in two independent steps. In the first step, App Manager queries the sources for new updates (based on the source assignment). Upon receiving such a query, the sources check for updates and return a list of updates to App Manager. In the second step, App Manager ask the sources to download some (or all) of those updates which the sources download (or retrieve from caches) and return a list of URIs that App Manager has access to. App Manager later retrieves those updates and installs them. This design has several advantages:
1. Each source remains separate and can be installed or removed independently
2. For each source, it's possible to assign a trust level and handle per source security (HPKP, GPG, etc.)
3. Each source only uses the minimum number of permissions to function which reduces the attack surface even if some of the security mechanisms are bypassed
4. It's easy to provide per extension updates compared to the monolithic approach where any simple changes to any sources requires a new update
5. Using modern Android platform features, it's easy to persist single source assignments beyond App Manager.

To clarify the level of trust a bit more, it's necessary to support only the legitimate sources instead of arbitrary source and assign each a priority which are actually more challenging than the rests, because the definition of legitimate sources remains unclear to me, and without an exact definition, it's almost impossible to assign priorities as well. I initially came up with a priority list for the app stores, but I didn't explain why they were prioritized this way. Therefore, it is necessary to define leigitimate sources and factors that are needed to be taken into account to assign priorities. Again, this is a challenging problem, and for now, I'll rely on my own instinct for it. For the same reason, App Manager will not support any third-party updater extensions. The updater will rely on a signature permission to interact with the sources, and therefore, the extensions must be signed using the same key used to sign App Manager.
