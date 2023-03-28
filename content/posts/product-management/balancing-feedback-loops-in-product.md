---
title: Balancing Feedback Loops in Product
date: 2020-09-15T04:30:03-07:00
categories: product-management
tags:
    - Product Management
    - Systems Thinking
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
    image: /uploads/cloud-conversion-3-1.png
    alt: Balancing Feedback Loops for cloud customer conversion
    caption:
    relative: false
    hidden: true
---
Working with some colleagues recently I was asked "Why aren't we doing all the things to really be \[desired state\], we should pause and think about how we really want to restructure the company and the way we build software to do it right."

My colleague has a great instinct and she isn't wrong in seeing the gaps that we have in the product and how we produce software.&nbsp; But I think that its important to apply systems thinking to solving these problems.&nbsp; That requires us to understand where we can apply leverage to change the balancing feedback loops that are enabling and constraining our products.<!--more-->

Lets say that you are trying to migrate a software product from an on-prem focused delivery to cloud first.&nbsp; I had a hand in this both at Splunk and at Tanium so I'm familiar with at least some patterns in this space.&nbsp;

{{< figure src="/uploads/cloud-conversion-1.png" alt="Converting potential customers to cloud customers." >}}

A balancing feedback loop consists of a current state, a desired state and flows that enable or limit the state change. In software their are many flows that divert people away from buying your software. It might cost to much,&nbsp; not solve their problems, be worse than a competitor, or not of sufficient quality.&nbsp;

In the context of a cloud migration, your most likely causes of customers not migrating into your cloud offering are capability gaps that either prevent your customers from adopting or your business from selling to them.

* You can't talk to their on-prem data
* You don't give customers the same administrative rights they have on-prem
* You don't have certifications required (FedRAMP, SOC2, ISO, etc)
* Architectural decisions on-prem make it expensive to operate
* Operating costs make your price for cloud to high for customers
* etc
{{< figure src="/uploads/cloud-conversion-2.png" alt="Balancing feedback loop of cloud customer conversion." >}}

I think what my college is looking at is that we need to remove those balances on our conversion system, with a particular eye on how important our technical infrastructure. Unfortunately we cannot eat the elephant all at once.&nbsp; If we dig in and start doing our homework as product managers we see that there aren't two balancing forces, there are dozens of smaller forces that we have to solve for more tactically. Picking the ones with the highest impact and the highest leverage as we go.

{{< figure src="/uploads/cloud-conversion-3.png" alt="Ballancing feedback loop of cloud conversion with split out forces." >}}

As we start to talk to more customers and operate the service with more customers we are going to be able to start to weight these priorities by their level of impact on our ability to convert. We might start by identifying that a particular administrative surface that we took away in cloud needs to be restored to unlock many potential conversions. So that becomes our number one priority.

{{< figure src="/uploads/cloud-conversion-4.png" alt="Balancing Feedback of cloud conversion with one feature highlighted as the priority" >}}

Once we work diligently to solve that problem the system will evolve. Now that we have all of these new customers we realize that all of these customers have pushed up our operational costs, and we are losing our shirt on storage costs on our compute instances.&nbsp; So now we need to prioritize an improvement to our storage architecture that will allow us to have a responsible business model before we can go after the SOC2 attestation that will let us get even more customers (who would make the storage problem even worse).

{{< figure src="/uploads/cloud-conversion-5.png" alt="A balancing feedback loop that shows storage costs are now the number one priortity" >}}

So not only can we not solve all the problems at once, the very act of solving the problems will change the very problems themselves.&nbsp; As we add new customers our audience changes and has different expectations, the costs of delivering the service changes. Process that worked for operations when we had 100 medium sized businesses doesn't work anymore when you have 1000 medium sized businesses and&nbsp; 100 large enterprises.&nbsp;

This can feel like you are just drifting from crisis to crisis and not building it right the first time.&nbsp; But in complex adaptive systems we the impact of the changes is mostly unknowable. So we can focus on the problems that are in front of us and adapt as we learn new things. As we change the system the strength of the flows will change and we will adjust our roadmap and plans appropriately.