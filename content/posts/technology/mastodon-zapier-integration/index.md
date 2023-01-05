---
title: "Create a Mastodon Integration for Zapier"
date: 2022-12-30 13:52:17
draft: false

categories: technology
tags: 
 - Mastodon
 - Zapier
 - Hugo

ShowToc: true

cover:
  image: "" # image path/url
  alt: "" # alt text
  caption: "" # display caption under cover$$
  relative: true # when using page bundles set this to true
  hidden: false # only hide on current single page
---


This site is hosted on GitHub pages using Hugo, mostly because it gives me an excuse to play with very simple CI/CD pipelines and scratch the itch that wishes I was an engineer rather than a product manager. Hugo is nice because it creates the RSS feeds that I love to have and use myself. I have been using that RSS feed to drive automated publishing of new articles to social media through Zapier.  The pipeline looks something like this until just recently

1. Write articles in VS Code on my laptop
2. [Push to GitHub](https://github.com/AndyNortrup/AndyNortrup.github.io/)
3. [GitHub Actions](https://github.com/AndyNortrup/AndyNortrup.github.io/blob/main/.github/workflows/auto-publish.yml) build the static site and host with GitHub pages.
4. Zapier sees the new post in the RSS Feed
5. Adds a new item to Buffer to publish on Twitter and LinkedIn. 

I've left twitter because of *reasons*, and moved to Mastodon. I quite like it and wanted to take some time to update my workflow to stop feeding Twitter my content and start sending that into Mastodon.  Unfortunately neither Buffer nor Zapier have a pre-made integration with Mastodon, so I had to do some DIY.  This seemed like a decent time to refactor buffer out of my workflow entirely. I think it's a great tool, but I don't write nearly enough to use it, and I've never paid for it because I'm not in a marketing department.

{{partial "partials/}}

## Integration vs simple HTTP Actions

I have seen several posts out there describing how to do this with just Zapier's Webhook POST action. But I got to the point where I had to store a credential and I wanted to be sure that my credentials were stored as credentials and not just as a string value.  To be sure of that I took the extra step of creating a full integration. The upside of this is that if I want to make more integrations I can start adding additional actions without having to redo some authentication pieces. 

## Mastodon Setup
The first thing you'll need is to create a mastodon app. In Mastodon settings go to `Development` and create a `New Application`. When you create the account you'll need to grant two scopes. 

* `read:accounts` which will be used to confirm that we have configured authentication correctly.
* `write:statuses` which will be used to create new posts.

After you create the application you'll be provided with a `Client Key` and `Client Secret` which you'll need in Zapier later.  Keep them available for copy and paste.

{{<figure src="2022-12-30-13-12-24.png" caption="A mastodon app with required scopes.">}}

## Zapier setup
You'll need to go to the [Zapier Developer section](https://developer.zapier.com) and click on the big `Start a Zapier Introduction`. Fill out the fields, I didn't worry about most of the values because I wasn't going to publish the integration publically, because I have no official association with the Mastodon project.

After that is done you need to setup authentication. Chose the OAuth scheme. I know OAuth is more complicated, but it's also the best tool out there. 

### Configure fields
I created a field for `Instance`  with a key of `instance`. If I worked a little harder I would have done additional fields for Client Key and Client Secret, but I was running out of nap time.  When I eventually do the additional work I'll be able to create different connections for different mastodon instances that I might some day take part in.  

### Copy you OAuth Redirect URL
Here Zapier is going to give you a redirect URL so that after you login with your mastodon instance you get sent back to Zapier.  Take this URL, go back to your Mastodon developer settings screen and paste it into the field titled `Redirect URI`.  That field likely has a default value of `urn:ietf:wg:oauth:2.0:oob` which you can add to or replace.

### Enter Application Credentials
Back in the Zapier console Step 3 is you'll paste in the credentials you have from Mastodon.  The `Client Key` value from Mastodon goes into the Zapier field `Cliend ID` and the `Client Secret` field goes into `Client Secret` 

### OAuth Endpoint Configuration
Next you are required to add in several URLs from the Mastodon OAuth API implementation.  If you've named your configuration field `instance` like me. You can do some copy and paste here.

* **Authorization URL**: `https://{{bundle.inputData.instance}}/oauth/authorize`
* **Scope**: `read:accounts write:statuses`
* **Access Token Request**: `https://{{bundle.inputData.instance}}/oauth/token`
* **Refresh Token Request**: I left this blank because my single action shouldn't need to refresh.  I can't think of a downside to checking it. 
* **Test**: `https://{{bundle.authData.instance}}/api/v1/accounts/verify_credentials` - This URL will be invoked to make sure that the credentials that we received are valid after login.  

After that you should be able to use the test buttons.  You should get redirected to your Mastodon instance and then bounced back to Zapier after login.

## Create an Action
I've opted to create a single action `Create Post`. Zapier has three tabs for this: Settings, Input Designer, and API Configuration.

### Settings
* **Type**: Create
* **Key**: publish
* **Name**: Create Post
* **Noun**: post

### Input Designer
Here I created a single text field that will be used for my post text.  More work for me might someday be to add a media support to this. To do that I think that I would need a second action to upload and a field in the post action to add the media URL. But again, I'm under a nap time deadline. 

* **Type**: Input field
* **Label**: Content
* **Key**: content

### API Configuration
This is where the magic happens. First set your `POST` request to `https://{{bundle.authData.instance}}/api/v1/statuses`. You'll see that we are grabbing the value of the instance name from the authentication fields. Next you'll need to expand your operations and add both HTTP Headers and a Request Body. 

In the Headers section you need to add one header. `Authorization` with a value of `Bearer {{bundle.authData.access_token}}`.  Again we are grabbing the access token from the authData bundle. Zapier does all authentication for you, all you need to do is grab the access token.

In the request body section add one field `status` with a value of `{{bundle.inputData.content}}`.  If you named your input field something other than `content` use that name here.

{{<figure src="2022-12-30-13-48-40.png" alt="Picture of the Zapier API Request configuration screen" caption="It should look like this!">}}

### Test and Use
After that I was able to test the action and see the post show up on Mastodon.  The final step was to go back to my zap and replace the step to add this to my Buffer for Twitter with the new Mastodon step. 
{{<figure src="2022-12-30-14-02-23.png" alt="Zapier zap step to publish to Mastodon" caption="The step in my zap posting to Mastodon">}}````````