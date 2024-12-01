---
layout: post
title:  Broken by design and openly sexist - two big reasons to avoid GoDaddy
date:   2016-08-11 17:36:09 +0100
categories: []
image: /content/images/2016/08/17015760108_c40f9a2a44_o.jpg
slug: broken-by-design-and-openly-sexist-two-big-reasons-to-avoid-godaddy
---

GoDaddy is huge. It's the biggest ICANN-accredited registrar in the world, and not by a short margin. The registrar for over 45 million domain names in 2010, it's four times bigger than its closest competitor. GoDaddy is cheap and easily accessible, and it's the first name that many people think of due to their extensive advertising in mainstream media, including the Superbowl.

Its policies are also written by people who are either ignorant, amoral or both.

## Outright Sexism At The Superbowl

GoDaddy has a history of advertising at the Superbowl. The single most watched television event in America, advertising costs for a spot are known in the industry as *fucking bonkers*.

GoDaddy also has a history of thinking that 70s-grade sexism is still okay.

Here's 2009's advert, starring some women with some breasts (and, as far as I can tell, that's the extent of their purpose) -

<iframe frameborder="0" height="345" src="http://www.youtube.com/embed/Uh5fTKI-rQM" width="420"></iframe>

Here's one from 2010, featuring a woman with some truly great aspirations; to have her breasts used to sell domain names -

<iframe frameborder="0" height="345" src="http://www.youtube.com/embed/yJc5RldnzIk" width="560"></iframe>

And they didn't forget about 2011. Hah! The joke's on you! She's old and ugly! Old women are less attractive, which is why it's funny! Hah! -

<iframe frameborder="0" height="345" src="http://www.youtube.com/embed/J83EQ7LubwE" width="560"></iframe>

By now, I think you're probably noticing a theme. Do you really want to support a company that has no qualms about putting stereotype-solidifying crap like this out there?

Maybe sexism's not enough for you. Alright, how about this. *Their services are intentionally impaired.*


## GoDaddy DNS: Broken By Design

When you buy a domain name, it's useless in itself without one or more nameservers associated to it. These servers translate hostnames - like `www.google.com` - to IP addresses that your computer and Internet connection can use, like `62.149.40.4`. Without a response from these servers, when you try to send email, visit a website or access any services on that domain, there is absolutely no information about which server your machine should talk to to get the information.

DNS is important. Without it, your domain name is worthless.

So it came as quite a surprise when R. Scott Perry posted about [an intentional blocking of DNS requests from certain sources](http://rscott.org/dns/GoDaddy_Selective_DNS_Blackouts.htm). GoDaddy claim that this is to protect their users' privacy, and that they're ensuring that DNS records are being "*accessed properly and not being harvested for unintended uses*". There's only one reason to harvest DNS records, and that's so that you can use the services at the domain.

Their press release about the issue says -

> Go Daddy monitors DNS queries to ensure our customers' information is being accessed properly and not being harvested for unintended uses. If we suspect that any service is gathering DNS data, we will limit access to that specific source. This is done to maintain our high level of system integrity. If a company or service has questions about accessing Go Daddy DNS, they can email dns (at) jomax.net.

This sounds a lot like another press release, issued when GoDaddy started to block systems harvesting WHOIS data (which *is* reasonable, as WHOIS data can be harvested for contact details) -

> Go Daddy ... monitors WHOIS data regularly to ensure our customers' information is being accessed properly and not being harvested for unintended uses. If we suspect that any service is harvesting WHOIS data, we will limit access to that specific source. We are not taking the WHOIS information offline, however. Anyone can find the WHOIS information on a domain name registered through Go Daddy by visiting http://whois.GoDaddy.com. If a company or service has questions about accessing Go Daddy WHOIS information, they can email dns (at) jomax.net.

Sounds like someone has either got their technical information mixed up. Or the alternative - that the prices that they charge are so low that they need to cut corners absolutely everywhere, including limiting the traffic to their DNS servers.

This is insidious. Customers affected by the issue will probably see no issue with their sites, but some customers will simply not be able to see their website or send them any email. It's a silent failure that will lose people business.

I've put together a handy flowchart to help you work out whether you should care about this -

![](/content/images/2016/08/godaddy-flowchart.png)

### GoDaddy alternatives

You are not stuck with GoDaddy. Domains can be transferred at any point, and if you don't want to transfer your domains then you can host your DNS elsewhere. I can heartily (and without affiliation) recommend [DNSimple](http://dnsimple.com) for this - it's a paid service but with a corresponding quality of product. For free DNS hosting, you can try [ClouDNS](http://cloudns.net), which I haven't tried but have heard positive reviews of. It's free for up to three domains.

Both of these services provide instructions on switching your nameservers. It's a painless process, and you should do it if you're affected by GoDaddy's bad decision-making and it matters to you that everyone who wants to visit your site is able to visit your site.
