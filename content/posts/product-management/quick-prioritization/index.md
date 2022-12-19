---
title: "Quick prioritization of a backlog"
date: 2022-04-18T16:34:12-07:00
draft: false

categories: product-management
tags:
- roadmap
- ProductManagement
- WSJF


cover:
  image: "lots-sorted.png" # image path/url
  alt: "A backlogs sorted by value." # alt text
  caption: "Quick prioritization of your backlog." # display caption under cover
  relative: true # when using page bundles set this to true
  hidden: false # only hide on current single page
---

There is a lot of complexity in Product Management, but at the very heart of it what we look to do is order all of the things we could be doing to produce the most value possible. To do that we have to carefully weight the balance of value to effort in order to properly sequence the infinite set of work that we could be doing. 

Estimating is a tricky and messy business, and I'm frequently skeptical of. But when you are trying to prioritize multiple potential projects as a product manager, having some basic numbers can really help things along.  This is a system I've used multiple times to quickly establish baseline value and effort estimates. I like it because it is fast and avoids a lot of hemming and hawing.  The goal of this system is to get things in mostly the right order and avoid making big mistakes.

{{< figure src="big-stupid-mistakes.png" title="Avoid Big Stupid Mistakes">}}

I'll now walk you through a process of establishing some baseline order. We'll go through this twice, once for value, probably set by a PM. And a second time for effort, probably lead by someone on the engineering team. To get through prioritization quickly we want people to use their system one thinking. And tell us what they think without a lot of deep analysis.  The more deep analysis we do at this stage the slower this will go and the less useful it will be.

Start with your stack of unsorted ideas. 
{{<figure src="unsorted-ideas.png" title="Unsorted ideas.">}}

As a PM, ask your self: 

> If I could wave a magic wand and have either one of these things right now what would I pick?

There are lots of reasons to want something more.  

* More revenue
* Better alignment with goals
* Better alignment with market
* More stakeholders yelling at you
* That irate customer
  
Put the thing you want more to the right of the thing you want less on the board. This is your first sort. Congratulations. Have your engineering counterpart or team sort the same two cards based on effort.  Which one of them is harder than the other?

{{< figure src="first-sort.png" alt="First sort with more valuable idea on the right">}}

Grab another card and ask yourself. Do I want this more, less, or the same as one of the other things on this board. 

{{< figure src="idea-3.png" alt="Adding a third card to the board." title="Add your third card">}}

Great, now you are really on your way. In this picture we decided that idea three was about as valuable as idea 1.  Do a quick feedback check with the room (you should be doing this with other people, it's a group activity). 

{{< figure src="three-sorted.png" alt="Three sorted idea cards">}}

Keep going until you have all of your big ideas on the board.  You should have something that looks roughly like this figure below.  Note that we have multiple cards that are about the same value.  Remember we don't need intense precision here. These are estimates not predictions. 

Ask everyone around the room for some feedback.  Anyone think you are super wrong.  Talk about that, briefly. 

{{< figure src="lots-sorted.png" alt="Lots of sorted cards by priority" >}}

Now you can add some column values above the cards. I didn't do this until now because we can always add something in between other columns and its a pain to renumber things. Also people's brains get weird when you put numbers up and they over think.  I use fibonacci sequence numbers for columns because I think it makes the final values spread out more.  

{{< figure src="sorted-with-values.png" alt="Ideas, sorted with fibonacci numbers as column values.">}}

Now you can combine the values from your PM `value` based order and the engineering `effort` based order and you get a number! This is the weighted shortest first value. Take all your cards, calculate their values and then sort the whole list.  Now you have the start of a prioritized backlog.  

{{< figure src="one-card-with-values.png" alt="One card with value and effort numbers">}}

The important things to remember is that this is just the first step.  You need to take these boards and start showing them to people. Show your boss, show your stakeholders, show other PMs, show customers.  Ask them which items are higher or lower on the list than they would like or expect. Dig into why they think something is higher or lower on the list. 

* You thought there was less value than they did.
* There is disagreement on how hard it is.
* Maybe you don't actually agree about what you have to do to solve that problem or build that solution. 
* Perhaps you forgot to recognize some piece of horrible technical debt?

Have lots of those conversations, have them all the time.  As you get interesting answers, revise your value and effort estimates. 