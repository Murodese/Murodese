---
layout: post
title:  "CFH-NS: Web Data Extraction Results and Testbed"
date:   2015-04-16 16:50:00pm
description: Results of the CFH-NS algorithm on web data, and the testbed of links used.
categories:
- data mining
- scraping
- web data extraction
permalink: cfhns-testbed
---

### Results

|---
| URL | AR-P | CFH-NS | DEPTA | AR | DEPTA-L | BUW-L
|-|:-:|:-:|:-:|:-:|:-:|:-:
| http://9to5mac.com/2... | 20   | 13/13     | 10/8    | 20   | 0/0     | 6/6      
| http://bbs.boingboin... | 18   | 18/18     | 6/6     | 18   | 5/2     | 0/0      
| http://clubtroppo.co... | 30   | 30/30     | 25/10   | 30   | 0/0     | 19/11   
| http://games.on.net/... | 13   | 13/13     | 13/13   | 13   | 13/13   | 13/13   
| http://homeserversho... | 60   | 55/55     | 21/21   | 60   | 0/0     | 44/34   
| http://larvatusprode... | 220  | 240/220   | 27/27   | 220  | 0/0     | 220/220 
| http://news.national... | 50   | 51/50     | 15/13   | 50   | 0/0     | 0/0     
| http://newsfeed.gawk... | 42   | 82/42     | 0/0     | 20   | 0/0     | 0/0     
| http://packetlife.ne... | 18   | 12/12     | 10/6    | 18   | 10/6    | 0/0     
| http://pivotallabs.c... | 5    | 5/5       | 16/4    | 5    | 16/4    | 5/5     
| http://submicron.dev... | 8    | 8/8       | 4/4     | 8    | 4/4     | 0/0     
| http://techcrunch.co... | 18   | 10/10     | 0/0     | 18   | 0/0     | 0/0     
| http://theconversati... | 115  | 115/115   | 52/46   | 115  | 0/0     | 111/111 
| http://the-toast.net... | 41   | 26/26     | 0/0     | 27   | 0/0     | 5/5     
| http://www.adelaiden... | 101  | 57/52     | 0/0     | 50   | 0/0     | 0/0     
| http://www.amazon.co... | 3    | 3/3       | 3/3     | 3    | 3/3     | 3/3     
| http://www.autocar.c... | 7    | 7/7       | 6/6     | 7    | 6/6     | 7/6     
| http://www.canonrumo... | 15   | 24/15     | 5/5     | 15   | 5/5     | 26/14   
| http://www.courierma... | 45   | 45/45     | 0/0     | 45   | 0/0     | 0/0     
| http://www.cracked.c... | 592  | 543/543   | 123/123 | 34   | 0/0     | 0/0     
| http://www.crymore.n... | 78   | 109/70    | 55/23   | 78   | 0/0     | 26/12   
| http://www.dailytele... | 72   | 54/54     | 0/0     | 50   | 0/0     | 0/0     
| http://www.destructo... | 219  | 220/219   | 72/72   | 50   | 0/0     | 0/0     
| http://www.dpreview.... | 193  | 205/193   | 72/72   | 176  | 0/0     | 0/0     
| http://www.engadget.... | 4    | 4/4       | 0/0     | 4    | 0/0     | 0/0     
| http://www.escapistm... | 5    | 10/5      | 0/0     | 5    | 0/0     | 0/0     
| http://www.gamespot.... | 24   | 24/24     | 9/9     | 24   | 0/0     | 24/0    
| http://www.gizmodo.c... | 10   | 10/10     | 3/3     | 10   | 0/0     | 9/8     
| http://www.joystiq.c... | 45   | 51/45     | 18/15   |     |         |         
| http://www.kotaku.co... | 23   | 23/23     | 5/5     | 23   | 0/0     | 13/8    
| http://www.layer9.or... | 23   | 23/23     | 0/0     | 23   | 0/0     | 0/0     
| http://www.macrumors... | 10   | 10/10     | 0/0     | 10   | 0/0     | 10/10   
| http://www.macworld.... | 36   | 44/36     | 8/8     | 36   | 0/0     | 0/0     
| http://www.mortgageb... | 2    | 4/2       | 0/0     | 2    | 0/0     | 0/0     
| http://www.neatorama... | 7    | 7/7       | 10/5    | 7    | 10/5    | 5/5     
| http://www.pcworld.c... | 12   | 20/12     | 4/4     | 12   | 0/0     | 9/7     
| http://www.rocketthe... | 10   | 20/10     | 5/5     | 10   | 5/5     | 10/10   
| http://www.rockpaper... | 64   | 64/64     | 16/16   | 64   | 16/16   | 43/18   
| http://www.smh.com.a... | 47   | 47/47     | 25/25   | 10   | 2/2     | 9/9     
| http://www.theage.co... | 545  | 545/545   | 138/138 | 10   | 3/3     | 9/9     
| http://www.tripadvis... | 20   | 20/20     | 0/0     | 10   | 0/0     | 10/10   
| http://www.urbanspoo... | 26   | 22/22     | 6/6     | 26   | 6/6     | 0/0     
| http://www.windowsce... | 27   | 64/27     | 8/8     | 27   | 8/8     | 18/9    
| https://gigaom.com/2... | 9    | 17/9      | 2/2     | 9    | 0/0     | 0/0     
| https://productforum... | 21   | 42/21     | 3/3     | 21   | 0/0     | 0/0     
| https://vimeo.com/98... | 17   | 17/17     | 3/3     | 17   | 0/0     | 0/0     
| https://www.indiegog... | 5    | 5/5       | 12/5    | 5    | 0/0     | 0/0     
| https://www.kickstar... | 50   | 45/45     | 25/25   | 50   | 25/25   | 50/50   
| https://www.ozbargai... | 44   | 44/44     | 12/11   | 44   | 12/11   | 0/0     
| http://www.theguardi... | 86   | 107/86    | 6/6     | 86   | 0/0     | 0/0
|===

### URLs

```
http://9to5mac.com/2015/03/08/apple-campus-2-drone-flyover/
http://bbs.boingboing.net/t/act-now-congress-wants-to-fast-track-the-trans-pacific-partnership/52776
http://clubtroppo.com.au/2015/02/12/stem-part-culture-war-part-cargo-cult-my-latest-fin-column/
http://games.on.net/2015/03/league-of-legends-ai-toxic-players/
http://homeservershow.com/hp-proliant-n40l-microserver-build-and-bios-modification-revisited.html
http://larvatusprodeo.net/archives/2011/01/brisbane-flood-maps-and-up-to-date-flood-information/
http://news.nationalgeographic.com/news/2015/03/150302-black-hole-blast-biggest-science-galaxies-space/
http://newsfeed.gawker.com/terror-owl-gleefully-tearing-apart-its-victims-in-the-1688525383/+jparham
http://packetlife.net/blog/2014/nov/18/mac-address-aggregation-and-translation/
http://pivotallabs.com/rspec-elasticsearchruby-elasticsearchmodel/
http://submicron.deviantart.com/art/Soulsequencer-Series-Hemocyte-Green-481438108?q=gallery%3Asubmicron%2F23534542&qo=8
http://techcrunch.com/2014/05/15/soldsie-the-service-that-lets-you-shop-via-facebook-and-instagram-comments-raises-4-million/
http://theconversation.com/we-are-all-suspects-now-thanks-to-australias-data-retention-plans-38223
http://the-toast.net/2015/02/10/gal-science-ant-lab/
http://www.adelaidenow.com.au/news/south-australia/sa-public-servant-paid-out-to-quit-at-age-of-76/story-fni6uo1m-1227255760836
http://www.amazon.com/dp/B00I15SB16
http://www.autocar.co.uk/car-news/detroit-motor-show/next-mercedes-benz-glk-spotted-ahead-2015-launch
http://www.canonrumors.com/forum/index.php?topic=25434.0
http://www.couriermail.com.au/news/mh370-disappearance-towelette-that-washed-up-on-wa-beach-being-tested-for-connection-to-missing-malaysia-airlines-plane/story-fnii5s41-1227256204320
http://www.cracked.com/article_22116_6-popular-games-that-were-meant-to-be-totally-different.html?wa_user1=2&wa_user2=Weird+World&wa_user3=article&wa_user4=feature_module
http://www.crymore.net/2015/02/06/the-4-best-animes-youre-missing-out-on-winter-2015-edition/
http://www.dailytelegraph.com.au/news/national/toxic-tuna-daily-telegraph-investigation-reveals-the-smelly-and-messy-conditions-at-thai-tuna-factories-linked-to-poisoned-fish/story-fnpn0zn5-1227255781943
http://www.destructoid.com/police-officer-killed-during-gamestop-robbery-288794.phtml
http://www.dpreview.com/reviews/sony-alpha-7-s?utm_campaign=internal-link&utm_source=features-default&utm_medium=homepage-block&ref=features-default
http://www.engadget.com/2015/03/09/apple-macbook/
http://www.escapistmagazine.com/articles/view/video-games/columns/extra-punctuation/13550-When-Remastering-Classic-Games-Stay-True-to-the-Originals
http://www.gamespot.com/videos/sid-meier-s-starships-ori-and-the-blind-forest-hot/2300-6423773/
http://www.gizmodo.com.au/2014/09/kindle-voyage-this-is-what-a-200-e-reader-looks-like-its-gorgeous/
http://www.joystiq.com/2015/02/03/there-is-no-end/
http://www.kotaku.com.au/2015/03/remember-this-735/
http://www.layer9.org/2014/10/session-3-paper-1-reclaiming-brain.html
http://www.macrumors.com/2015/03/06/hands-on-with-the-textblade-keyboard/
http://www.macworld.com/article/2894575/apples-radical-12-inch-macbook-air-is-the-slimmest-lightest-mac-ever.html
http://www.mortgagebusiness.com.au/breaking-news/8218-frydenberg-concerned-about-smsf-lending?utm_source=Mortgage+Business&utm_campaign=Mortgage_Business_Newsletter02_03_2015&utm_medium=email
http://www.neatorama.com/2015/02/27/The-Girl-Who-Gets-Gifts-from-Crows/
http://www.pcworld.com/article/2893647/gnome-2-is-back-ubuntu-mate-is-now-an-official-flavor.html
http://www.rockettheme.com/forum/general-discussion/147147-page-with-modules-only-no-mainbody-apart-from-home-page
http://www.rockpapershotgun.com/2015/02/26/rimworld-alpha-review/
http://www.smh.com.au/federal-politics/political-opinion/inequality-at-the-heart-of-rejection-of-gonski-program-20131130-2yi54.html
http://www.theage.com.au/federal-politics/political-news/asylum-seeker-torture-report-united-nations-special-rapporteur-juan-mendez-responds-to-tony-abbott-criticism-20150310-13zrwz.html
http://www.tripadvisor.com.au/Restaurant_Review-g1076168-d3418528-Reviews-Blend_Cafe_and_Pizza_Bar-Melville_Greater_Perth_Western_Australia.html
http://www.urbanspoon.com/r/338/1430837/restaurant/Perth/Blend-Cafe-and-Pizza-Bar-Melville
http://www.windowscentral.com/gdc-2015-quick-look-siegecraft-commander-coming-xbox-one-summer
https://gigaom.com/2015/03/08/how-i-manage-my-creative-process-on-an-11-inch-macbook-air/
https://productforums.google.com/forum/#!category-topic/hangouts/Xfh-RfpGBP4%5B1-25%5D
https://vimeo.com/98201214
https://www.indiegogo.com/projects/rocketbook-cloud-integrated-microwavable-notebook#comments
https://www.kickstarter.com/projects/1853707494/pancakebot-the-worlds-first-pancake-printer/comments
https://www.ozbargain.com.au/node/185655
http://www.theguardian.com/australia-news/2015/mar/15/crossbenchers-rebuff-pyne-ultimatum-on-university-reforms-and-research
```