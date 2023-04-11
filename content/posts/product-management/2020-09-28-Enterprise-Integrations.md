---
date: "2020-09-28T00:00:00Z"
title: Enterprise Product Integrations Journey
excerpt: 'Building integrations for your enterprise product sounds like a great idea at first, but the challenges can add up fast. Take care with how you build or you build a feature factory.'

tags: 
- 'Product Management'
- 'Enterprise Products'

categories: ['Product Management']

aliases:
- /Enterprise-Integrations/


---
 
If you start building an enterprise product eventually you are going to get asked to start building integrations with other enterprise products. This is ultimately an essential evil.  Your customers already have a host of enterprise products handling the rest of their workflow. Your product is looking to do something with data coming from or going to another part of the business workflow.  No one wants to reenter all of their data into a new system by hand, you need to be part of the ecosystem.
 
When your product is early, you'll be tempted to build point integrations. Early customers will have a product, it'll probably be from a major technology vendor, you might even be using the same product in your infrastructure.  You'll go out, you'll learn some APIs you'll figure out how to batch some data back and forth. Problem solved, deal closed, happy customer. Your next customer comes along and you get another request for another integration point. You'll build that one too. After a few of these you'll decide to build an "extensibility system" or a "module system" or "app framework" to make it easier to build first and third party extensions. People in your organization will dream of becoming a __platform__. You'll start putting things on the road map for your platform ecosystem. But before the app marketplace really catches on you need to seed the environment with the first apps. Now you are going out and finding the integrations people might want. 
 
*__You should stop now.__*
 
This road is a road to a feature factory that you cannot get to run fast enough to keep up with.  Every single integration that you build in this model creates more and more obligations, and will produce more and more tech debt than you want to pay, all by itself.  Each and every product that you integrate with has their own road map.  They are building new features all the time, they will eventually update their API to support the new things they are building. Once they update their API the clock is ticking for you to update your integration to match. You now have other products putting an obligation on you. You have surrendered the initiative, and you have lost some ability to maneuver. 
 
Soon you'll be committing resources nearly full time to keep up with the changes in other people's products.  Some things you won't want to keep up, the customer who originally asked for the integration will no longer be with you, or the integration is no longer ascendant or strategic. But you have it and it's on the website, and a customer or five are using it still.  It will bite your ankles until you drop support. Dropping support is hard and not really supporting something you haven't actually stopped supporting is a bad look.
 
I've been in an organization that had a team that was literally called the "add-on factory". Full time engineers by the dozens that were expected to keep up with all the partners that weren't building their own integrations. 
 
Also beware of building your *__platform__* play too early. Understanding where your software is going to go is hard, even having more than a few customers or partners building on your platform can sap your ability to change and adapt.  If you change your platform integration pattern you have now put all of your partners into the trap that you are trying to avoid yourself.  And the slower they are to adapt your new pattern the longer you need to keep the old one around. 
 
## Watch the Transforms
 
When you start collecting multiple integrations, you will have temptations to build features to shape the data coming into or out of your system. Filters, formats, new items filters, deduplication, and at least once delivery. These are all great, but they add on complexity that you might want to externalize into another system to process.  Depending on the level of assurance that you want to offer that you are doing these things right you can find yourself with hard computer science to do them right. I'm willing to bet that in most cases doing them is not core to your business.  If they were core to your business it's likely they are your business and not an add-on integration.
 
## Constraints to consider
1. __Web standards.__ You can't get yourself into too much trouble moving or reading data from web standard technologies. Supporting web standards will usually make you friends with customers who have a bent towards open source. Depending on how well adopted the standard is there will be more library support in all the colors of the programming rainbow.  
 
2. __Buffers.__ You usually have the option to write directly to the other technology or write to a buffer that the other technology already knows how to read from. Disks are the simplest version of this. You write some files out to disk, \<other software\> reads the data from disk using their "extension framework" and processes it. If you think a little more web-scale you can write to S3 or any number of S3 API compatible services and have other services read from that bucket. Buffers also allow for things to get picked up by automated hooks. Kinesis reads every new file written to a bucket and puts the objects into a data pipeline, and you are off to the races. 
 
3. __Integration Partners.__ There are a host of integration tools out there in the world, from big expensive systems like MuleSoft that have adoption as a corporate priority on their own. On the lighter side you have offerings like IFTTT, Zapier, Microsoft Flow. These have the advantages of you write a few triggers and a few actions and you get access to lots and lots of potential integration points and some level of data transform tool. The downside of these is you may not always have customers who are willing to buy your product and also buy those services too. 

3. __Build the simplest data pump possible.__ When you start pulling and pushing data keep the mechanism of pumping and pulling data as simple as possible. Pick some data formats that line up with as many of the targets as you can; honestly start with JSON. Add more only when you absolutely have to. Keeping it simple until it really hurts to do otherwise.  Be willing to put some hard limits on how you are willing to transform or process data. Give them some options of how they could use other tools to build their Rube Goldberg machine themselves.  If you are going to be part of a Rube Goldberg data processing pipeline, try to be only one step. 

4. __Limits.__ You want to put limits on how much data you are going to push or pull through the system. Think about how you are going to limit the use of the use of the integration. Are you supporting streaming or batch processing? If you are streaming, then think about the rate that you want to support, think about the hardware required to keep that stream flowing. If you have a batch system, how often can you batch, how many concurrent batches will you support, how much data can be in each batch, what version of cron string are you supporting for batch scheduling.  All of this will shape your system architecture and eventually cause you pain if you don't put limits on them early.  Better to say you will only work up to a point early and then grow that number than put no constraints on it and spend support hours trying to solve your customer's scale problems, and building a scale testing tool.
 
5. __Build the integration.__ If the integration is truly strategic you should build it.  If you are adjacent to a market segment with dominant leaders in the Forrester Wave or Gartner Magic Quadrant, then your best option might be to build a real first class integration.  Be a little skeptical when you hear the request, think if you have good options to utilize web-standards or integration partners to stay a little decoupled. But if you are going to build the integration it should be foundational for selling your product for the next 1 to 3 years.