---
layout: post
title:  After the closure of Lavabit, don't look for an alternative
date:   2016-08-11 17:37:48 +0100
categories: []
image: /content/images/2016/08/26171461423_23c0cd67b9_o.jpg
slug: after-the-closure-of-lavabit-dont-look-for-an-alternative
---

Having made the news by being used by [Edward Snowden](http://en.wikipedia.org/wiki/Edward_Snowden "Edward Snowden"), the hosted secure email service service Lavabit has been forced to shut down. In a statement now available on [the Lavabit website](http://lavabit.com/ "Lavabit"), its creator said â€“

> I wish that I could legally share with you the events that led to my decision. I cannot. I feel you deserve to know what's going onâ€“the first amendment is supposed to guarantee me the freedom to speak out in situations like this. Unfortunately, Congress has passed laws that say otherwise. As things currently stand, I cannot share my experiences over the last six weeks, even though I have twice made the appropriate requests.

Obviously, Lavabit's actions are laudable from a privacy viewpoint. They were offered a choice between handing data over or shutting down, and chose the latter. The service was well-built, but it suffered from one unavoidable and critically important issue â€“ it was a trusted third party, which is a great big flashing danger sign to crypto / privacy geeks.

## HushMail: when trusted third parties go bad

HushMail was the original attempt to provide strong cryptography in a web-based email service. It used a Java applet to perform cryptographic operations, with an encrypted private key stored with HushMail. All well and good, until you realise that [HushMail started serving a backdoored version of its Java applet to certain users when requested by a court order](http://www.wired.com/threatlevel/2007/11/encrypted-e-mai/ "HushMail backdoor"). Their crypto was solid, unless you were served the intentionally broken Java applet, at which point your data was no longer secure. Admitting to this was laudable, but there's a clear message: trusted third-parties can rarely, if ever, be fully trusted.

## Lavabit, but better

Lavabit offered two separate points of value to its users â€“ privacy and security. Privacy, in that it was difficult to link a user to an actual human, and security, in that cryptography and good key management was used. Unfortunately, from a privacy perspective, it was all too easy to link a user to their IP addresses and/or billing information, and from a security perspective, key security was impaired by the nature of being a hosted service. We can look at privacy and security separately, and consider how to achieve what Lavabit achieved, except more successfully.

## Better privacy

Communications with Lavabit were sent over the open Internet, using SSL/TLS for transport encryption and authentication. SSL/TLS relies on trusted third-parties for authentication, which [has resulted in fraudulent certificate issuance](http://www.scmagazine.com/experts-weigh-in-on-comodo-ssl-certificate-fraud/article/199109/ "SSL certificate fraud") in the recent past. For a governmental attacker, fraudulent SSL certificate issuance is quite achievable, meaning that you can't be 100% certain that you're talking to the real Lavabit. The good news about SSL/TLS encryption is that it's pretty solid, though; authentication issues aside, the crypto is reliable. So, what to do? Self-management isn't an option when you're after privacy and anonymity. Some kind of hosted service is necessary.

[alert-warning] Suggestions for privacy-respecting email services have been removed, after the Freedom Hosting shutdown. Admittedly, Freedom Hosting was a hotbed of some truly reprehensible content, but it also hosted a service that was previously my best suggestion. [/alert-warning]

## Better security

Lavabit rolled encryption in with its email offering. While this was convenient, it meant that your private key had to be held on their end and decrypted by your passphrase. There's a huge difference between brute-forcing a passphrase to a known 4096-bit key, and brute-forcing an unknown 4096-bit key itself.

### Own your keys

The necessity of a hosted service for privacy and anonymity means that it's much better to keep encryption separate. The de facto standards for strong email encryption and strong IM encryption involve managing your own keys.

### GnuPG: strong email cryptography

[GnuPG](http://gnupg.org/ "GnuPG") is an open-source crypto suite based on PGP, and is reliably strong. It can be a bit daunting to get started with, but the payoff is enormous. A guide is somewhat out of scope, but it's something that I'll be posting about soon. In the meantime, Windows users should check out [Gpg4win](http://www.gpg4win.org/ "GnuPG for Windows"), Mac OS X users should investigate [GPGTools](https://gpgtools.org/ "GnuPG for Mac"), and Linux users should have a look through their package manager for command line packages and hassle-saving frontends.

### OTR: strong IM cryptography

While [GnuPG](http://gnupg.org/ "GnuPG") can be used for IM crypto, something more lightweight is more suitable. [OTR](http://www.cypherpunks.ca/otr/ "OTR cryptography") ('Off The Record') is the standard that has emerged. It's supported by nearly every multiprotocol client ([libpurple](https://developer.pidgin.im/wiki/WhatIsLibpurple "libpurple")-based clients such as [Pidgin](http://www.pidgin.im/ "Pidgin") and [Adium](http://adium.im/ "Adium") come heartily recommended). Alongside encryption and authentication, OTR offers both perfect forward secrecy and deniability after the fact.

## Use private and encrypted communications for everything

Traffic analysis, the art of inferring information about communication from the flow of communication itself rather than its content, is surprisingly effective. Encrypting only important communication is a dead giveaway of an interesting target. Encrypt as often as possible, even if you're just sending pictures of cats to your mum. It makes an attacker's job a lot harder.

## Avoid shortcuts

Services such as Lavabit are tempting because of the low barrier to entry, compared to managing your own encryption and sneaking around with Tor or remailers. Unfortunately, with privacy and security, 'easy' usually means 'less effective'. Quite simply, investing a bit of time in getting yourself set up will result in better protection â€“ both for you, and for the people that you correspond with.
