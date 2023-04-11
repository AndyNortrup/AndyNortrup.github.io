---
date: "2020-05-13T00:00:00Z"
excerpt: Solid Pods (Personal Online Data Store) are an open source project from the
  efforts of Sir Tim Berners-Lee (creator of the original internet) with a goal of
  re-decentralizing the internet.  This project is still in development, I think it
  has a lot to offer in order to help make developing web applications easier and
  safer for the developer, user, and society at large.
tags: 
- Technology 
- 'Open Source'
  
categories: 'technology'

aliases: 
- /solid-pods/

title: Solid Pods - A better place to store user data
---
 
[Solid Pods](https://solidproject.org/) (Personal Online Data Store) are an open source project from the efforts of Sir Tim Berners-Lee (creator of the original internet) with a goal of re-decentralizing the internet.  This project is still in development, I think it has a lot to offer in order to help make developing web applications easier and safer for the developer, user, and society at large.
 
Solid provides a web standard's compliant API to provide the owner of the pod with an identity (WebID), storage (document store), and relational language for data.  Applications can be built to access and store data in the pod, rather than in storage systems owned by the application.  
 
## You don't want to store your customer's data
 
In the beginning there were web pages and they were good. Then customers wanted to have web pages that had data that was specific to them.  The web portal was born it works but from a privacy standpoint it has been going downhill for customers and the companies that are storing this data.
 
The conventional wisdom is that storage is cheap, which makes it easy to store data about your customers. In today’s world you should be asking yourself, just because I can, should I.  The real cost of data is in the [liability of keeping it](https://themargins.substack.com/p/the-secret-liabilities-of-data).  The average cost of a data breach in 2019 was [$3.29 Million](https://securityintelligence.com/posts/whats-new-in-the-2019-cost-of-a-data-breach-report/).
 
Even if you manage to keep all of your data under lock and key, you will face a growing number of privacy process challenges for the data.  Right now any EU citizen can make a subject access data request to you through the General Data Protection Regulation (GDPR).  Each of those requests are costing businesses on [average $1400 per request to process](https://www.gartner.com/en/newsroom/press-releases/2020-02-25-gartner-says-over-40-percent-of-privacy-compliance-technology-will-rely-on-artificial-intelligence-in-the-next-three-years). 
 
It isn't just the EU other countries and states are moving in that direction.  Brazil's privacy law closely matches the GDPR to stay inline with Portugal. Japan has adopted legislation that is also very similar to Europe. In the U.S. California has adopted the California Consumer Privacy Act (CCPA) and 40% of Americans are covered by some form of state privacy law.  There is significant debate what shape a federal privacy law will take, but that is more about what type of law we get rather than if there will be a law. 
 
If the actual administrative, legal and reputational risk of storing data isn't enough; having large stores of data increases national security risks as well.  As recently highlighted by the [Cyberspace Solarium Commission report](https://www.solarium.gov/report) every website that becomes a target decreases the overall national cybersecurity posture. We already have large examples of IT systems at Marriott being attacked by likely state intelligence services in order to get a rich set of data about the travel patterns and personal preferences of Americans and particularly the U.S. government employees that stay in their hotels for work and pleasure.
 
You might tell yourself, this won't happen to me. I run a tight ship and take security seriously.  Don't count on it.  Every web connected anything is open to attack from well financed, trained and organized state and organized crime groups.  There are more smart people out there with a motivation to attack you than there are engineers you can hire to protect yourself.  Read enough [Krebs on Security](https://krebsonsecurity.com/) and you will realize that breaches happen to everyone, they happen to large smart companies and the folks who thought they were small enough to fly under the radar.
 
## The safest way to live is to have nothing to steal
 
How do Solid Pods help solve this problem? Right now identity on the internet looks a lot like this:
 

![Fractured Internet with individual accounts at every website](/images/posts/technology/solid-pods/fractured-internet.png)
 
No individual has a standardized identity on the internet or storage system, each website forces you to create a new one every time.  Even worse, many web-sites have to implement storage of these identity systems from scratch.  Many of the big players (Google, Facebook, Apple, Microsoft, etc.) have allowed you to federate authentication using their existing identities,  but that requires you to share data with those companies about who is using your service, frequently feeding them the data on how to compete with you. You can (and probably should) pay for someone else who has implemented identity systems already (Auth0, Okta, etc), doing it yourself is not advisable.
 
Regardless of how you implement it, every web-site you go to forces you to create another identity, password and slowly collects some amount of data about the user. That data is likely repeated over and over for every website. You enter your shipping and billing addresses from every commerce transaction, then have to update those when you move. I moved more than a year ago and am still finding websites that still have my old address listed.  I still get mail at my house for the old owners.  Your data is in bits and bobs all over the internet. 
 
I love 1Password (really you should use a password manager); but the fact that I have a product to keep track of and secure 389 logins that I'm aware of on the internet right now, is an indication that the internet is broken.
 
### **It. Doesn't. Have. To. Be. This. Way.**
 
In a world with Solid the internet instead looks more like this:
 
![Unified Identity and Data Storage with Solid](/images/posts/technology/solid-pods/solid-unified-identity.png)
 
You have one identity, provided by your solid pod.  When you go to a web-site you grant it permission to show you your data from your pod. When you leave the website, they no longer have access to your data. Even better when you go to a new website, you don't have to re-enter all of that data, you have already filled in the shipping address field on your identity, applications can simply read that.
 
The underlying technology is still early and has some clear growing that it needs to do.  But I think it offers an interesting potential solution for both enterprise and consumer software.
 
In the Enterprise data owners get a big step forward in data ownership and control.  You have to trust your SaaS vendor less when you own and control the data. For developers it provides an opportunity to move enormously difficult parts of every compliance attestation, outside of your compliance boundary.
 
Right now if you want to avoid getting a PCI attestation, you use Stripe, you never touch the credit card data and avoid a boat load of problems.  If you applied the same theory to user authentication, authorization and data storage, you could eliminate entire categories of compliance problems.
 
* Encrypting data at rest, nope you never touched the data.
* Backups, nope never had anything to backup.
* Backup restoration testing, all I need to do is redeploy the single page app.
 
A smaller compliance boundary means that you can gain attestation with less effort for significant payoff.  Many enterprise customers won't talk to you unless you have at least an ISO-27001 cert, and that is the bottom rung.  Every standard you add on opens your potential customer base more.
 
On top of that you no longer need to invest in building or integrating then operating and monitoring the systems that are required for authentication, authorization and storage.  That means you can move faster on core product improvements and either charge less or have improved margins.
 
For consumers software Solid allows you to significantly minimize the regulation of consumer privacy on your business.  In the ideal world, when a user shows up to your site, the only thing you know about them is the address of their pod, even that could live in their browser.
 
Similar enterprise software you now get to focus on your product rather than lots of web-scale infrastructure and the engineers required to maintain that infrastructure.  Ben Thompson of Stratechery has [written](https://stratechery.com/2019/portability-and-interoperability/) extensively about the impact of regulation to reinforce the position of the Big Cos. The short version is that everyone collects data on their users, the data gets mis-used by the big companies, governments create regulations with the intent of making sure the big companies behave and user privacy is respected.  The outcome however is that you need a lot of infrastructure, legal and investment to follow those rules. Meaning big companies are in the best position to make those investments and everyone else goes away because they can't afford to follow the regulation and build a product.
 
If you don't have any data, you don't have to pay as many lawyers or compliance engineers, and you aren't actually running the infrastructure to store the data, then your operations cost just went way down.  Lower costs make you more competitive.  Yay!
 
 
### Other tricks
There are some other tricks in the Solid universe. If a user has all of their data in one location multiple apps can re-use and enrich the same data.  This helps solve some portability problems and potentially decrease time to value for your users. There is also a rich and extensible language for defining relationships between pods.  Meaning you can create social relationships without having to tap into Facebook. 
 
## The way ahead - Chicken meet Egg
 
Solid might be nice tech but it is going to need some decent applications.  Before people use the application they will need to get a pod.  There are currently some applications, but most of them appear to be more playground work than production ready. 
 
In order to use the applications, users will need to have a solid pod.  The pod providers are going to be picking up the responsibility for securing your data, I personally would want the pod provider to have their compliance ducks in a row.  My personal preference would be to know that my pod provider can't read the contents of my pod, that all pods are cleanly separated, plus all of the backup and restoration things.
 
There are currently a smattering of [providers](https://solid.github.io/solid-idps/), but none of them quite feel like something I would pay for yet. Inrupt's own service lists itself as a prototype. ¯\\\_(ツ)_/¯
 
I could see some of the following companies being strategically aligned with adding a pod hosting option to their services.
 
* Identity Provider solutions (Auth0 or Okta) are already in the authentication technology space and already have strong relationships with the enterprise software landscape. Adding Solid would be an extension that would allow them to serve more of their customer needs. And provide an OAuth + Solid developer pattern in addition to an OAuth + SCIM pattern that is common today.
* Password Managers (1Password, LastPass, Dashlane) are already in the business of selling users secure containers for their most personal data.  They also have some Enterprise and SMB relationships. Add Solid would extend their ability to contain more data than just passwords for their users. 
* Apple has made a particular strategic lift in the past several years to make themselves the company that cares about your privacy and data.  Most significantly they added [Sign In with Apple](https://support.apple.com/en-us/HT210318) for login.  Adding Solid support would allow them to add a developer layer on top of iCloud storage that provides more privacy protection than an obfuscated user id.
* AWS/Azure/GCP - If you were a business looking for a Solid provider, then you would probably hope that one of these companies provides it.  They probably already hold a bunch of data for you, and they are highly competent at running data centers. 

