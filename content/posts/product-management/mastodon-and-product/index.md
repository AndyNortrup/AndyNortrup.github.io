---
title: "Mastodon projects and failure to product"
date: 2023-01-04 22:11:45
# weight: 1
# aliases: ["/first"]
categories: "ProductManagement"
tags: ["mastodon, productmanagement"]
# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false

ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---

I've been enjoying the fediverse and mastodon as I've left Twitter for *reasons*. But one thing that I've been exceptionally interested in has been watching multiple newcomers attempt to build offerings on top of the activitypub protocol, then fail dramatically when they realize that while what they have built might be useful for some use cases that it runs into an incredibly hard wall of fediverse culture.  

> I’m not speaking hypothetically. In the dying days of 2022 I watched in real-time as this eager young fellow bounced onto the stage and said he had this new full-text thing he was about to launch, it would index all the instances your instance was federated with, and it was carefully built to penetrate various Mastodon blockages. And anyone who didn’t want to be scraped and indexed had to opt out. (He also claimed it was going to be available only to “genuine admins”.) 
> 
> -- Tim Bray [Private and Public Mastodon](https://www.tbray.org/ongoing/When/202x/2022/12/30/Mastodon-Privacy-and-Search)

* Tim Bray covered some items around [full text search](https://www.tbray.org/ongoing/When/202x/2022/12/30/Mastodon-Privacy-and-Search).
* [Mastinator](https://mastinator.com/apology/) - Some folks created an ActivityPub tool that could be very handy for testing ActivityPub implementations, but they left it running, and it was randomly following and reposting toots without consent.
* [lgbt.furry](https://furry.lgbt/@updates/109621439802503104) attempted to build a blocklist aggregator on top of the #fediblock hashtag without taking any efforts to understand the history of the hashtag or why and how it was created.  Mostly they tried to erase the fact that it was created to actively combat anti-black racism in the fediverse. 

Each of these examples are case studies in running into a market that does not want what you are selling (even when you are giving it away) and floundering. As far as I can see from these efforts each effort was lead by curious engineers who were excited about the fediverse and wanted to contribute to this new platform by building on top of it. I even think that each of these ideas has merit and value. 

* Not everyone wants full text search, but it might be valuable in some cases.  Admins and the community at large objected to being default opt in added to a full text search of all the things. 
* End-to-end testing is a good thing :tm: but the community at large objected to having their posts reposted by a bot without any consent or clear opt out. 
* Good block list and defederation lists are going to be important to manage the scale that seems like it is coming for the fediverse if Twitter continues to implode.

But in each case, despite valid use cases the products (yes we'll call them products even if they were free and open source) failed early and hard because the market was not remotely interested. And while the actual cost is probably a few weekends of time and some EC2 instances.  But it is very easy to imagine this happening to a company with actual stakes. 

> Aside: This is also an interesting example of the dichotomy of user vs buyer that plagues enterprise software.  Here the buyers weren't CISOs with their security budget, but fediveres admins who can choose to defederate and promote the defederation of projects that violate community norms. 

That isn't to say that every open source needs a product manager, but it is a reminder that one of the most important things that the product management skill set can bring to a project is helping to identify and mitigate risk early in the product lifecycle.  All three products could probably been successful if they had done some minimal additional research on what the community expectations were.  Full-text search and Fedinator probably would have been just fine if they had been opt-in. All that was asked of the lgbt.furry team was to credit the creators of the #fediblock hash tag and the hard work that had been done to turn that into a community norm. 

Instead, in each case the individuals and teams dug their heels in and insisted that their work should be accepted because it was technically possible and technically novel.  I think there is a fair amount of white privilege in those positions, potentially bordering on racism. I've seen this in multiple enterprise products where superior technical solutions failed to win the day because they didn't actually meet market needs or community expectations. 

Those failures frequently happen outside the product / engineering agile delivery process.  They happen in the ideation and bet selection process where good ideas get approved without clear identification of the risks and dynamics of the product. Or, they happen after the product is built and go to market fails to properly position or launch the product. 

So before you go build your next fediverse project or enterprise software feature. Spend some time de-risking the whole product experience, not just the technical implementation.  How will the product be received by the whole community that will interact with it. 