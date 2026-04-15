---
layout: post
title: "Linux Apps that I Frequently Use"
description: "About four months ago, I had migrated to Fedora 43 (GNOME 49). After four months, I think I can share the frequently used apps like I did for Android."
date: 2026-04-14T21:30:00-07:00
tags: linux
comment_id: 11
---

Linux is not particularly known for having good and usable (GUI) applications. This is the #2 complain that you hear from people (#1 being the difficulty of installation which, unfortunately, still exists today) who do not use a Linux distro. I think this is largely invalid now. With the introduction of GTK 4, the development of GUI applications have been accelerated, and we see a lot of young and student developers building applications for Linux. In addition, with WINE and Proton, Linux is becoming a popular platform for gaming too. If you are interested in old games that have 8-bit components, WINE is basically the only option right now since they no longer work on Windows. Anyway, let's talk about the applications I have been using quite frequently on Fedora. Unlike [my previous post for Android]({{ "" | relative_url }}{% link _posts/2022-12-30-android-apps-that-i-frequently-use.md %}), I shall talk about the applications in a little bit more detail since unlike Android, Linux is still a growing platform and most applications have a certain level of instability.

## GNOME Extensions

Since I am using GNOME Shell 49, I thought I should list the GNOME extensions first since they the one of the most frequently used applications. The list is sorted alphabetically.
1. [Battery Power Indicator](https://extensions.gnome.org/extension/9204/battery-power-mode-indicator/): Changes battery icon color based on active power profile. Very useful extension if you're on a laptop.
2. [Bluetooth Battery Meter](https://extensions.gnome.org/extension/6670/bluetooth-battery-meter/): Displays battery levels for the connected devices. Very useful extension if you use a lot of wireless devices, such as wireless mouse, keyboard, or headsets.
3. [Compiz alike Magic lamp effect](https://extensions.gnome.org/extension/3740/compiz-alike-magic-lamp-effect/): Magic lamp effect inspired by the Compiz ones from macOS, works good with Dash to Dock.
4. [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock/): Moves the dash out of the overview transforming it in a dock for an easier launching of applications and a faster switching between windows and desktops. Surprised that it's not built-in in GNOME. For better UX, set "Click action" to "Minimize or show previews". It may look like macOS, but it has more useful features than macOS' dock.
5. [Dim Completed Calendar Events](https://extensions.gnome.org/extension/5979/dim-completed-calendar-events/): Dims completed events in the top panel menu to easily distinguish between upcoming and past events. Again, surprised that GNOME doesn't do this by default. It's the most basic feature in most calendar applications.
6. [In Picture](https://extensions.gnome.org/extension/8692/in-picture/): To fix broken Picture-in-Picture in Wayland that is taking GNOME ages to fix.
7. [Kiwi is not Apple](https://extensions.gnome.org/extension/8276/kiwi-is-not-apple/): Brings macOS-inspired features for GNOME. Actually, I dislike many features that macOS has. For example, I have disabled the following features among others: transparent move, panel transparency, macOS window buttons. But the rests are useful in the sense that I had to install a few more extensions that would allow me to achieve the same.
8. [Light style](https://extensions.gnome.org/extension/6198/light-style/): Enables light mode in GNOME. I used to be a big fan of dark mode, but nowadays, I prefer light mode since it looks more natural.
9. [Peek Top Bar On Fullscreen](https://extensions.gnome.org/extension/6048/peek-top-bar-on-fullscreen/): Shows the top panel on demand while displaying full screen content on (like watching a video in full screen mode). A very useful feature not just for watching videos but also when delivering a presentation.
10. [Rounded Window Corners Reborn](https://extensions.gnome.org/extension/7048/rounded-window-corners-reborn/): It's 2026, and GNOME still doesn't offer rounded corners for windows by default when even Windows is trying to do the same.
11. [Screencast extra feature](https://extensions.gnome.org/extension/8764/screencast-extra-feature/): Again, it's 2026, and GNOME is still struggling with recording audio with the built-in screen recorder. Alternative is to use OBS Studio, of course.
12. [Slob Dictionary Quick Lookup](https://github.com/MuntashirAkon/SlobDict): Launches Slob Dictionary to display defition of the selected text. This is one of my own applications, and also the first ever GUI application I have built for Linux.
13. [Smart Pause & Resume](https://extensions.gnome.org/extension/9167/smart-pause-resume/): Automatically pauses previously playing media to prevent overlapping sound. Surprised that GNOME doesn't provide this by default. Pretty much every other operating system offers similar features.
14. [Steal my focus window](https://extensions.gnome.org/extension/6385/steal-my-focus-window/): Removes the "window is ready" message and focus the window instead. When a window is already running and you open something that triggers the window, instead of bringing the window to the top of the window stack, GNOME chooses to display a popup notification instead. Never understood the reason for this weird behavior.
15. [system-monitor-next](https://extensions.gnome.org/extension/3010/system-monitor-next/): Displays system information in the status bar, such as memory, CPU, disk and battery usages, network rates. I'm only interested in the network monitor, but there is not a good extension for displaying network monitor only.
16. [WinTile](https://extensions.gnome.org/extension/1723/wintile-windows-10-window-tiling-for-gnome/): a hotkey driven window tiling system that imitates the standard Win-Arrow keys of Windows 10. GNOME's default tiling behavior is too simple. WinTile is one of the basic ones. There are a couple of advanced ones too, such as [Tiling Shell](https://extensions.gnome.org/extension/7065/tiling-shell/).
17. [WorkNavigator](https://extensions.gnome.org/extension/9120/worknavigator/): A simple workspace navigator. I like it's simplicity and design.

It might seem a lot, but many of the features should have already been in GNOME itself, or fix those long standing bugs.

## Firefox, a Web Browser

I used to use [Ungoogled Chromium (UGC)](https://github.com/ungoogled-software/ungoogled-chromium) on Windows and macOS. But since Firefox comes default in Fedora, I decided to give it a try, and it looks very decent albeit not as good as Chromium-based browsers in terms of UX. I use a multi-profile setup like I used to on UGC. I know Firefox support compartmentalization in a single profile, but in my threat model, a multi-profile setup is better. Nothing to complain here. As usual, extensions such as [uBlock Origin](https://github.com/gorhill/uBlock), [Clear URLs](https://docs.clearurls.xyz/), and [Decentraleyes](https://decentraleyes.org/) are a must for Firefox too. To match GNOME theme, I use a theming application called [Add Water](https://addwater.qwery.dev/).

## VSCodium, a Code Editor

As a developer, [VSCodium](https://vscodium.com/) (the open source version of VSCode) is a must. Good thing is that most Microsoft-signed proprietary extensions do not work here. I mostly use the open source extensions, such as clangd, Kylin Python, and Open Remote - SSH.

## Terminal

I use [the built-in terminal](https://gitlab.gnome.org/chergert/ptyxis) in GNOME Shell. It's a pretty decent terminal emulator and works as expected.

## Betterbird, an Email Client

[Betterbird](https://www.betterbird.eu/) is a better version of [Thunderbird](https://www.thunderbird.net/) that has a wider set of features, including an option to add it in the status bar, which is useful in GNOME since the email client doesn't run in the background if it is closed. The UI still looks very old, but there is a way to fix this via [this theme](https://github.com/rafaelmardojai/thunderbird-gnome-theme).

## Calendar

I use [the built-in calendar](https://apps.gnome.org/Calendar/) in GNOME Shell. The calendar mostly works well except for two issues: first, if you set an event with _from_ and _to_ dates, the _to_ date appears exclusive, which is highly unusual. Second, it doesn't allow arbitrary days of the week selection in _Weekly_ mode which is a big problem. Fortunately, ALL the other calendar applications I have tried has both features, so I can just use them instead on my other devices. There are also a few other annoyance, but it _mostly_ works. For synchronization, I use a [NextCloud](https://nextcloud.com) instance.

## LibreOffice, a Document Processor

For document processor (as well as spreadsheet and presentation), I use [LibreOffice](https://www.libreoffice.org/). It comes built-in with Fedora 43. So, I didn't have to do anything.

## BitWarden, a Password Manager

For password manager, I use [BitWarden](https://bitwarden.com/). It looks more like a wrapper around the web UI instead of an actual desktop application though. It seems UI/UX is not particularly a strong suit for BitWarden team.

## Recordbox, a Music Player

[Recordbox](https://codeberg.org/edestcroix/Recordbox/) is a music player written in Rust and GTK 4 framework and still under heavy development, and it is the only music player that balances the features and the look (trust me, I've tried over 20 music players). Unfortunately, it doesn't offer a tag editor (only offers a lyrics editor). But it can play a lot of different music formats. In the past it had some weird bugs which prompted me to use [Elisa](https://apps.kde.org/elisa/) instead (which doesn't have a good UI but has a fully featured tag editor), but they seem to have been addressed, and it works pretty well now.

<figure>
  <img loading="lazy" src="{{ 'images/Screenshot From 2026-04-14 19-29-23.png' | absolute_url }}" alt="Playing Beethoven's Piano Concerto No. 5 in Recordbox" />
  <span class="marginnote">Playing Beethoven's Piano Concerto No. 5 in Recordbox</span>
</figure>

## nheko, a Matrix-client

[nheko](https://nheko-reborn.github.io/) is a Matrix client developed using Qt 6. It is one of the first fully-featured Matrix clients that doesn't use Electron. So, it looks native to the platform and has less memory footprint. The user interface is similar to Telegram albeit a little low on the style part. It also supports running on the system tray and offers desktop notifications. If you want a GTK 4 client, [Fractal](https://gitlab.gnome.org/World/fractal/) is one of the emerging clients. However, as of writing this post, it doesn't support running in the background and neither does it support running it in the system tray. So, there is no way to receive notifications without keeping it in the foreground. It is also very slow to scroll in room with a lot of messages, and most importantly, no option to filter messages. So, I wouldn't recommend it.

<figure>
  <img loading="lazy" src="{{ 'images/nheko-chat.png' | absolute_url }}" alt="The chat window of nheko" />
  <span class="marginnote">The chat window of nheko (taken from their website)</span>
</figure>

## LocalSend, a Local File-sharing Application

[LocalSend](https://localsend.org/) is a cross-platform local file sharing service that I use in all platforms. I use a bunch of different operating systems (Android, Fedora, iPadOS), and LocalSend is the only file sharing service that supports all of them. So, it's very useful, and one of the first applications that I install in any platform.

<figure>
  <img loading="lazy" src="{{ 'images/Screenshot From 2026-04-14 19-58-25.png' | absolute_url }}" alt="The main window of LocalSend" />
  <span class="marginnote">The main window of LocalSend</span>
</figure>

## Cine, a Video Player

[Cine](https://github.com/diegopvlk/Cine) is a MPV-based video player developed with GTK 4 and libadwaita. So, it has a native look-and-feel in GNOME. It is actually far better than the default video player which sometimes fails to play certain video formats. It is comparable to [IINA](https://iina.io/), my all-time favorite video player from macOS, except a dedicated Picture-in-Picture (PiP) mode. Since it doesn't offer a PiP mode, I simply move it to one side and enable “Always on Top” and “Always on Visible Workspace” to achieve something similar.

<figure>
  <img loading="lazy" src="{{ 'images/Screenshot From 2026-04-14 20-14-53.png' | absolute_url }}" alt="Playing a random video in Cine" />
  <span class="marginnote">Playing a random video in Cine</span>
</figure>

## Foliate, an eBook Reader

[Foliate](https://github.com/johnfactotum/foliate) is a GTK 4-based eBook reader. It automatically adds all the opened books to its library, and also allows downloading books from OPDS catalogs (with Internet Archive, Project Gutenberg, etc. provided by default). It also support adding annotations to eBooks as well as exporting them. It has a look-and-feel similar to Apple Books, which is one of my favorite eBook readers.

<figure>
  <img loading="lazy" src="{{ 'images/Screenshot From 2026-04-14 20-19-13.png' | absolute_url }}" alt="First pages of “Pride and Prejudice” opened on Foliate" />
  <span class="marginnote">First pages of “Pride and Prejudice” opened on Foliate</span>
</figure>

## Tuba, a Fediverse Client

[Tuba](https://tuba.geopjr.dev/) is a GTK 4 and libadwaita-based Fediverse client that supports Mastodon, GoToSocial, Akkoma, and a few others. It fully supports GNOME with background notification (disabled by default for some reason). I didn't find any other alternatives to this application.

<figure>
  <img loading="lazy" src="{{ 'images/Screenshot From 2026-04-14 20-35-24.png' | absolute_url }}" alt="Mastodon on Tuba" />
  <span class="marginnote">Mastodon on Tuba</span>
</figure>

## Switchyard, a Browser Launcher

[Switchyard](https://switchyard.aly.codes/) is a GTK 4-based browser launcher. I have been looking for a [URLCheck](https://f-droid.org/packages/com.trianguloy.urlchecker/)-like alternative for Linux, and Switchyard is as far as I could go. It offers browser rules, link redirections, and a custom configuration, all good. Unfortunately, it doesn't support the ClearURL format, which I was looking for. But at least, there is an app like this.

<figure>
  <img loading="lazy" src="{{ 'images/Screenshot From 2026-04-14 20-44-54.png' | absolute_url }}" alt="Switchyard UI" />
  <span class="marginnote">Switchyard UI</span>
</figure>

## Flatseal, Permission Manager for Flatpak

[Flatseal](https://github.com/tchx84/flatseal) is a permission manager for Flatpak, basically a GUI wrapper over the flatpak command, but it is very useful in managing permissions of Flatpak applications.

## Ignition, a Startup Manager

[Ignition](https://github.com/flattool/ignition/) is a GTK 4 and libadwaita-based application that allows managing startup applications and scripts. Although not really a frequently-used application, it is highly recommended since GNOME Tweaks is no longer in the picture.

## OBS Studio

Unfortunately, GNOME has troubles with projectors. Many projectors have lower resolution than a modern laptop, and as a result, when connected to a projector in the mirror mode, it calculates the lowest resolution among the two and falls back to the lowest resolution, which is a problem if the projector has a really low resolution. As an workaround, OBS Studio can be used to stream the laptop screen to the projector and use the full resolution.
