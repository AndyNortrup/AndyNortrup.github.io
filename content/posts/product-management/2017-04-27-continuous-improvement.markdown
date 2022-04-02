---
date: "2017-04-27T00:00:00Z"
excerpt: I listened to a great episode of [Deliver It](http://deliveritcast.com/)
  on [DevOps for Product Owners](http://deliveritcast.com/ep49-devops-for-product-owners)
  and a comment by the [Lee Janson](https://medium.com/u/ea6cf58a5883) that you don’t
  have to have perfect DevOps practices right away really struck home with me. Upon
  reflection it exactly maps to the evolution that my team has been going through
  over the past year on our developer tool [Splunk AppInspect](https://dev.splunk.com/goto/appinspect).
tags: 
- 'product-management'

categories: 
- 'Product Management'

aliases: 
- /continuous-improvement/

type: post
title: Continuous Improvement — A journey
---

I listened to a great episode of [Deliver It](http://deliveritcast.com/) on [DevOps for Product Owners](http://deliveritcast.com/ep49-devops-for-product-owners) and a comment by the [Lee Janson](https://medium.com/u/ea6cf58a5883) that you don’t have to have perfect DevOps practices right away really struck home with me. Upon reflection it exactly maps to the evolution that my team has been going through over the past year on our developer tool [Splunk AppInspect](https://dev.splunk.com/goto/appinspect).

AppInspect is a tool that has grown tremendously in my year with Splunk from a something we built for internal assessment of apps that applied for our [Certification Program](http://dev.splunk.com/view/app-cert/SP-CAAAE2S), to a tool publically available that as both a standalone CLI tool or through an REST API.

We are really excited about what the product is and does. But, my team’s journey with it has been a great example of continuous improvement of both product and practice, and is perhaps a more interesting story than what the product itself does.

#### The Infant: A CLI tool for our own team

Appinspect was born out of necessity when the team took over the App Certification it was more popular than the initial resources could handle and a backlog of apps had collected. The first essential task was to automate evaluation of app quality. With basic automation in place we were able to quickly establish which apps were ready for careful review and which ones could be sent back to the developer for further development.

AppInspect drew strong inspiration from the unit testing tools that we loved and is written in Python 2.7 to line up with Splunk and most Splunk development. Building a CLI test suite allowed us to greatly reduce the amount of work to determine some aspects of quality for apps. This saved us a lot of time and money, which is good, but it didn’t fix all of our problems.

#### The Toddler: I need this on Windows

As the certification program grew in popularity we needed to split out responsibilities for our work so that the engineers doing code reviews and development on the tool didn’t also have to run the tool and send the results back to our customers. To do this we brought on a contractor to help manage workflow and communications with developers.

Unfortunately she worked on a Windows computer, and we were dependent on some of the *nix utilities of our development environment, like the “file” command to test permissions and docker for running dynamic tests in a sandboxed environment. Rather than reduce features to put the tool on Windows we moved forward and built a web-app for internal use that allowed our contractor to run reports on her own and send well formatted reports to our developers.

This first web tool was by no means a web-service or an API. It was a very simple tool built with Flask, it did all of the work server side and output the results. But it was progress, with a web UI we were able to provide a cleaner format for results than a text file.

From a DevOps perspective this was also our first separation from the developer and the users. This is the point that we introduced releases and release management to our process. When we had a simple CLI it was very simple for a developer to write a new test and have it almost immediately show up in the next run. With our web tool we now had to write, build, test and deploy to a server. Releases were infrequent, in part because they were manual. But also they remained manual because we had a slow release cycle.

#### The Terrible Twos: Let’s make this public

Adding the web tool was an enormous success for us, it helped us get data back to our customers much faster so that they could make changes and improve their apps. Unfortunately a better process is still not a perfect process. At this point we had a nice web tool but only if you were on our team and only if you were on our intranet. Additionally the feedback mechanism was slow. Developers needed to upload their app to our app store, we needed to see that there was a new version, we needed to test the app and send them results by email (*cringe*).

The way ahead was clear, we needed to enable our customers to submit apps themselves and get feedback without ever talking to us. To do that we needed to turn our simple Flask app into a proper REST API and make it publically available.

Along the way we picked up additional stakeholders. [Splunk Add On Builder](https://splunkbase.splunk.com/app/2962/) wanted to be able test add-on against our best practices before developers finished development and internal development teams wanted to test apps as part of their build and release process.

This was a great validation of what we were doing, but it put us on a timeline, we needed to have the API out the door in time for Splunk’s .conf2016, when the next version of Add On Builder was set to ship.

The good news is that we made it. The bad news is that we accumulated some technical debt in the process that made CI/CD, debugging and testing much harder.

#### The Threenager: This monolith is becoming a bit cumbersome

As we grew the initial version of our API we had a single repository that contained all of our docker half dozen docker images and the docker compose files that spun it up into a service. Additionally our dockerfiles were a little beefy, all built around Ubuntu, which has everything you need but probably a lot of things you don’t need.

It worked, but it was a burden to develop around. A single build of the repository could take an hour. That wasn’t a great flow for our developers and it really wasn’t popular with our build tools team that all of our commits tied up our shared build server for a significant amount of time.

Not only was it a pain to develop for, it was a pain to deploy. And because it was a pain to deploy into production. Because it was hard to deploy we waited to deploy updates until we had a lot of things worth putting into production. Because we were deploying big chunks we were gun shy about testing all of the changes.

The solution is what we call the “great refactor”. We staked out a full two and a half weeks to break out every container into it’s own repository. At the same time we were able to consolidate on a single base image based on Alpine. Using Alpine ment that all of our images were super small, and fast to build. Even better because we were using a common base image for the project the only thing we had to build was the changes between containers. This has been great for us for a lot of reasons.

1. Faster builds. Right now our longest build is about 1:30.
2. Individual unit tests for each container.
3. Individual versions for each container meant that we could do integration tests that only reflected changes in a single component.
4. Merges got easier.
5. The ability to deploy an individual components
All of these things made it much easier to deploy, in fact it made it easy to deploy.

#### The Preschooler: Automate build and test

Around the time that we did our refactoring we also were allocated a dedicated QA resource. We had build thousands of unit tests to support validation of individual checks. What we gained a specialized QA resource was someone helping to build more comprehensive end to end, integration and system testing.

Not only did we get more actual tests, we gained test and build automation. This change meant every commit to our development and master branches and all pull requests kicked off our test suite. This greatly increased our confidence in merging and deploying.

More confidence meant that were more comfortable merging and deploying with frequency. With confidence came speed of delivery which allowed us to ship new solutions, and solve problems faster for our users.

#### The Kindergartener: Let’s make get better with data

The refactor of our API provided us an opportunity to get more feedback about our App. One of the best things we did for ourselves was to start gathering our application data into our corporate Splunk server. Onboarding this data allowed us to drastically improve our ability to debug and monitor the environment.

The entirety of our application runs inside of Docker, so we are able to use the [Splunk logging driver for Docker](https://docs.docker.com/engine/admin/logging/splunk/) to collect all of the application logs and ingest them in Splunk. With this information in hand we were able to gain critical knowledge about our app’s performance and information about how developers were using our service and the Splunk platform. We can now:

1. Trace the entire flow of a request through the system
2. Identify checks that fail disproportionately and target changes in the platform, documentation or check
3. Identify how much areas of the Splunk platform are used to drive marketing, development and documentation changes
4. Debug issues with the API
5. Monitor the performance of the API
6. Understand user behavior and usage
#### The Grade Schooler: Automated deployment and monitoring

The next step in our journey is to begin doing truly continuous deployments and improving our monitoring processes so that we not only have confidence before we build, but we have confidence after we deploy that services are running.

Our primary vehicle for monitoring will be Splunk’s IT Service Intelligence product which allows us to define all of our services and associate KPIs to them and monitor their performance continuously. Using ITSI’s built in machine learning tools we will be able to set thresholds automatically based on prior usage.

I’ve framed this article as a journey rather than a set an executed plan because I don’t think it will ever truly end. Just like children the service will continue to grow and evolve, and we will update our practices and tools to keep pace with new demands.

Most importantly we have learned that we need to be continuously aware of our pain points interrogate those challenges to determine what the cause of the problem is and how it can be resolved.

## 2022 Update
AppInspect is now used for every single Splunkbase upload and some failures are blocking for all apps.  This is one of the fullest visions we had for the service as we were designing it. It's nice to see products you've built carry through to their full potential even after you've left.

AppInspect also served an important role in helping Splunk and it's partners find and update a lot of Python 2 as it was being removed from the platform. 
