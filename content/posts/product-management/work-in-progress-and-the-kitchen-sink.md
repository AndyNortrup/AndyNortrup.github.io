---
_schema: default
title: Work in progress and the kitchen sink
date: 2023-12-29T21:49:00-08:00
categories: Product Management
tags:
    - Work in Progress
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
disableHLJS: false
disableShare: false
hideSummary: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
cover:
    image: <image path/url>
    alt: <alt text>
    caption: <text>
    relative: false
    hidden: true
---
I try to explain work in progress limits a lot and feel like it comes across as an abstract concept a lot of the time. How much work can the team do at the same time? Or it gets a historical example from Toyota about kanban cards and spots on a pallet, which doesn't make a ton of sense if you've never worked in a factory.

Today I have a more concrete example, the kitchen sink and putting the dishes away. My system of washing the dishes starts at the dining room table, goes to the dishwasher or sink then goes back to the drying rack or the cabinets

At each step there are distinct work in progress limits. I can only put so many dishes in the sink, dishwasher or drying rack, and when they are full they create a constraint on the rest of the system. There are limits to what I can put on the table and in the cabinets, but those don't come into play very often and are less useful to the discussion.

What does it look like when I hit my work in progress limits in this system

* If I have dirty dishes on the table or in the sink and the dishwasher is full, then the dishes wait to go into the dishwasher until I empty the dishwasher (or I have to be less efficient and wash them by hand)
* If I'm emptying the dishwasher and the drying rack is full, I can't put dishes there that are still wet. I have to either be less efficiet and dry things by hand or empty the drying rack before emptying the dishwasher.

I like this example because it it has nice clear physical constraints that you don't see in software development. In software we can stack up as many things as we want in the "needs qa" column of a jira board (yes it's usually the QA column). You don't run out of space. But the more things you put in that queue the more expensive things get.

* The more time between when an engineer worked on something and a QA engineer finds a bug the harder it will be to fix.
* The more time something waits for QA before deployment the longer bad assumptions will be baked into later work. Fixing this bad assumptions will be more expensive.

Additionally, this example shows that I can fix a backed up queue in more than one way. You can wait for the work center to catch up by waiting for the dishwashir to finish and empty it or empty the drying rack. **Or** you can use a less efficient resource to complete the work. I can wash the dishes by hand. It will take longer and use more water; but the dishes will get done.

In the software parallel we can find less efficient ways to clear a queue to keep the whole system moving.

* You can ask non-QA engineers to do some QA, or look at merge requests that aren't in their normal specialty.
* Product managers frequently pinch hit to do testing.

These things might take more energy, but they are options that move things along and are better than those same engineers sitting in their hands waiting for the queue to clear.

The other thing you can do when a queue is full is something that will help the queue clear faster later. In the kitchen, if the dishwasher is finishing, I might empty the drying rack, so that there is space to set things out to dry. In software I might have engineers impacted by a blocked queue use that slack time to work on build systems, test automation or documentation that helps everyone go faster.