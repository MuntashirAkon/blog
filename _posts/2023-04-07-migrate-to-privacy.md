---
layout: post
title: "Migrate to Privacy"
description: "You know about the privacy implications. But how to actually migrate away from the things that seem to be a part and parcel of your life?"
date: 2023-04-07T00:21:00+06:00
tags: Privacy
comment_id: 3
---

Several years ago, I quite accidently ran into an article on privacy while I
was browsing a website belonging to a sister project of Wikimedia Foundation.
It is amazing how carefully we are manipulated not to care about so basic a
right as privacy. But it is even more amazing how hard it is to find anything
on privacy online unless you're actually looking for it, and most privacy
activism groups seem to have no idea regarding this. Otherwise, none of them
would have put this famous Ed Snowden quote at the front:

> Arguing that you don't care about the right to privacy because you have
> nothing to hide is no different than saying you don't care about free speech
> because you have nothing to say.

Because this quote doesn't mean anything to those who have no idea what privacy
means. Privacy is not something that is taught in educational institutions, at
least, not seriously. And why should it be? Privacy awareness is perceived to
be harmful for the governments and intelligence agencies. Profiling citizens in
the name of terrorism is not just good for population control, it turned out to
be a very profitable business too.

So, you are one of the few (unfortunate!) people who are not only satisfied
with learning about privacy but also ready to actually do something about it,
this writing is for you. If you are a critic, please ignore this because I
shall not begin this by asking the readers to choose a threat model. When I was
looking for advice regarding privacy, people told me to choose a threat model
too. But the entire privacy-thing was new to me, and that particular statement,
at that time, seemed a little overwhelming.

Before getting started, there are a few things you should remember:
1. You cannot achieve privacy overnight. Depending on your online presence, it
   might take a couple of weeks to several years. Even then, there is no
   guarantee whether you've achieved total privacy.
2. You have to be ready to make some sacrifices. Like any sacrifice, they would
   seem quite depressing from time to time. But eventually, you will find
   yourself happier than you ever were.
3. You will begin to see the real faces of the people around you. This could be
   the most painful thing for you if you're fond of company. But it's better to
   learn the true nature of people around you early on so that you won't feel
   betrayed later in the most vulnerable moment of your life. This, you could
   say, is a byproduct of achieving privacy. Ease of communication, it appears,
   made it quite easy to deceive people.
4. You might have to lead a solo life if you do not have people who share your
   views. A great way to avoid this would be meeting people online in various
   groups where people discuss about privacy. You may end up finding some real
   good people there.

## Getting Started
The first thing you should do is change your E-Mail address. This might seem
quite silly thing to do to some people, especially those who do not use E-Mail
in a daily basis. But E-Mail plays an important role in tasks such as creating
accounts, delivery of good and services, and so on. E-Mail is your primary
identity on the Internet, thus, changing it is essential to achieve any privacy
at all.

There are many privacy-friendly E-Mail providers such as
[Riseup](https://riseup.net), [Disroot](https://disroot.org),
[Proton](https://proton.me) and [Tutanota](https://tutanota.com). Each offers
free services, and a few of them also offer premium services. Riseup requires
an invitation code meaning that you need to know someone who already use the
service in order to create an account there. In other cases, this is quite
straightforward. However, since you're just getting started, I would recommend
Disroot as it offers a wide range of features including NextCloud which is
quite useful as we shall see later.

After changing your E-Mail address, you may still need to use the old E-Mail,
at least, for receiving messages from contacts who may not know your new E-Mail
address. Some E-Mail providers such as Gmail offer E-Mail forwarding feature
which, when enabled, forwards all the messages to the specified E-Mail address.

Next, you need a temporay E-Mail service. This is essential for many reasons
such as creating temporary accounts to use a service with known privacy issues
or inserting E-Mail address in a download page which prevents you to download
your desired content unless you insert a verified E-Mail address. This may not
immediately be clear to you, but as you start to understand fingerprinting
methods, you'll find yourself using temporary E-Mails quite often. There are
many providers which offer such service such as
[AnonAddy](https://anonaddy.com/) and [Simple Login](https://simplelogin.io/).
Both are open source, privacy friendly, and has free tiers which should be
enough for most use.

## Migrate Cloud Services
Thanks to services offered by Google or iCloud, we become quite reliant on the
cloud services to store personal information such as contact list, calendar
events, notes, documents, etc., and due to how they are integrated and somewhat
abstracted, it might seem quite difficult to move away from them. This is not
quite true, however. You can quite easily replace most of these services with
privacy-friendly alternatives. The best alternative is NextCloud.

[NextCloud](https://nextcloud.com/) is a self-hostable, open-source and quite
popular alternative to the cloud services offered by the big companies. Despite
its being quite easy to setup and use, it is understandable that you may not
want to self-host it due to financial or other reasons. This is where Disroot
can help you. Because Disroot offers most of the NextCloud features for free.
This means when you create an account in Disroot, you automatically get most of
the features offered by those big companies in addition to privacy.

You can easily set up contact and calendar synchronisation in your favourite
app or operating system by setting up NextCloud as your CardDAV and CalDAV
provider just like E-Mails. In Android, you can achieve both using
[DAVx⁵](https://github.com/bitfireAT/davx5-ose/).

However, one of the biggest cloud service appears to be something people don't
even know of: Web Browsers. Both Google Chrome and Microsoft Edge use your
respective account for synchronisation which means that it knows all your
browsing history and timeline, and, thereby, knowing everything you do in the
Internet. The easiest way to migrate is to use a privacy friendly browser.
For Android, [Bromite](https://www.bromite.org/) is considered the best
alternative to Google Chrome. But for iOS, the only alternative at present is
[Brave Browser](https://brave.com/). If you've used Firefox, you can continue
using it, but be aware that Firefox, by default, is not a privacy-friendly
browser and requires a lot of tweaking to do. For Desktop,
[Ungoogled Chromium](https://github.com/ungoogled-software/ungoogled-chromium)
could be used, but although Ungoogled Chromium does not contain anything from
Google, most of the privacy features are disabled by default and you will need
to enable them manually. In addition, you need to install a few browser
extensions to prevent big brothers from tracking you across the web. I would
recommend the following browser extensions:

1. uBlock Origin - For blocking tracking and ads
2. LibRedirect - Redirect popular websites to their privacy-friendly
   alternatives
3. Floccus - Synchronise bookmarks in the cloud such as NextCloud
4. Chromium Web Store - Keep your web extensions up-to-date
5. Decentraleyes - Cache regularly used files delivered by a Content Delivery
   Network (CDN) to prevent tracking.

If you are an advanced user, you can also install the following extensions:
6. uMatrix - Similar to uBlock Origin but it gives tighter control
7. ScriptSafe - Similar to uBlock Origina and uMatrix but with a different
   philosophy
8. Vytal - Control trivial features that are used to generate unique
   fingerprint from your browser such as timezone.
   
However, a few days ago, the best VPN provider, Mullvad VPN along with the team
behind the Tor Browser has launched a tweaked version of Firefox Browser. This
browser, called [Mullvad Browser](https://mullvad.net/en/browser), generates a
single fingerprint for all users, making it difficult to track you across the
web.

Note that the browser-default synchronisation is disabled in those browsers.
For better privacy, you should synchronise your bookmarks using a browser
extension such as the one specified above. Also, never save your passwords in
the browser-default password manger. Every interested person knows where those
passwords are located.

## Secure Your Logins
Securing your login details is something you should do even when you don't care
about privacy. Because this might help you avoiding a lot of griefs due to your
weak security measures. As you may already know, for better security, it is
necessary to use strong and unique passwords for every account you create along
with two- or multi-factor authentication. Managing unique passwords is not
something you can do using your memory alone, you need a password manager.
Depending on what you need, you can choose [BitWarden](https://bitwarden.com/)
or [KeePassXC](https://keepassxc.org/)/[KeePassDX](https://www.keepassdx.com/)
as your password manager. Since you're only getting started, I would suggest
BitWarden since it provides a better flexibility than the others. For
authenticator, never use outdated, insecure and closed-source providers such as
Google Authenticator or Authy. Instead use well-known open source alternatives
such as [Aegis Authenticator](https://github.com/beemdevelopment/Aegis).

If you are already using a password manager such as Google or Lastpass, you
should immediately migrate to a better and privacy-friendly alternative.

## Secure Your Phone
If you use a smartphone, it's essential to secure it properly in order to
achieve both privacy and security. First of all, check if your existing phone
is enough for you. If the phone does not receive regular updates or is not
from a reputed company, it may not be a sutiable phone, and if you afford it,
you should upgrade your phone so that you can use a secure operating system
such as [Graphene OS](https://grapheneos.org/). Otherwise, you should uninstall
all the unnecessary system applications from your phone.

Secondly, make sure that the device is encrypted. When it's possible, the
encryption password should be as long as possible. Avoid using insecure
security features such as fingerprint or face ID, and use pin or password.

Thirdly, replace the closed source apps with good and trackerless open source
alternatives. While this may not improve your security, it will improve your
privacy. Here's a [list of apps that I frequently use]({% post_url 2022-12-30-android-apps-that-i-frequently-use %}) 
which may help you getting started. 

## Be Clever, Consume Less
Less consumption is freqently associated with economic and health benefits. But
it plays an important role in achieving privacy, and it, sort of, answers the
question as to why companies want us to consume more. By displaying advertises
appealing to you, the big companies want you to consume more because ads are a
good source of revenue for them. Through social media, they also induce people
to show themselves off so that you, fearing of being missing out, would imitate
them and start consuming all those useless things you are trying to keep
yourself distant from as it is well-known that these needs, though may provide
temporary happiness, are the cause for depression in the long run. Instead of
going after temporary happiness, I think, we should sought for things that give
us a more permanent happiness. I am not a psychiatrist, but I found that
reflecting on your deeds and beliefs, that is, self-judgement, is a powerful
tool to gain long term happiness as you start to understand yourself better
this way and what you really need, as opposed to the ones imposed on you
through the “induction” process above.

## Obliviate Yourself from the Internet
This could the most tedious task depending on how interactive you were. If you
were like me and used a lot of sites carelessly, you will need to do a lot of
things to wipe youself from the Internet. When I first started to wipe my
online activities, it was quite difficult thing to do since a lot of services
did not offer a way to delete an account or profile. But nowadays, it is quite
easy as they have to oblige various policies around the world regarding data
retention and privacy. These services can work even if you're not located in a
country with such laws. However, some services might not entirely delete your
data or claim to delete your data while all they did was made it private. In
both cases, if there's an account involved, you might want to keep it in your
password manager to check whether you're account is still present a few years
later. But even if they made the data private, it should be enough to keep the
search engines from indexing your data which should be your primary concern.
Because OSINT (open source intelligent) experts and data brokers primarily use
various search engines with special keywords (e.g. Google dorks) to collect
data about you.

## Keep Informed and Inform the Family and Friends
The only way to effectively achieve total privacy is by spreading privacy
awareness among the people you care about. This is because the importance of
privacy is not immediately clear to people, even to those who are new to all
this. If you're the latter, at first ask yourself why you're here. This should
get you started. Another important thing is keeping yourself informed about
what is happening around you. Accept it or not, you're now a member of an
extended economic society which some poeple calls “Global Village”. The
Internet is not created for you to watch some movies or play games, it was
created for speeding up the communication which are vital for economy and
defence. So, as member of the society, it's your responsibility to keep
yourself well-informed about events and issues that may affect you or the
people you care about.
