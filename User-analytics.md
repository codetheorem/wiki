We use [Google Analytics](https://analytics.google.com/) to track the EOS website. Analytics is added to the page by using [Google's Tag Manager](http://tagmanager.google.com/). Please bear in mind that Ad blockers and script blockers such as [uBlock](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=en) will disable GTM.

---

## Google Tag Manager
Google Tag Manager (GTM) is a tag management system created by Google to manage JavaScript and HTML tags used for tracking and analytics on websites. It listens for events in the page and is able to insert these tags where needed. Its great advantage is that no coding is required in order to add such scripts as it is all handled by GTM itself.

![event_tracking.001](/uploads/1c3f058e2f711d3e196409f795ae137b/event_tracking.001.jpeg)

### Setting up a tag & its trigger
How to set up a tag (Google Analytics)
Thanks to Google Tag Manager, setting up any tag is easy and does not involve writing any code. It's as simple as setting up the event trigger (this could be when a specific page is loaded, when a button is clicked, when there's certain elements on a page...) and then simply we add the tag containing the script.

There are plenty of tracking tools available, but we'll concentrate on using Google's Analytics tool.

Here's a [link to a video](https://www.youtube.com/watch?v=28d60ejfk3s) explaining the basics of GTM and how to set up a tag and its trigger.

## Analytics
Google Analytics is one of the best, free tools you can have for UX research. It collects your website usage data and help you see the result in easy to digest visual manner.

[Brief Google Analytics for beginners tutorial](https://www.youtube.com/watch?v=mreOWm3e9lg)

We've created a Dashboard that digests UX data that is relevant to the EOS project. You can access it from Customisation > Dashboards > EOS UX Analytics Dashboard

![EOS UX Dashboard](https://i.imgur.com/polzCEZ.png)

In order to get a good range of data, we need to set a relevant date range

![Analytics date range](https://i.imgur.com/JALcFsV.png)

### Prevent internal traffic from appearing in Google Analytics
In order to prevent internal traffic (our own visits) we will use a [Chrome add-on](https://goo.gl/1YFNP7). All that is needed is to activate it when loading our [heroku instance](http://eos-test.herokuapp.com/)
