---
layout: post
title:  ""
//TODO: Fix the date
date: yyyy-mm-dd
tags: 
---
 I've been pulling and analyzing Mik Kirsten's Flow Framework metrics for several months at work.  I do this with an incredibly ugly Clojure script that I wrote to lean clojure.  But I do think the metrics themselves have been a helpful lense to look at what is happening.  Here are some of th questions I ask myself when I sit down to analyze the metrics.
<!--more-->

First some qualifications:
* I pull metrics monthly with weekly intervals.
* I pull metrics at the portfolio level (lead by a Sr. Director of PM) I have occasionally pulled the metrics for my own projects. But the portfolio level feels closest to the value stream customers buy and also hits a nice balance of me doing the analysis in my spare time.
* I pull metrics entirely from JIRA, I know that I have some blind spots by doing that and my connectivity index is low; but it is what I have.

Things I look for:
* Is velocity increasing? As a growing product company we generally want to see velocity increasing. Either by improving our systems of work or by adding more people to the company.
* Did the velocity change at a reasonable rate.  
  * If I see big spikes I worry that someone is on a death march to get a feature out
  * If I see big dips I worry that a new impediment has arisen and needs to be stabilized. 
* Does the distribution of flow items match the stated strategy? 
  * If we are focused on the SaaS business I expect to see more tasks.
  * If we just released a major update I expect to see more bugs.
  * If we are in the middle of pushing a big update out I expect to see more features.
* Are the active time, flow time and flow efficiency pretty even?
  * Big variations are an indicator that the system of work is not consistent.
* Are the active time, flow time and flow efficiency improving?
  * Much like velocity we should be doing consistent work to improve the system of work and improve our flow time and efficiency. 

Hopefully this helps you have some thoughts to start looking at you own flow metrics.