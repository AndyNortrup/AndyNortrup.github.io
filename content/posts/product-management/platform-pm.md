---
title: "Being a Platform PM"
date: 2022-10-31T09:30:00-07:00
draft: false

categories: product-management
tags:
 - ProductManagement
 - platform

cover:
  image: "" # image path/url
  alt: "" # alt text
  caption: "" # display caption under cover
  relative: true # when using page bundles set this to true
  hidden: false # only hide on current single page
---

I've spent a lot of time as a platform product manager.  At Splunk I managed the app certification platform that Splunkbase and Cloud relied on. Later I helped build the platform services for Splunk Cloud Services from the ground up.  At Tanium I managed the Tanium Data Service which served as a common data layer for all of our modules. 

Being the PM for a deeply technical platform team can be really hard.  Unless you come from a deeply technical background it feels hard to have a way to helpfully contribute to that effort. A lot of the work that gets done by a platform team will be very in the weeds, or will be in close execution with the consumer up the stack and their PM on the problem you are trying to solve. You are also more removed from the end-user of the product, which can make empathy and understanding harder. That can make you feel like a glorified project manager.

* You need to do less solution definition with the team and more working ahead of the team to prioritize the work that they are going to do.
* You have multiple consumers all of whom have their top priority things.
* You have a highly leveraged platform team.
* The platform has higher stability requirements than your consumers because you have more dependencies.
* You can't easily change things that other teams consume
* You literally have higher up-time requirements than consumers because you are lower in the stack then they are.

To help manage these constraints you need to be a little bit more of a [scout](../2019-07-06-product-managers-as-scouts/) and less of a solution maker. Here are some things that have helped me be successful: 

* Be actively looking at the roadmaps of all of you consumers to understand which things will require changes to your platform.
* Understand the company strategy and help prioritize that muddle of requirements into a prioritized queue of items your team can work on.
* Help your team understand any of the timelines that consumers are working against and what their impact will be on that timeline.
* Help other teams understand what the flow rates of your team is and help them plan their timeline and backlog around your [flow rate](../2021-10-31-what-i-look-for-in-flow).
* Help refine the acceptance criteria in someone else's requirements to clarify the work for your team.
* In providing a backlog of which items you have coming up in the backlog and what the timelines you can help them make better technical choices.
* They can see what the next ~3 months look like and if there are common patterns in the up coming work that they might want to build stronger abstractions and reuse.  Or they will see that they can build something simpler because they don't have variations coming down the line.
* By helping them see deadlines you can head off some over engineering.  In my experience the level of detail that folks on platform teams tend to want to over engineer things.  They come from a good place but sometimes as the PM we need to help keep that in check with reality.
