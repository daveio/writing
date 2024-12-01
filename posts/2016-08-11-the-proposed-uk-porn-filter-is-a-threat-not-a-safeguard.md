---
layout: post
title:  The proposed UK porn filter is a threat, not a safeguard
date:   2016-08-11 17:37:38 +0100
categories: []
image: /content/images/2016/08/26280058862_6a20311dd2_o.jpg
slug: the-proposed-uk-porn-filter-is-a-threat-not-a-safeguard
---

I can count the number of times that I've agreed with David Cameron on policy without having to resort to counting. The latest move to come out of the tabloid-courting Conservative government is an opt-out filter â€“ meaning 'enabled by default' â€“ for all adult content, legal and otherwise.

The usual suspects have rallied behind this illiberal idea. The Daily Mail calls it "a victory for the Daily Mail" and "protection for every home". Cameron even namechecks the rag himself.

> "The Daily Mail has campaigned hard to make internet search engine filters 'default on'. Today they can declare that campaign a success."

I'm not going to target the reasons that this is a terrible idea from a sociopolitical standpoint. [Stavvers, over at Another Angry Woman, has done it better](http://stavvers.wordpress.com/2013/07/22/not-that-porn-blocking-bollocks-again/ "Another Angry Woman: Not that porn-blocking bollocks again"). What I am going to cover is the details of the filtering that is already in place (and has been for some time now), and the technical reasons why a filter like this will do more harm than good.

## We already have a child abuse filter

The [Internet Watch Foundation](http://www.iwf.org.uk/ "Internet Watch Foundation") serves two purposes. Firstly, it provides a clearinghouse for reports of child abuse content online, and secondly, it produces a list of sites hosting such content, which is used by an existing filter called [Cleanfeed](http://en.wikipedia.org/wiki/Cleanfeed_(content_blocking_system) "Cleanfeed (content blocking system)") that is used by most UK ISPs.

It's far from perfect. The most memorable false positive was the blocking of a Wikipedia article about the Scorpions' album *Virgin Killer*. The cover art features a nude ten-year-old girl, with her genitalia obscured by a shattered glass effect. Whether or not you believe that's acceptable, it is not illegal content. The IWF felt otherwise â€“ that there were erotic undertones â€“ and classified it as 'erotic posing with no sexual activity'.

Wikipedia editors are nothing if not obsessive about their subject matter. It didn't take long for someone to notice, and the IWF removed the image from their list three days later.

Cleanfeed, in collaboration with the IWF, is already a default-on filter for child abuse content. Whether you're in favour of it or not, it exists, and has been active since 2004.

## Filters can never be perfect

Whenever you use an automated system (or even a human system) to process data, you will get errors. Entropy can't be eliminated. What you can do, however, is change the design of that system to eliminate or enormously reduce false positives or false negatives. Importantly, you have to pick one â€“ you can't have both.

If you're building a car alarm, you want to favour false positives. A false negative could result in the car being stolen, and a false positive could result in the car owner having to get out of bed to disable it. Favouring false positives and reducing false negatives enhances the system.

On the other hand, there are times that you want to favour false negatives. Consider an automatic gun turret that supports other armed guards. If the gun turret fails to identify an attacker and as such does not fire, the armed guards are still around to deal with the situation. If, however, the gun turret identifies a friendly guard as an attacker and fires, it will kill them.

Internet filters usually filter favouring false positives, due to the huge, varied, and constantly increasing number of ways to evade filtering. A false negative will let the content in question through, whereas a false positive will block it.

Let's consider the various types of filter, and why a filter favouring false positives that you have to explicitly disable is a bad idea.

### Image and video content filters

These are the smartest filters around. Rather than working on a list of known illegal content, they can analyse an image or video and make a fairly decent guess about what it contains. The simplest example of this is looking for the ratio of skin tones to other colours â€“ adult content usually has naked people in it, resulting in a much higher ratio.

This is flawed for the simple reason that nudity is not inherently adult content. Art nude paintings, photography, and cinematography will also trigger this type of filter. Sex education material suffers the same fate. Even photos of patches of skin, for example medical illustrations, will trigger it.

### Text content filters

These scan the text of the resource being accessed for keywords. They can either operate by blocking if a single 'bad' keyword is found, or by analysing the ratio of 'bad' keywords to 'clean' text.

We again run into problems. Medical textbooks will trigger this kind of filter, as will a lot of literature that involves sexual activity or discussion. Sex education resources have no chance. LGBT community and activism, along with rape survivor resources, have a long history of falling foul of text content filtering.

### URL filters

These web-only filters scan the address of the resource being accessed. Usually they'll be matched against a whitelist (anything not explicitly allowed is blocked) or a blacklist (everything not explicitly blocked is allowed). Cleanfeed uses this as one of its two filtering methods, operating in blacklist mode.

Operating such a filter in whitelist mode would be completely impractical for what's being proposed, so let's focus on the problems with blacklists. The short version is that they're actually pretty good, if the people building the blacklists are honest and attentive â€“ unfortunately, they're extremely labour-intensive and as such expensive to maintain, so the quality slips and material that shouldn't be included makes its way into the blacklist.

### IP filters

These operate similarly to URL filters, and is the second filtering method used by Cleanfeed. Instead of blocking a page, or an image, or a video, the entire site is blocked. They operate in whitelist or blacklist mode as mentioned in the **URL filters** section above, and suffer from the same problems.

## People won't understand how to opt out

Not everyone has technical ability. Many users, when presented with a 'this content has been blocked' message (or, in Cleanfeed's case, a false 'not found' error message) won't know what to do. Falsely blocked material will therefore be unavailable to them â€“ and, as we've discussed, that will include innocent content and content that it is very important that certain people (LGBT people, rape survivors, and similar) *can* access.

## 'Opt-out' gives away compromising information

A system in which you have to opt in allows the organisation managing the filter to know that you want content filtering. The implications of this are perhaps that you have children, or you simply don't want adult content appearing as you browse. Nothing sensitive.

In contrast, a system in which you have to explicitly opt out of tells the same organisation a far juicier detail â€“ you consume adult content. Of course, it might not be adult content, but that's irrelevant. That kind of socially compromising information has a long history of being abused, and in the situation of a future far-right-wing government having access to that information, your liberty is immediately threatened.

As an example, O2 and Vodafone have an opt-out filter for adult content on their mobile web platform. What proportion of the customer base impacted by it have disabled it, do you think? Your options are to make a payment from a credit (not debit) card, or visit a store with identification and ask someone face-to-face. Fortunately, I'm rather shameless, but this kind of embarrassment-based social pressure is the kind of crap that we tried to leave behind with the Victorians.

## It won't work

The Internet was originally designed to provide a communications network that would survive a nuclear assault. It routes around damage, and it sees censorship as damage. The people who want to share truly reprehensible material will continue to be able to do so. I won't go into detail, but I can immediately think of four different ways to achieve this (and there are more) that would be unaffected by any kind of filter based on anything but a whitelist â€“ and, as I mentioned earlier, a whitelist is completely impractical for a nationwide filtering system. It's pretty impractical for even a family-wide filter.

## Filtering technology itself does not care what it's filtering

If you can filter one category of content, you can filter another. With this system in place, an authoritarian government would be able to filter anything they chose. We already see this in China â€“ opposition politics, political satire, anything that is decided to be 'undesirable' can be blocked.

## Any filtering technology is always also monitoring technology

Filtering technology requires interception and analysis of communication. Co-opting this platform to inspect and monitor the same communication is trivially simple. You wouldn't stand for a government that opened all your post, so why would you stand for this?

## Don't be fooled

This is a move designed to court the tabloids and gain votes. It will harm people. No matter how much the language is couched in justifications of 'protection', remember that it is a move that will be inordinately expensive, has a huge number of unavoidable drawbacks, and does not provide any significant improvement over what we already have in place â€“ so it's unfit for purpose, too.
