---
title: "A Solid Fediverse"
date: 2023-06-14T09:48:12-07:00
# weight: 1
# aliases: ["/first"]
categories: "Technology"
tags: ["Fediverse", "Solid"]

# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
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
The Fediverse is great, I love it, but as I see more and more projects to spring up to replace different private social media operations.  First it was Twitter, now Reddit is seeing an exodus to [Lemmy](https://join-lemmy.org), there is also [Pixelfed](https://pixelfed.social) to replace instagram and bookwyrm to replace Goodreads. 

It's great. But it isn't without its problems.  

## No consistent Identity
We don't have a clear identity federation system.  I came across [Keyoxide](https://keyoxide.org/) which seems like a great way to start gluing your identities together, but is not yet user friendly. As a result I have an ID on three different fediverse services and I can only sort of glue them together with profile links.

## Community Admins and  Moderators
We are very dependent on having groups of mostly volunteers to keep our instances and communities up and running. I'm personally using an instance a former co-worker runs.  He does this because he finds it fun, but if he were to decide that it's no longer fun, then my instance could go away with little to no notice. We've seen this happen several times to large instances where several thousands of users were displaced with a few weeks notice.

This shouldn't be surprising, to host a social media community you have to perform DevOps to keep the computers working. You have to deal with content moderation, which is a loosing game; it cannot be won. You also have to deal with trust and safety issues.  How long would you keep doing something for no money after you got a few moderation reports for Child Sexual Abuse Material (CSAM)? I personally would not put up with it for long.

## Solid Pods at the center of it all
I think there is a better solution close at hand.  I've been watching the [Solid Project](https://solidproject.org/) for years and this feels like it should be it's moment.  Rather than joining an instances of a particular project I should be able to have my own Pod with all of my data stored in it.  

Then each project I want to use all the project needs to do is provide a front end over my data.  I can have one identity for PixelFed when I want to look at and post pictures of my trees, I can log into [Elk](https://elk.zone) when I want to read a feed of microblogs.  I can go to [Lemmy](https://join-lemmy.org) when I want to get questions answered. 

Elk is actually a great example of what should be possible.  The Elk front end is my favorite UI for Mastodon, and it stores effectively no data about me.  It talks to my instance and it displays the data.  Instead it should be able to talk to my pod and project my data.  My pod serving as a single instance for multiple different lenses of the same data.

I suspect there are thorny problems in here with caching and distribution to many many more single instances.  But maybe that is something that a good Pod provider can help solve at scale?

But the escape from corporate social media has taught us that we need to own our own data.  But changing from having a big central company holding your data to some nice person holding your data is a step in the right direction but not the destination.  We need to own our data.