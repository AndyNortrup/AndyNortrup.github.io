---
title: Fediverse Hosting Wishlist
description: "I want the Fediverse to succeed, but it needs to be easy for laypersons to start and run their own small communities, here is how to make it work."
date: 2023-02-10 14:56:30
preview: null
draft: false
tags:
  - Fediverse
  - Mastodon
categories: technology
---
I've been experimenting with the Fediverse / Mastadon and I really like it.  I've been on my friend's Seattle locals instance that he runs as a hobby. I sort of want to run my own instance, but I don't want to think about any of the server operations. I want a hosting provider and I want it t to make it easy.

## Content moderation is the problem
Content moderation is the biggest problem in Social Media, particularly scaled social media.  Facebook makes more content moderation decisions every hour than the entire U.S. Justice system has made in it's entire existence. Some of those are really thorny issues that don't have a single solution. And there are some very serious problems with serious legal implications.

These content problems fall into two big buckets. Stuff that people go to court or jail for and problems that just make people mad at each other. The former includes Child Sexual Abuse Material (CSAM), copyright infringement, threats of violence and harassment. The later includes the more mundane but also thorny issues of people saying things that other people don't like, which get reported and someone needs to decide on. 

If we look at big social media, they have been better and worse about the first class. They staff trust and safety teams that work on abuse and CSAM. Maybe they should work more, but their has been a lot of good work with various governments to be able to easily report CSAM when it gets found.  They are less good on abuse, but efforts are made.  Much of this work is done on the backs of low paid contractors who have to wade through the muck of humanity and suffer terribly for their labors.

The second class of content is just straight unsolvable.  If you've watched the GOP try to drag social media execs through clown show hearings to complain about moderation decisions and how conservatives are treated unfairly in social media, you can see the problem. 

## Solutions
I think that the Fediverse if operated well can have a better structure for managing those problems. In my mind most of this runs through distributing content moderation decisions into smaller instances and creating social pressures for better behavior. 

I'd love to see a Fediverse hosting company that does the following: 

### Non technical 
Makes it easy for an individual to create a new instance for themselves and their communities without having to speak any geek.  If you mention server specs you have made it to hard.

### Caped, invite only communities
Caps instance size and enforce invite only communities.  Keep communities in the 150 to 250 member range. This isn't about managing the technical cost of the instance operation but keeping the community small enough that it can be managed by humans on a part time basis.  If you have to extend an invitation to my personal community, you'll be have like you are at a social club meeting rather than like you are at a bar. 

{{< figure src="DunbarsNumber.png" alt="Dunbar's Number" caption="Dunbar's Number ([Wikipedia](https://commons.wikimedia.org/wiki/File:DunbarsNumber.png))">}}

As content moderation reports it should also be easier to make decisions because a small community will have a clearer sense of cohesion and social norms.  You'll know the person who has been reported or the person who invited them and be able to have a conversation about what has happened and what is OK in your community.  You can:
* Decide to censure the author of the offending post
* Decide to block or mute reporter for malicious reports
* Choose to defederate instances.

### Support for the go to jail problems
The hosting provider should do some of the admin lift for you. Things like scan images for known CSAM with from [NCMEC](https://www.missingkids.org/HOME) and have a team and process to automatically report and handle reports of CSAM on your server.  They should help handle things like DMCA takedown requests. Also, you should maybe have some support line for moderation decisions. 

If we want folks to have their own communities they should feel safe that they aren't going to have someone in their community that makes them unsafe, creates legal liability, or could land them in jail.

### Out of the box block lists
Instance admins and mods should be able to subscribe to a continuously updated block list.  Keeping continuous track of which hosts need to be defederated and blocked because they are hives of scum and villainy shouldn't be required to have a Pixelfed instance to share pictures with your Bonsai club, or share toots of dad jokes with your friends.

### Enforce that moderation happens
If you are going to run an instance you need to have someone doing moderation. If your instance receives moderation requests and doesn't handle them in a timely manner, then there should be consequences.  Those can ramp up from a warning, to forced isolation of the instance, to loss of service.

Also if an instance is a continued source of malicious activity, if you are getting aggressively defederated for being a haven for bad actors. No amount of "processing" your moderation queue and saying LGTM should be OK.  This protects both the larger fediverse and the hosting provider.

### Effective Operation 
There is lots of space for an effective hosting platform to make use of shared resources that make the Fediverse more efficient. This can all be on the backend, no one has to see what is going on. But some amount of database clustering, auto scaling, resource multi-tenancy will go a long way.  I say this mostly from my experience helping two B2B SaaS companies move from single tenancy to multi-tenancy models.  It a hugely important step for resource management and reliability.  It is probably some level of forking away from the main branches of Mastodon. 

### Early discovery

Starting on Mastodon is easier if you can jump to the local timeline and start to find some things to discover.  If you are in an instance all by yourself it would be really quiet.  If you want folks to be successful, you are going to need to give them some starter material so they can find someone to follow.