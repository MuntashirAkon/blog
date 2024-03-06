---
layout: post
title: "WhatsApp's 2-step Verification can be Futile"
description: "A peculiar story of Denial-of-Service and the reality of buying a SIM card in Bangladesh."
date: 2024-03-06T13:58:10+06:00
tags: Story
comment_id: 6
---

_[I attempted to contact WhatsApp on 17 February, but I received nothing other than a few automated responses. On 2 March, I reported it via Meta where the issue was closed as invalid.]_


My friend, (let's call him) Asad, contacted me in January with an unbelievable story: somebody's hacking into his account in every three days or so. It all started in January when Asad switched his WhatsApp phone number. As the hacker has been frequently hacking his WhatsApp account, it has become difficult for him to stay logged in. A classic Denial-of-Service (DoS) attack.

My first thing that I found curious was that the verification SMS begins with `<#>` and ends with eleven random characters. This usually means that the hacker must have a cloned SIM card installed in his **Android** phone (my friend uses an iPhone) or could be faking both the SIM card and the device using some sophisticated hacking techniques (e.g., having remote access to the device). WhatsApp naturally allows only one primary device. Hence, my friend is being logged out of his device the moment the hacker logs in to his account.

<figure>
  <img loading="lazy" src="{{ 'images/IMG_0140.png' | absolute_url }}" alt="Asad receving SMS from WhatsApp bearing `<#>` which means the SMS is intended for an Android device with the SIM installed in it, but my friend uses an iPhone." />
  <span class="marginnote">Asad receving SMS from WhatsApp bearing `<#>` which means the SMS is intended for an Android device with the SIM installed in it, but my friend uses an iPhone.</span>
</figure>

At first, it was necessary to figure out if the SIM card was cloned. Since he has brought the SIM card only recently, chances are that it might be cloned even before he brought it (not uncommon here in Bangladesh). To eliminate this theory, I've tried all the usual methods to detect if the SIM card has been cloned, but found nothing unusual. I have also contacted the mobile operator who too have not found any issues with the SIM card. Another interesting thing I noticed was that the hacker was unable to log in when WhatsApp chose to call or display the code in the app instead of sending an SMS. So, I figured that the hacker can somehow access the SMS messages. But Asad was logged out of WhatsApp as soon as the SMS arrived, even when he's not connected to the network. How can this be possible without compromising the SIM card or the network? Since re-issuing a SIM card costs money, I chose to explore a bit further.

I later found that the account didn't have 2-step verification enabled, which helps prevent unauthorised logins. So, I enabled 2-step verification and waited a few days to see if the hacker could still log in. Almost three days later, my friend was still logged out almost instantly after receiving a verification code via SMS! I really couldn't believe my own eyes at that point. I've also tried altering the PIN code which is part of 2-step verification. It didn't help at all. This cannot happen due to a compromised SIM card or SMS network, or can it?

<figure>
  <img loading="lazy" src="{{ 'images/IMG_0141.png' | absolute_url }}" alt="Hacking continued even if 2-step verification was enabled in WhatsApp." />
  <span class="marginnote">Hacking continued even if 2-step verification was enabled in WhatsApp.</span>
</figure>

Naturally, I contacted WhatsApp with everything I had at that point, half expecting any response (of course), and within a few minutes, I received an automated response with a few typical AI generated advice. In the reply, I demanded an answer from a human, but it still replied with a new set of advice (a rather dumb AI).

Then, I had an idea. I assumed that the hacker does not know the PIN code. So, they should not be able to actually use the account. This can be tested quite easily. I opened a new WhatsApp account in my device (say, DeviceM) without setting a PIN code (e.g. 2-step verification). Then I installed WhatsApp in another device (say, DeviceR), logged in to the same WhatsApp account (which means WhatsApp on DeviceM was no longer functional) and set up a PIN. Then, in DeviceM, when I tried to log in to the same account, it prompted me to input the PIN after inserting the WhatsApp code that was sent to the device via SMS. I didn't enter the PIN number (assuming that the owner of DeviceM does not know it). What was curious is that WhatsApp in DeviceR was also no longer functional even though the 2-step verification was not completed in DeviceM, and if you wanted to log in to DeviceR immediately, you would be asked to wait for a few minutes to several hours depending on some factors unknown to me. But if you are a clever hacker, you can actually exploit this to run a Denial-of-Service (DoS) attack in the following way:

1. User logs in to WhatsApp using the cell phone number they own in their own device
2. User sets 2-step verification PIN and email (and expects to use WhatsApp as is)
3. Hacker attempts to log in to WhatsApp using the same (and compromised) cell phone number in another device
4. Hacker successfully logs in using the intercepted WhatsApp code sent to the cell phone
5. Hacker gets a 2-step verification PIN prompt but fails to complete the step since the PIN is unknown to them
6. User is logged out of their WhatsApp account immediately when step 4 is completed
7. User attempts to log in WhatsApp again, but since the previous attempt has failed, WhatsApp asks the user to wait for a few minutes to several hours depending on the conditions
8. Hacker follows steps 3–5 in a variable or fixed interval, causing a Denial-of-Service.

I promptly reported my discovery to Meta, but they closed it as invalid because “if a user have access to the victim phone number, they can verify the ownership of phone number and login into the account” without mentioning the PIN and email that could be used for 2-step verification which is solely there to avoid such an issue, nor giving an explanation as to why the user is logged out upon the completion of step 4 instead of step 5.

So, we consulted the mobile operator again with the new information, and we were asked to consult the cybersecurity division of the police department. We, then, went to the nearest police station. They said that this is not yet considered a crime, because there is no evidence that a crime has been committed or a harm has been done. So, I asked my friend to reissue a SIM card which will cause all other cards bearing that number to be unregistered from the network. Asad followed my advice, and so far, the hacker could not hack into his WhatsApp account.

But my question is why Asad? Asad is a jobless individual who barely uses his WhatsApp account. So, my theory, I mentioned earlier, is that Asad must've bought an already cloned phone number. SIM cloning, of late, has become quite popular in Bangladesh for many reasons, such as:

1. To impersonate government officials or businessmen, and ask money from people on their behalf.
2. To hack into individual's social media account (e.g., Facebook and Instagram), and send spam messages to others or ask money from them.
3. To use mobile banking using the hacked number and involve in illicit activities, such as money laundering, betting, stealing or making illegal transactions.
4. To use the phone number for online verification or sell it online in an illegal manner (as many online services nowadays require a physical phone number to register).

Among them, no. 4 is the most likely reason for cloning his SIM card since the hacker only uses it for online verification (e.g., he often receives verification codes from random sites, such as Waky, MarcoPolo) and unable to verify WhatsApp if it chooses to call instead of sending an SMS.

As for WhatsApp, I do believe the above to be a security issue. Because WhatsApp should only log someone out of their app if the 2-step verification is successful in another device (in addition to noting down the suspicious activity).