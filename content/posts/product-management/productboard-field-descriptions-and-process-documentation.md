---
title: Productboard Field Descriptions and Process Documentation
date: 2023-03-18T20:00:00-07:00
categories: Product Operations
tags:
    - Product Operations
    - Productboard
    - ''
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
I've been working with Productboard a lot in the past few months. Purchasing and helping Tanium implement it has been one of my primary tools to help improve our prioritization, process, and transparency with the rest of the organization.

One of my favorite things about Productboard is the ability to super easily document what fields are and how they are supposed to be used immediately inside of the product. I use this all the time to both make my life easier as the person building systems, and it lowers the adoption curve quite a bit for my users. It also feels like a good example of your [process being open source.](https://www.rubick.com/engineering-handbook/) Where it is clear it is easy update your process documentation.

<!--more-->

I use this in two ways. First is to help simplify instructions when I need someone to set or update a status or informational field. Second, I can use it to keep a running history of why the field exists and what expectations we have around it.

In the first case I take advantage of the fact that Productboard will give you a link directly to a feature view with a field description panel open, you can send someone a link that says "I need you to update this field \[link\]". And the link brings them exactly the view I care about and a description on how to fill out the field.

In the second case I utilize templates that remind me to keep a changelog in the field description of why the field was created and any significant changes in how we use the field. I find that having good templates really helps the whole process along because it makes it faster to write good docs.

For example, my template for a status field looks something like the below. Keys to success here.

1. Clear sections and prompts to myself on what I want to capture when creating a new field.
2. I have blocked out the different states so that I can easily write what they are and think about if we need all of them. My template for drivers is similarly outlined with the different score options (⬜⬜⬜⬜🟦).

\## Description

Why does this field exist, who looks at it, who gets value from the information that we are capturing here.&nbsp;

🔘Not Needed -<br>🔵 Planned -<br>🟡 In Progress -<br>🔴Blocked -<br>🟢Complete -

\## Chaneglog

\* &lt;&lt;Date&gt;&gt; - When was this created, who asked for it. What were we trying to accomplish at the time it was created.