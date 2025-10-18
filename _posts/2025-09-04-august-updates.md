---
layout: post
title: "August'25 Updates"
description: "App Manager development update: delayed release, acid test for open source community, and integrating ADB backups in App Manager."
date: 2025-09-04T15:14:00-07:00
tags: app_manager
---

The next release of App Manager (that is, v4.0.6) is delayed because I was very busy with work last week. I'll try to release it in the next week as I need to take care of a few more things.

At first, I'd like to talk about one of my concerns that has been in mind for a while. Despite what many politicians want you to believe, the world is in a grave financial crisis, and there is no easy way out of it. What we're seeing at present seems to be a replay of the financial crises in the 1970s, except the world is more connected than before, thanks to the Internet, and this has its own set of disadvantages like we saw during the Covid period when the world ran into an absolute chaos. However, unlike the Covid period, people's ability and motivation to continue hobbies are going to be challenged, especially if they are not financially productive, and this can have an adverse effect in the open source community where many projects (including App Manager and the related projects) are developed and maintained by hobbyists like me. Notice that App Manager costs me nothing other than time (which is still quite costly in the developed world), but there are many projects that are quite costly in terms of money and resources. Most concerning of all: some of them play a significant role in areas of utmost importance (like the Internet itself or defense, compared to App Manager which is not that important as a project) and are being developed by maintainers quite thanklessly without any form of compensation. This is going to be an acid test for the open source community, and I believe the landscape will see a significant alteration in the future.

Of late, I've been working on the backup/restore feature of App Manager. As some of you know, I've already created the framework for converting a App Manager backup to and from a regular ADB backup a long time ago, but handling ADB backup and restore itself is not that straightforward using the Android APIs, but it's not impossible, and since a lot of the users are now using App Manager in ADB mode, I think I'll give it one more shot. If I can implement this correctly, the feature will be available v4.1.0, otherwise we'll continue to test it in the debug versions.

Lastly, I'm still looking for contributors for the ADL project. If you're interested, please send me an email with your Matrix username. Thanks.