---
title: Against Global Priorities
date: "2020-12-14T00:00:00Z"

tags: 
- 'product-management'
- 'prioritization'

categories: 
- 'Product Management'

type: post

alises:
- /against-global-priorities
---

I've been working with some stakeholders on how we do prioritization as a Product Management team.  I started by trying to build a matrix that would serve as an easy key for keeping product managers mostly on the same page for setting the priority field in JIRA.  I think there is value in having common standards.  But the more I thought about the problem, I got more uncomfortable, because we can't prioritize globally and take into account local context.
<!--more-->

The priority field in JIRA has started to feel a lot like story points, not worth a lot outside of their local context. In an attempt to keep things simple my initial effort I put the number of endpoints impacted with some broad 1/3 buckets and complexity on the very broad criteria of the number of components that would need to be changed to complete the improvement.  It's nice, but I quickly realized that it doesn't tie in any of the other factors.

* Time criticality / cost of delay - Some things are extremely important if you can do them right now, but not valuable at in a month.
* What value stream does the idea support, what is the priority of that value stream? I have lots of ideas that woudl improve the product, some of them touch 100% of customer endpoints, but the improvement itself is not well connected to the larger value streams that are important to the company right now.
* How well validated is the idea? Do we have lots of customer telling us that they are feeling this pain point? Is this as good idea we just had in the shower? 

Clearly this list goes on and on. There is always more context, this is why the classic Product Manager answer is "it depends." If you need to get into a multi-dimensional table to quick reference your global priority, than you are probably approaching things in a way that is going to cause difficulty  in the longer term. If this is happening to you, start considering if you are using proxy metrics for success rather than real customer focused outcomes.  

Priority is still a useful field in tools like JIRA, it helps local teams sort and see what is important.  It can be helpful in reports one level up to highlight potential discussions to be had (I see that you have this as a P0, why is that?).  It might even help you tell if something has been vetted (I put a priority on things after I've talked about it with my team, it's a local standard that we use to know what is triaged). But it gets less useful as you go up the chain to directors and chief product officers.

We should be looking as product managers to build systems where every level of the organization has room to manuever as long as we are aligned on priorities.  More important than keeping track of how many P0s are open is being able to see what is in progress and what value stream does it align with. If you see work that doesn't have clear alignment than we should start investigating what is going on.  If everything is on alignment we should ask if we are goals have the right levels of investment in each of our value streams. Then we can discuss if we are picking the highest leverage work inside of any given value stream.