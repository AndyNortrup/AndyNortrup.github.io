---
title: "Manipulating the Sorted Backlog"
date: 2022-04-18T16:34:12-07:00
draft: false

categories: ['Product Management']
tags:
- Roadmap
- 'Product Management'
- WSJF
- Prioritization

cover:
  image: "value-and-effort.png" # image path/url
  alt: "Value over Effort" # alt text
  caption: "Value over effort is the essential sorting function of an effective backlog." # display caption under cover
  relative: true # when using page bundles set this to true
  hidden: false # only hide on current single page
---
I've written recent guides to creating a [backlog from scratch]({{< ref "../2022-04-01-roadmap-from-scratch.md">}}) and [sorting your backlog]( {{< ref "../quick-prioritization/index.md">}}) by value and effort. As part of building and sorting the ideas and initiatives on your roadmap you will start to show that roadmap to other people. When you do people will have opinions about the order that you have sorted things in.  In most cases their opinion will either be agreement, or more commonly, they would like the thing that is important to them to be higher on the list. These differing opinions are good, this is why we build a roadmap. It is better to have those discussions when we are thinking about building things then after we have spent time building something.

{{< figure src="backlog-math.png" alt="Changing the backlog sort by changing value or effort" caption="Changing the backlog math">}}

If a stakeholder wants to move something around on the backlog then they should have information that justifies changing the underlying math of the backlog. If you want something to move up the stack you need to convince the PM that it is either more valuable or eaiser to build. If you want to drive something down the backlog (because sabotage is a strategy) then you need to convince the PM that it is less valuable and harder to build. So let's outline some decent reasons to move those numbers around. These are some patterns of prioritization that you can use to help clarify the discussion.

### More important
* More strongly supports one or more business goals or OKR
* Unlocks another initiative that is higher ranked. 
* Feature or step must be part of a first release
* Strong customer demand
* Customers are upset this isn't fixed yet 


### Less important
* Unlikely advance a stated business goal
* Lack of executive sponsorship
* No one has actually asked for this / lack of clear interest
* People have said they want it but not that they would pay for it

### Easier to Build
* Similar to something already built
* Prior art and recommended practices to draw from
* Open-source components can be utilized
* Decreasing the success criteria (you are aiming to high)
* Decrease scope and remove planned but not strictly necessary features

### Harder to Build
* Techdebt
* In a more difficult [Cynefin domain](https://en.wikipedia.org/wiki/Cynefin_framework). 
* Blocked waiting on something else to get built
* Cross team, valuestream or platform work is required
* Works against your core technology differentiators
* Available engineers don't have proper experience  

## Watch out for local optimizations

As discussed in my post on quick sorting, we want to avoid trying to micro prioritize issues and initiatives. Our ability to accurately estimate the granular value or effort of our work in advance is limited. You are looking to draw out information you missed that would move an idea or initiative between the big columns in our sorting process. Changing our value score from a 2 to a 3 or a 2 to a 5 is significant in our course sorting. Trying to change the sort order inside of a column is less useful. We probably in the long run can't tell the difference in outcomes between `Idea 3` being marginally more important than `Idea 7` if both ideas still have a value of 2. 

{{< figure  src="moving-between-columns.png" >}}   

