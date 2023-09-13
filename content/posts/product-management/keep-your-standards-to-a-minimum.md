---
_schema: product-operations
title: Keep your standards to a minimum
date: 2023-09-13T00:00:00-07:00
categories: Product Management
tags:
    - Product Operations
    - Product Management
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
I recently had a conversation with several Product Managers&nbsp; at work who wanted me to step in and set a standard for how and who was responsible for triaging bugs reported to their teams. The question was mostly focused on who inside of the team was responsible. Was that the engineering manager, the PM, the TPM?&nbsp; Between the four folks who came in mass to my office hours, there were five different ways of managing bug triage.&nbsp; This was causing some challenges because there was a RACI being built to set expectations.

I had a very firm "No I won't create this standard for you".&nbsp; And I'm here to caution other product leaders and product operations teams not to do it either.&nbsp; When you are operating a dynamic adaptive system with multiple independent teams.&nbsp; It is important to be very thoughtful about where and when you set and enforce standards.&nbsp; Some questions you should ask yourself before establishing a standard that everyone must follow.&nbsp; <!--more-->

We should think about standards in systems in and teams as a tool to reduce the Cognitive Load on teams and individuals and make it easier for value to flow through the system. So when we are considering creating a standard we need to think of who and how we will reduce the cognitive load.

<img src="/uploads/team-topologies.png" width="900" height="506" alt="Cognitive load was characterized in 1988 by psychologist John Sweller as “the total amount of mental effort being used in the working memory.” Team Topologies by Matthew Skelton" />

Book Recommendation: <a target="_blank" rel="noopener" href="https://bookshop.org/a/8319/9781942788812">Team Topologies</a> (Affiliate Link)

## Downstream Consumers

Is there one or more groups that is consuming the output of this process from multiple teams that depends on having a standardized output. If multiple teams are passing work to a common destination further down the value stream then it makes sense to standardize for the ease of the downstream teams.&nbsp;

Cloud infrastructure is an example. Its a reasonable expectation that teams conform to standards to gain access to cloud infrastructure if that supports availability, reporting, alerting and ease of use.&nbsp; This is probably true even when that standardization might cost the team to lose some flexibility in their design.

## Enforcement

If something is really going to be a standard someone is going to have to invest in actually enforcing that standard.&nbsp; This is in part credibility issue and also what is the point of creating a standard if you'll let folks keep doing non-standard things. So you have to ask yourself, how will you effectively track and remediate compliance with the standard. If you can't effectively enforce the standard why are you bothering to create it in the first place?

## Team Flexibility

If you have teams that need to form and reform it can be beneficial to have standards that make it easy for everyone to start working together because there is a baseline of how things are done.&nbsp; It is also helpful if you are adding lots of people and scaling rapidly to have a documented standard that they can be trained on

The Army has a standardized planning process that is taught from everyone from staff NCOs general officers at every school from when you join to when you retire.&nbsp; This makes it easy for the Army to take almost any group of officers form anywhere in the Army put them in a room and tell them to plan and they know what process to use.&nbsp; That is handy when you make people move every 3 years or when you are in combat.

## Return on Investment

The other thing to consider is if setting a standard will impose more harm than good on the teams that use that standard.&nbsp; In the case I outlined at the top of the article, I had four PMs and five methods of doing triage.&nbsp; I might create a standard that aligns with one or two of those teams. But I would likely interrupt the norms of at least 3 or four teams.&nbsp; And that was just in a subset of my whole org. As an extension, if you have strong norms across the organization that are doing the same thing, there is lest cost to imposing a standard.

## Size of the organization

The smaller the team that you are trying to standardize, the easier it is to create a standard.&nbsp; Its really easy and low cost to create standards at the individual team level. It's more expensive to do it for several teams in one coherant portfolio.&nbsp; And the cost continues to go up the higher that we go in the org chart.

We want to try and build systems that allow individual teams to be self organizing in their process and find what works for them. Occasionally we will set standards for everyone. But we should do that only when we have compelling reasons.

## All Together Now

Let's review the example we discussed at the top of the post. Should I set a standard on who inside of a team is responsible for leading bug triage?

1\. **Downstream standardization:** ❌ Downstream consumers probably want to understand what our standards are in JIRA for marking a ticket as triaged, and how long they should expect to wait for something to be triaged. But they mostly don't care who does the triage.&nbsp;

2\. **Enforcement: ❌** I cannot go to every standup for all of the teams and make sure that they are following a standard for triage.&nbsp; I don't even think that I have a feasible mechanism from observing it externally.&nbsp; So whatever I say the standard is, people will continue to mostly do what they want in their own meetings.

3\. **Flexibility:** ❌ We have generally long lived teams on long lived projects.&nbsp; Sure there is turn over, but we are not trying to hot swap people on a regular basis.

4\. **Return on Investment: ❌** In order to set a standard here I would have to do a lot of work to teach people the new way, it would have upset their flow and patterns. It would be a high cost to get people to use the standard and we would have sacrificed velocity on the way.

5\. **Size of the Organization:** ❌ The request was to set a standard that would impact every engineering team in the company. That's a very high bar to try and standardize on.

So keep your standards as tight as you can. You can be more specific the closer to the action you go, but refrain from getting to perscriptive whenever you can get away with it.