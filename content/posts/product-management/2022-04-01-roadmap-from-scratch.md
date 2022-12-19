---
title: "Roadmaps From Scratch"
date: 2022-04-02T18:42:12-07:00
draft: false

categories: product-management

tags:
- roadmap
- ProductManagement
- "Cost of Delay"
- WSJF

cover:
    image: "/images/posts/product-management/roadmap-from-scratch/now-next-later.jpg" # image path/url
    alt: "Now Next Later Roadmap" # alt text
    caption: "Building a Roadmap From Scratch" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
---
Very rarely will you build a roadmap from absolute scratch. But the technique is helpful because you can apply the process to help rationalize or refit an existing roadmap. I'm a strong believer that you should be able to connect all the work you are doing from top to bottom of the company.  A developer should be able to look at any task and put it into the context of the larger solution they are building, the problem it solves for the customer, and the business objective that it supports. 

I see this as an extension of something that I wrote into all military orders.  Every unit received their mission as well as the mission of units two levels up. So that when the plan wasn't working you could make intelligent decisions to keep the larger mission moving in the right direction.

## Business Goals
Start with your business goals, what is your company trying to be or accomplish? These are probably the things that other departments are talking about. Ask your CEO, CFO, Head of Sales, head of support, customer entablement, partnerships.

Goals will probably be something along the lines of:

* More revenue
* More customers
* Bigger customers or moving up market.
* Smaller customers or moving down market
* Shorter sales cycles
* More support revenue
* Less support hours
* Happier Customers
* Pay down technical debt

Hopefully these are also paired with a "Why".  Something like:

> We want to have 1000 customers in the small business segment by the end of next fiscal year because they have more revenue per-customer than our individual premium customers and have a higher lifetime value because they rarely churn.

You'll probably get two or three of these if you canvas across the company. Talk to all the folks at the leadership level and ask them to bucket these goals into groups of importance.


{{< figure src="/images/posts/product-management/roadmap-from-scratch/goals.jpg"  height="300"
title="Organizational Goals" >}}

Next talk to all sorts of folks about about customer problems that you can solve to help sell to the customers that will help you accomplish those goals.Talk to customers, sellers, read notes on deals you didn't win, look at telemetry to see where there are breaks in the customer journey in your target audience. You'll find lots of potential problems you could solve in 10 years. Also get metrics for what solving these problems would mean.

{{< figure src="/images/posts/product-management/roadmap-from-scratch/goals-and-ideas.jpg"  
height="300" 
title="Goals with unordered ideas">}}

As you start to discover these problems begin order those goals but which ones will give you the most impact for the least amount of work. The general formula is `Cost of Delay / Effort`. You should be able to start bucketing your goals into groups that are generally about as valuable as each other.  You don't have to get into super granular dollar value estimates of how much revenue is at stake. If you can do that good on you.  But we are trying to avoid really big mistakes not pick between two things that could have very similar outcomes.

Work with your engineering partners and work out the same very granular level of detail on how hard problems will be to solve. I like the cyneffin framework at this level.  Really we want to understand where on the spectrum of "we know how to do this and need time" to "I have no freaking idea where to start" 

{{< figure src="/images/posts/product-management/roadmap-from-scratch/goals-and-weighted-ideas.jpg"  height="300" title="Goals with Weighted Ideas">}}

Now you have a list of goals, with a list of problems you could solve to help accomplish them roughly sorted into `Weighted Shortest Job First` order. Work with your leadership to figure out how much you want to put into each goal, nice round percentages of your engineering staff.  Keep aside some capacity for engineering to do engineering things. DevOps, infrastructure, bug fixing and fire fighting.  Leave slack in the system. 

{{< figure src="/images/posts/product-management/roadmap-from-scratch/ordered-ideas.jpg"  height="400" title="Goals with Weighted Ideas">}}
 

Look at your lists of problems for each goal, decide how many you can work at once with the number of engineers allocated to thePut them into the buckets of Now, Next, and Later.

**Now** is everything you are currently working on.
**Next** are things you are willing to commit to customers that you will do. You'll pick things up from this column when you finish a problem.
**Later** are things you are thinking about but aren't committed to doing. 

{{< figure src="/images/posts/product-management/roadmap-from-scratch/now-next-later.jpg"  height="300" title="Now Next Later Roadmap">}}

Then start showing this to other people and see how they respond. Have good discussions and adjust based on those discussions. When you have confidence start building solutions to problems in your Now list. Have some folks (PM and Engineers) doing discovery for items in the next column

Congratulations, you have a roadmap!