---
layout: post
title:  "A Q&A on the Metadata Retention Laws"
date:   2015-03-30 17:41:00
description: A brief Q&A on the new laws passed.
categories:
- security
- privacy
permalink: metadata-retention-qa
---

I figured a lot of people would have no idea what the new Australian metadata retention laws mean, so I thought I'd write an FAQ on it. For those of you that are very technical: I've simplified it quite a lot for consumption by the average person, so apologies in advance.

***

**Q. What changed?**

**A.** The government is now tracking pretty much everything you do, including:

* Details of any phone calls you make/receive and the time/location you are when you make them

* The IP address of any websites you visit, or any sites that you communicate through

* Details of any emails that you write to people that go through ISP servers (ie. if you're using an @iinet address, rather than @gmail)

* Your real-time location, if you're carrying your phone

* The internet address you're using to access the internet, at all times

All of this data (and more) is kept for a minimum of 2 years, starting 2017.

***

**Q. I don't do anything wrong, why should I worry about this?**

**A.** The current set of laws are pretty small-time, and are designed to be expanded. Even the laws in the current form are pretty radical, though. Here's some examples of stuff they can do:

* Because they're storing real-time locations of everybody, they don't need speed cameras anymore. By tracking your location, they're able to determine your relative speed, so it'd be pretty easy to set up a system that automatically fines anyone that goes over the speed limit.

* If you access your dentist's website to make an appointment and the dentist's site happens to be on the same server as another site hosting child pornography, there's a _very real_ chance that you could be implicated in it. Because they don't store domain names (only IP addresses), they can pretty much just say "IP Address 145.65.45.34 was hosting CP: find anyone that ever connected to it." Because websites share IP addresses for hosting, anybody that's connected to that server is now assoicated to that site - without the associated domain name, there's no way to tell what you were really accessing. When they bust the CP ring, you'll get your door kicked in and arrested for access of child pornography - even though you never did. The metadata "proves" it, though. You'd think this is a pretty small problem, but the same IP address can be used for hosting thousands of sites, and overreach by government departments in similar ways has [knocked hundreds of thousands of sites offline in the past] [offline].

* There's also big problems with placing a massive set of personal data in the hands of ISPs, phone companies and security agencies: they're all massive targets for hacking. Even if you're perfectly innocent and do nothing wrong ever and don't jaywalk, never speed and certainly never mention murdering people, there's a pretty good chance you're going to get screwed over when one of these databases gets popped. Plus, the government [doesn't have a great track record on this] [diac-breach], or even in [trying to keep the personal data of G20 leaders private] [g20-breach]. Not to worry though, it's usually going to be the ISPs keeping your data safe, such as Optus ([who were recently breached, too] [optus-breach]), or Telstra ([also breached] [telstra-breach]).

* Data storage on a large scale like this always has unintended consequences. Data mining is something of a mystic art, and we constantly find new ways to use old data. Data to this level of detail, kept for such long periods of time, over such a large percentage of the population? I'm literally salivating, and that should terrify you.

* There's some definite potential for collateral here. It'd be relatively easy for somebody to trick people into clicking on links to flagged sites containing terrorism-related material, and flag them for automated investigations. I imagine there'll be a bunch of attacks related to HTTP request echoing that could flag innocent people, as well.

***

**Q. But at least this wide-scale monitoring is being used to stop terrorists, paedophiles and criminals, right?**

**A.** Well, no. The level of technical expertise needed to completely defeat the metadata retention regime is extremely low. Using a VPN (a security tool commonly used by companies, banks, everybody) defeats it. Using end-to-end encrypted chat also defeats it (very easy). Connecting to internationally-based relay servers effectively defeats it. Using gmail or MSN/Hotmail/Live/Outlook.com defeats it. Using Skype, MSN, Facebook Chat, XMPP defeats it. Using iMessage or Google Talk defeats it. Being in a public cafe and using their wifi defeats it. Being in a library defeats it. Using your work internet defeats it.

Effectively, no terrorist or criminal network will ever be dumb enough to fall under the scheme, and the ones that are dumb enough would've been caught without the laws. Paedophiles are already extremely adept at hiding their communications online, and won't be affected (the majority of busts are by getting agents within the circle). 

***

**Q. So.. why are they doing it?**

**A.** Who knows. The copyright industry (movies, music primarily) donated a [literal buttload of cash to the Liberal Party] [donations], so that's probably a good indicator. 

***

**Q. So I can't torrent anymore?**

**A.** Not a good idea. Part of the anonymity behind using torrents previously was that copyright lobbies had difficulty matching the IP addresses that they'd tracked to an actual person, because they needed to subpoena your ISP. As this is one of the key components of what's stored, this is now trivial and can be accessed without a warrant.

When you use torrents, you make 1 + (a lot) of connections. The first is to a site such as kat.ph, in which you download the torrent. The others are to other clients that send you bits of data. It's very easy for a copyright lobby to pretend to be one of these clients and note down everybody that connects to them, which they can then (easily) pass to the metadata db to get a person out of. Once they have that, you're screwed. The maximum fine for somebody like you is $6,600 per offence. Download an album of 15 songs? 15 offenses. Download a movie and the copyright lobbies estimate that people downloaded it off you 300 times? 300 offenses (that's massively dishonest on their part, but they've done it before).

AG Brandis mentioned in the Senate today (26/03) that data stored under this regime can only be used for criminal offences. This is subject to legislative change, however, and you'd have to trust Brandis on that one.

Heh.

***

**Q. Usenet?**

**A.** Use an international SSL news server and an SSL-enabled indexer and you're fine.

***

**Q. So some random AFP guy is now aware that I watch cat videos on youtube?**

**A.** It's not immediately obvious to them, but they can discover it with a small amount of investigation. While ISPs are not mandated to store content or web addresses, they store enough information that it can be worked out.

***

**Q. My phone is a special snowflake, can they still track it?**

**A.** Yes. If you have a mobile phone of any kind, it can be tracked. There's some research to defeat GSM triangulation, but it's limited and it's not been implemented in consumer-grade phones. The only way to avoid being tracked is to leave your phone at home.

***

**Q. Who's to blame for this?**

**A.** The LNP, with the support of the ALP. They both suck. Gasp. 17 out of 18 senate crossbenchers voted against the legislation, including the Greens, Lambie, Lazarus, Leyonhjelm, Xenophon et al. 3 people voted against it in the lower house - Adam Bandt (Green), Andrew Wilkie (Independent), Cathy McGowan (Independent). 

***

Let me know if you have any other questions, on Github, on Twitter (@murodese) or by email: murodese@gmail.com

[offline]: http://www.abc.net.au/news/2014-08-27/asic-accidentally-blocked-250000-websites-ip-address/5701734

[donations]: http://www.itnews.com.au/News/399933,village-roadshow-boosts-donations-amidst-copyright-crackdown.aspx

[diac-breach]: http://www.abc.net.au/news/2014-11-12/immigration-department-breached-privacy-of-9250-asylum-seekers/5885326

[g20-breach]: http://www.theguardian.com/world/2015/mar/30/personal-details-of-world-leaders-accidentally-revealed-by-g20-organisers

[optus-breach]: http://www.itnews.com.au/News/402156,optus-admits-to-three-big-data-breaches.aspx

[telstra-breach]: http://www.theage.com.au/it-pro/security-it/telstra-breaches-privacy-of-thousands-of-customers-20140311-hvh92.html
