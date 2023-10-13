---
layout: post
title: "An introduction to threat modelling"
description: "Threat modelling your life: scope, threats/risks, actions with satisfaction and philosophy"
date: 2023-10-13T00:12:58+06:00
tags: Privacy
comment_id: 5
---

<small>[This article is intended for those who want to apply threat modelling
in their virtual and real life. If you're a developer trying to devise a threat
model for your project, this article may not going to help you much. Instead,
you might want to start from the OWASP's community page on
[threat modelling](https://owasp.org/www-community/Threat_Modeling).]</small>

People say a relationship is built on trust. Sure, there are a lot of other
elements to it such as mutual respect, security, brain chemistry, but trust
ultimately defines them all. Because it's quite difficult to regain trust once
it is lost. Trust is our vulnerability, and whoever exploits the vulnerability
is the ultimate villain who can never be forgiven.

But our perception of trust, when comes to the things that aren't important to
us or do not directly affect us, is somewhat vague. Take social media as an
example (or even politics, for that matter). Many spend hours after hours on
social media without thinking about how those feeds are continuously generated,
unknowingly putting their trust on algorithms developed by big corporations
whose primary purpose is the maximisation of profits regardless of the nobility
of the means. In politics, we somewhat randomly choose to trust or distrust a
political party or a candidate because it's a game of the elites anyway. Modern
society is very complex, and it is thought that the evolution of our brain is
not fast enough to keep up with it, and this is probably why our list of
priorities have become so big that we often need to prioritise priorities
themselves, and all those indirect stuffs seem to find their way at the bottom
of the list. Hence, we never really get a chance to do something about them
while knowing quite well that we cannot live without them and that we should
seriously think about them.

Enough philosophy for one day, you may ask. But understanding the priorities is
the most important thing in our life, and “understanding the priorities” is
threat modelling.

## Life's full of threats

<blockquote>
Most people blunder around this city and all they see are streets and shops and
cars. When you walk with Sherlock Holmes, you see the battlefield. You've seen
it already, haven't you?
<footer>Mycroft Holmes, <em>Sherlock</em></footer>
</blockquote>

When nobody is at home or when everybody is going to sleep, you must lock the
windows, the main door or gate properly to avoid being theft. Even then,
certain household items such as jewelries may need extra protections. Your
phone might be protected with a pin/pattern or biometric lock to prevent
other people from viewing things that are private to you. You may have also
installed location tracker or other anti-theft applications to find or remotely
wipe your device if you somehow loose it. Similarly, other devices you own such
as computer, smart devices, etc. may also be protected with pin or passwords to
prevent others from gaining access to those devices. If you're driving, you may
limit your consumption of alcohol or drugs so that you can drive properly. If
you work, you may set alarm multiple times when you sleep late. If you're going
on a vacation, you may start listing everything you're bringing with you days
before the final date in order to avoid missing anything.

Everyday in our life, we do things like the ones I've mentioned above. In each
example, there was a *scope*, there were existing *threats* or *risks*, and we
somehow needed to mitigate those by taking some *actions* (precautions) or
*measures*. These actions or measures are not arbitrary, however. We choose
them exclusively so that we're *satisfied* with the results. In the first
example, the scope was your household, the threats were thieves and burglars,
the risks or vulnerabilities were windows, main door or gate, etc., and the
measures were locking them properly and providing some extra protections for
precious items to meet your satisfaction. In the second example, the scope was
your phone, the threats were basically everybody else who knows how to use a
smartphone, the risks were your private data and usage statistics, and the
measures were protecting the data with a pin or pattern as well as biometric
lock. Now, not everybody might be satisfied with a biometric lock because
biometric lock requires fingerprint or face-scanning which are easy to obtain
by some adversaries (or threats).

What you've just read is actually threat modelling. It's nothing new or fancy.
We all do this, only we didn't know what it is called. And as you might have
guessed from above, threat modelling involves four things:

1. Finding the scope
2. Identification of threats and risks
3. Identification of actions or measures to manage the risks
4. Evaluate the work done.

So, from now on, every decision you make, you can note the first three things
and evaluate your work (and repeat until you're satisfied). This note does not
have to be written and proper. You can do it in your mind too. But one thing
should be noted that indentification of threats and risks plays the most
important role in threat modelling since all the actions or measures you take
will be based on those threats and risks. Also, a scope may have sub-scopes
(like in the first example where precious items fall under a sub-scope), and
each sub-scope may have a different threat model than the parent scope. This is
perfectly okay. You only need to ensure that you're satisfied with everything
you've done.

## Satisfaction is not cheap

<blockquote>
Life is pain, Highness. Anyone who says differently is selling something.
<footer>Pirate Roberts (Westley), <em>The Princess Bride</em></footer>
</blockquote>

Identifying the scope seems easy because every decision always comes with a
scope. But what about the others? For example, identification of threats and
risks seems easy when it comes to protecting your smartphone, or does it? Sure
we have considered anyone with the knowledge of smartphone to be a potential
threat, but we haven't actually defined the risks, such as hacking or cracking
either physically or via the Internet, unattended access by someone you know,
loss of data due to theft or operating system upgrade. As you have identified
new risks, you need to adjust the actions or measures taken earlier. For
example, earlier you've only used pin/password or biometric lock which is not
enough to mitigate the newly identified risks. You need some additional
measures, such as using a secure router with an up-to-date firmware, using a
VPN in an untrusted network, investigating an app before installing it, using a
timeout for lock, using a secure browser, backing up data, using device
encryption, etc. But then, you also need to ensure that you're not being
paranoid by overdoing things, such as considering unrelated or impossible
things as risks, or mitigate risks using a way that is harmful for you or the
people around you. For example, if you cannot afford a Pixel phone to use
Graphene OS, do not sell one of your kidneys to buy one. Instead, devise a new
threat model that might be applicable for a phone that you can afford.
Similarly, if you cannot manage an invitation code for Riseup email, you may
not actually be eligible for one and try other alternatives instead of
bothering other people whom you've never met.

But where do all these knowledge come from? And how do you evaluate your new
model so that you don't miss out or overdo things? Satisfaction, after all, is
not something one can easily achieve.

In beginning of [my last article]({{ "" | relative_url }}{% link _posts/2023-04-07-migrate-to-privacy.md %}),
I've said three things about privacy: one, you cannot see privacy-related
contents unless you're actively looking for it, two, they're not taught in
schools, and three, they harm corporations and governments. When I said it, I
didn't imply all three of them to be correlated or that the former two things
are caused by the latter, because there are a lot of things at work here. The
reason I've rephrased them here is because they can help you answer these
questions if you think it through. For example, since privacy is not taught in
schools, it's necessary to understand what privacy and security (the previous
article was mostly about privacy, but this article is applicable to both
privacy and security) actually mean before doing anything else. This you can
do by looking up these terminologies specifically, and when you do this,
continue looking up until you're convinced that you've understood these
terminologies. This you can ensure by attempting to answer questions like “What
is privacy?” or “Why is privacy essential?”. I can very well link a few
articles here, but I won't. Because it's necessary that you develop an
investigative mind. This is useful not only for privacy or security but also
for almost everything you do. With the advent of artificial intelligence,
disinformation and conspiracy theories can be quite convincing, and having an
investigative mind will prevent you from believing everything you see, read or
install. The five senses are a vital part of our body, but they're also our
vulnerabilities actively exploited by people around us. So, it's necessary that
we develop skills to defend them.

After you're convinced that you've understood the meaning of privacy and
security, it's time to actually learn something about them. However, before
going into details, you should note that learning is a continuous process, and
there's no way you can learn everything in a few weeks or so. A good place to
start learning about privacy and security and what you can do about them is
Electric Frontier Foundation's <a href="https://ssd.eff.org/" rel="noreferrer">
guides on surveillance self-defence</a>. While the guides offer no specific
threat model, they are useful for learning and getting yourself acquainted with
various concepts and keywords which are what you need to get started. After
all, you need knowledge before you can devise any threat model at all. While
reading one of the guides, you may find some concepts and keywords quite
difficult to understand. If this is the case, use your investigative mind to
look them up and understand those things yourself. Use forums or groups as the
last resort, because unfortunately, good advices are difficult to find in those
places, and most advices are highly opinionated (which is understandable,
because people in those places judge you or your question by their own
perspective or threat model. Only somebody with working experience can truly be
able to understand you and give an answer you're looking for, but those people
usually avoid forums because of the sheer number of spamming done in the
pretension of helping the questioner which they cannot). While you're learning,
you can also devise your threat models as an exercise and adjust them as you
learn new stuffs. The adjustment process, as indicated earlier, is a continuous
process just like learning, and therefore, you can never stop learning nor
adjusting. A second source of information is the online news portals. Websites
like news.ycombinator.com, ghacks.net or thehackernews.com could be quite
useful in keeping yourself up-to-date with the latest privacy and security
issues, and, thereby, helping you adjust your threat model. If you cannot
afford to keep yourself up-to-date, you need to devise a threat model where you
spend less time on the Internet or smart devices. Because both are evolving
constantly, and your inability to keep up with them will be your greatest
vulnerability. However, when you'll begin to take actions, you'll start to
discover something else, something which may turn out to be quite painful to
handle.

## Handling the aftershock

<blockquote>
You see? Life. Yes, life’s [a] sentence. So what? I will do what needs to be
done, even if they hate me or love me. You have to be solid so that it makes
no difference what they think.
<footer>Ivan Locke, <em>Locke</em></footer>
</blockquote>

In the previous article, I've talked of seeing the real character of people
around you after you achieved some level of privacy. The reason behind this
revelation is often quite simple: When you adopt a threat model with best
privacy and security practices, you become too much work. That is, you avoid
the typical or popular means of communication, you are suddenly seen making
more logical decisions than expected or becoming more skeptical about things
that are considered trivial, which make it quite difficult for them to keep up
with you and force them to stop pretending to be something they are not. This
could very well be proven as the most shocking thing you've ever come across in
your life, especially, if you're fond of company. Also, the very thought of
sacrificing your friendship for privacy and security may force you to put both
in a scale to decide which weighs more. This is not the only issue. You may
find yourself ineligible for certain jobs only because your threat model put a
moral embargo on your applying for such jobs. This could be frustrating if job
opportunities are scarce in your area, or the job is one of your *dream* jobs.
Depression, at this point, may surround you like darkness in a forest. But if
you think carefully, you'll soon find that the issues above are only threats
that you forgot to consider when you decided you threat models. And the reasons
you didn't consider them earlier were that they were not immediately visible to
you, and unfortunately, there exists hardly any guide that speaks of these
threats. Threat modelling is primarily used in the fields of computer science
and engineering, therefore, when the writers write about threat modelling for
common people, they tend to use their understanding of threat modelling from
that perspective and neglect the additional consequences of it on human mind.

Since these threats are never discussed broadly, I shall share some of the
strategies (ie. measures or actions) that I have followed in my life. Depending
on your situations in life, they might be different, but these should give you
some hints.

### People who value you will follow you

Those who can use social media or instant messengers can also use or switch to
a different one for the sake of communicating with you. If someone does not
want to migrate from WhatsApp to, say, Signal, it's probably time to reevaluate
your relationship with the person. But there is also a high chance that the
person is ill-educated in regards to privacy and security, in which case, you
have the responsibility to educate them on those topcis. However, if the
person, despite having a good knowledge and understanding of privacy and/or
security, still refuses to respect your privacy, they may not simply worth the
effort. If someone is upset because you lock your door, they may not be your
friends.

### Getting rid of the fear of missing out

This is basically getting rid of the feeling of being miserable because you're
no longer a part of _the herd_. If you're addicted to social media, fear of
missing out (FOMO) will prevent you from moving away from those platforms.
Getting rid of the addiction is quite difficult but not impossible. First of
all, you need to reduce the your activities on social media. This involves
three main things: 1. Reducing the amount of posts you share social media,
especially, the ones involving your personal activities, 2. reducing the screen
time for those platforms, and 3. reducing interactions. In Facebook, for
example, you can use the JavaScript-less mbasic.facebook.com to browse Facebook
uninstalling any Facebook apps you have in your phone or PC, and abstain from
liking or commenting on any posts. Secondly, start unfollowing people who are
already present in other privacy-friendly or federated alternatives and start
following them on those platforms instead. For example, unfollow celebrity
profiles and the like from Facebook or Twitter if they have profiles in
Mastodon. Thirdly, start unfollowing people who do not matter to you. This may
include famous celebrities whom you follow only for entertainment, your
neighbours with whom you never talked more than two lines in the past few
years, or your “friends” or “relatives” whose attitudes do not display any sign
that might indicate that they still care about you. Fourthly, spend some time
outside, preferably, without your phone but definitely without any internet
connection. Maybe half an hour of walking or simply sitting somewhere thinking
about something interesting or reading an interesting book, newspaper or
magazine. The joy of spending time in the real world may not immediately be
realised, but gradually, you'll start to feel what you were missing. Fifthly,
if you are fond of company, arrange parties where phones aren't allowed. It's
simply pointless to join a party where nobody talks because everybody's busy
with their phones. Finally and the most important of all, build a personality.
I believe that the primary reason for somebody to be affected by the activities
of others is the lack or inferiority of their personality. So, building a good
personality will ensure your indifference to the activities of others. Note
that this does not mean you will remain constant and not adapt or accept
changes (on the contrary, learning to adapt quickly is a very important step in
a threat model as it should be clear from the previous section).

### Simplicity is the key

As I've stated in my previous post, consuming less is beneficial to our body
and mind (well, if you're the an executive of a company which needs more
consumers, this may not be applicable to you). It can be beneficial for your
bank account or credit card, too, if you're low on money. In developed world,
loans were made trivial by the use of credit cards as they have learned to
buy an item without looking at the price tags (we can all see how credit card
debts have been steadily increasing in the USA). In developing countries, banks
are trying to popularise credit cards for the same reason, but they're still
quite behind. In underdeveloped countries, microcredit is the ultimate debt
trap that everybody in the developed world seems to be praising. You might
argue that credit cards give a lot of offers, but where do the offers come
from? And would you really need to buy all those products in first place?
Leading a simple life reduces your need, your _want_, and your urge to showoff
yourself to the rest of the world. Spending money on these things brings
nothing except depression, sorrow and the urge to do something stupid (such as
committing suicide). Today, the leading causes of death among the population of
USA between the age 18 to 30 are drug abuse and suicide. This is the state of
one of the most developed countries in the world. Uncontrolled capitalism and
lack of ideology has made people lonely, depressed and desparate. And people
are ready to do anything to prevent those feelings, and they choose the vicious
cycle of consumption thanks to the efforts of the companies who were
successfully able to motivate people to do so. Only developing a personality
(that is, an ideology) and leading a simple life can be able to help you with
those issues. Loneliness is not a bad thing, neither is depression. Everyone in
their life encounters them but we only need to learn how to handle them without
being desperate. When you have a strong personality, you develop the capability
to keep yourself calm, and by leading a simple life, you reduce the frequency
of encountering those things. This is the ulitmate threat model of your life
that can define them all.

I'll end this article by sharing a dialog taken from the drama “Detachment”:

<blockquote><p>
Henry Barthes: “How are you to imagine anything if the images are always
    provided for you? Who here read 1984 last year? [A few raise hands] Good.
    [Writes ‘Doublethink’ on the blackboard] Anyone?”
</p><p>
Meredith: “Having two opposing beliefs at once, and believing that both are
    true.”
</p><p>
Henry Barthes: “Excellent, Meredith. To deliberately believe in lies while
    knowing they’re false. Examples of this in everyday life: Oh, I need to be
    pretty to be happy, I need surgery to be pretty, I need to be thin, famous,
    fashionable. Our young men today are being told that women are whores,
    bitches, things to be screwed, beaten, shit on, ashamed. This is a
    marketing Holocaust, 24 hours a day for the rest of our lives, powers at
    be, are hard at work dumbing us to death. So, to defend ourselves and fight
    against assimilating this dullness to our thought processes, you must learn
    to read, to stimulate our own imagination, to cultivate our own
    consciousness, our own belief systems. We all need these skills to defend,
    to preserve our own minds.”
</p></blockquote>
