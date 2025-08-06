---
layout: post
title: "July'24 Updates"
description: "App Manager update amid Bangladesh's July Massacre: no beta release due to nationwide violence and internet blackout during protests against the discriminatory government job quota system causing over 277 deaths; progress on backup/restore feature; investigation ongoing into directory access issues on some devices via ADB; some insights on Android permission model."
date: 2024-08-01T06:05:00-07:00
tags: app_manager
---

1. The situation in my country wasn’t very well this month (and won’t be in this month). The police, the special forces, the armed forces along with the student wing of the current political party attacked the students and civilians, protesting against a discriminating quota system in govt jobs, throughout the country resulting in the death of 277 or even more, which is highest number of deaths in a single movement since its independence in 1971 (we’re now calling it the July Massacre). In addition, the Internet wasn’t available for five days throughout the country, and the cellular Internet wasn’t available for ten days, and the Internet speed is still very slow. I posted some updates earlier in the debug channel on Telegram, and a few users emailed me and offered to help me in any way they can. Thank you for your emails. Just to give you an update, I’m well and safe, and I don’t need any help right now. I also couldn’t focus on anything else, including this project. So, I couldn’t make a beta release like I announced earlier.
2. “Contributor of the Month” will be skipped for July due to the above circumstances.
3. I’ve been seriously working on the backup/restore feature. It needs a lot of improvements including support for importing/exporting contacts, SMS/MMS, Wi-Fi configurations, VPN apps, autofill apps, accessibility apps, input methods, spell checkers, notification channels, and so on. Some of the features require a lot of work, and won’t be available anytime soon. Be sure to take a look at the changelogs to find what’s new in backups!
4. It appears that some directories aren’t accessible on some devices (Amazon Fire TV, or example) in ADB mode. What’s more curious is that newer Androids don’t support opening streams via ADB in some directories (blocked via SELinux). As a result, we may need alternative methods (such as no-root usage or streaming via shell) for those cases. However, further investigation is needed.
5. As I started looking into the permission issues, it appears that the sorting out all the permissions is not an easy thing to do, and a lot of people in the past have tried to come up with solutions, but none of them have offered any perfect solution. This is almost an impossible task for several reasons:
    a. There are two permission APIs (i.e., PermissionManager and AppOpsManager)
    b. Some permissions are merged with each other in those APIs which can cause unexpected behaviour both aren’t altered at the same time
    c. Although each permission (or app op) supports a wide set of modes or flags, only a few specific modes or flags actually work with a permission and finding this out is complicated, especially for the infrequently used permissions (as they are not available in Android Settings to find how they should actually be granted or revoked)
    d. Many permissions (and most app ops) have no public documentation, making it difficult to find out what they are supposed to do
    e. There are some other APIs that should’ve been included with the permission APIs (e.g., battery optimisation, sensor, net policy) as their independent presence makes no sense
    f. Some vendors include their own sets of permissions and app ops whose behaviours are largely unknown
    g. Vendors provide permission whitelists for some applications (fortunately, this is manageable through the permission flags)
    h. Same permissions work differently in each version of Android, and
    i. Some app ops depend on other app ops.
    
    Therefore, in creating a permission model, we’ll have to unify all those permission APIs and present them to the user in a way so that it would look as if the permissions are handled by a single permission API, and this isn’t an easy thing to do. Because we still have to provide a way to show which permissions are affected by the change and offer an option to alter them manually. This is further complicated by other apps (e.g., App Ops, Permission Pilot) that offer their own sets of abstraction, and the user expects similar behaviour from App Manager. Another issue is that the purpose of the “Uses Permissions” and “Permissions” tabs were to display the permissions declared in the manifest of the app. If such a permission model is implemented, it should not replace those tabs.
