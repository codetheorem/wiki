![image](https://developers.google.com/open-source/gsoc/resources/downloads/GSoC-logo-horizontal-200.png)

# About EOS Design System

![image](uploads/fe7c791500d57753f652223d9475f0f7/image.png)

Many companies of all different sizes struggle with today's IT agendas: bleeding edge software, agile development, short time-to-market, etc., and this "new" (and really not so) kid on the block is not making it any easier for developer and designers to keep up: UX design. 

Design Systems can help solve this problem, and a few more. Design Systems serve as a centralized source of information for UX, UI, and other brand-related guidelines that help not only developers find the UI element or component they need, but also designers to build faster prototypes while streamlining the collaboration between the two.

At EOS, we are creating the first open source and customizable Design System to help open source, SMEs, and all types of organizations deliver outstanding user interfaces, and consistent user experience cross-products by the hand of the current industry standards.

EOS also created an iconic font made specifically to fit more complex scenarios seen in more technical OSS, as for example endpoints_disconnected, file_system, repositories, proxy, and some other icons not found in the most popular and open source iconic fonts out there.

Our project relies upon several open source technologies:
Python, Node.js, Express.js, Fontforge, Strapi CMS, Bootstrap 4, Pug.js, and others.

# Contacting EOS Design System

Our main communication channel is Slack, although you will need to be invited first to join.
To be invited get in touch with us via any of the following:
- Slack: https://eos-community.slack.com. Request an invite at: https://slack.eosdesignsystem.com/
- Twitter: https://twitter.com/eosdesignsystem
- Gitlab: https://gitlab.com/SUSE-UIUX/eos


# Getting Started

This year, we want GSoC participants to work on EOS-icons. Help us make the most amazing, free and customizable icon set on the internet for open source products working on enterprise software for cloud computing, IoT, infrastructure, operating systems, augmented reality, etc.

Setting up EOS-icons locally is pretty easy. Our readme.md file in our repository explains everything you should do to have the instance running in your machine. It is important that you follow the instructions correctly:

https://gitlab.com/SUSE-UIUX/eos-icons-landing

As you have seen above, we use Gitlab as source control, which is a web runner of GIT (read more about GIT https://git-scm.com/). If GIT is new to you, we recommend you spending 20 minutes in this beginner's course https://www.codecademy.com/learn/learn-git.
We also recommend you using Fork if you use Mac or Windows: https://git-fork.com/. It is an excellent GUI (graphical user interface) to use GIT avoiding the terminal.

To submit a bug, you should simply go to our issues list in Gitlab (https://gitlab.com/SUSE-UIUX/eos-icons-landing/issues) and report in as many words as possible, using examples (images if you can, too), and everything you can so other contributors can understand exactly the issue and how to reproduce it or understand it. Ideally, open a PR to solve it yourself since, according to Python rules for GSoC, you should have submitted at least 1 Pull Request (or merge request as it is called in Gitlab) in order to become eligible for GSoC.

If you would like to submit a bug fix for an already submitted issue, please make sure that the issue has been assigned a label first. Issues with no labels assigned are not yet ready, they are either waiting for a response, have not been read, or are not aligned with the current roadmap. If you opened an issue and would like to start working immediately on it but no label has been assigned, please contact @cynthia in our slack channel and ask her to review your issue ASAP. She's our Product Owner and will try to respond as promptly as possible.

# Writing your GSoC application

The first and most important step to not get rejected is to remember to add the name of our sub-org (EOS) in the title of your GSoC application. Students not adding "EOS" will be rejected by Python.org. More information at http://python-gsoc.org/index.html#apply

Get in contact with the mentors of the project you chose ASAP. The time you wait to get in touch could be the difference between getting selected or going home.

Before even submitting the idea, get a feeling of EOS-icons: clone the repository and get a better understanding of what we're doing. Again, ask as many questions as you want!

Take some hours to read the full WIKI page of EOS: https://gitlab.com/SUSE-UIUX/eos/wikis/home. Yes, we have a lot of pages but they will help you get those Pull Requests merged faster if you understand our coding conventions beforehand.
*NOTE*: all the information in this wiki applies to EOS-icons. We have all of our guidelines in one repo since we apply the same rules and settings to all of our products at EOS in order to have a cohesive codebase across products.

### Application template

* Contact information *

> Name:
> E-mail address:
> Time zone: 
> Other information that may be useful to contact you.

* Synopsis *

> Give us the “elevator pitch“. You have 30 seconds to tell us what you are going to make, why we will like this project, and to convince us that you are qualified to do it! (You might want to write this section last).

* Which of the published tasks are you interested in? What do you plan to do? *

> Detail your idea. Take into consideration the current technologies used at EOS and explain how they can be used, perhaps introducing new ones, to successfully achieve the task.

* What have you done so far with this idea? *

> Research, benchmark with other tools available in the market, analyze the best options, try out EOS, and possibly even make a PR or 2 to warm up with the team.

* Schedule of Deliverables *

> Make a plan. Being disciplined is important and it will help you have a stress-free summer coding amazing features. We won't micromanage you if you haven't stuck to the plan by the hour, it is not the point. We want you to be organized and in sync with the EOS team.

* Tell us about your previous experience * 

> Take the time to tell us about previous work experiences, courses you've taken, open source projects you've contributed to.

* Tell us a bit about you *

> We also want to have a sense of who you are as an individual. At EOS we are young and very energetic. We have artists, musicians, gamers, and all types of people ready to have some quality time on Slack too.

# Project Ideas

## Project 1

**Project Title:** EOS-icons landing page - request icons

**Skill Level:** Easy

**Description:** EOS delivers a set of icons that are made 1-to-1 following Material Design Icons: icons.eosdesignsystem.com. 

**Goals:** We want more people to suggest and request new icons. Currently, we do this by letting people open an issue in Gitlab. An issue we see is that not a lot of people want to sign in to Gitlab to send an issue, they want something faster, within the same interface of EOS. We've benchmarked and https://iconscout.com/unicons uses https://discuss.iconscout.com/ to let their users request new icons. We would like something similar, although simpler.

**Deliverable:** The main objective of this project is to deliver a web interface for EOS icons that allow users to request new icons in an easy and intuitive way. The interface should have 2 types of users: 
- admins: EOS maintainers would have access to this account to be able to leave comments, resolve, close, and revision requests before they become visible for the rest of the users.
- user: any user should be able to submit a request providing certain information so our designers have data enough to process the request. Ideally, the user should be able to opt for leaving an email address or a twitter user to contact them [more ideas welcome].

**Mentors:** [Cynthia Sanchez](https://twitter.com/cyntss), [Sorin Curescu](https://twitter.com/en3sis), [Kartikay Bhutani](https://twitter.com/kbhutani0001), [Abhinandan Sharma](https://twitter.com/abhinandan0659).

**Skills:** SCSS, Bootstrap 4, Pug.js, CI Heroku, Headless CMSs, some DB.

**Get started:** Make some researches before submitting your application. Read about some CMS, forum tool, etc. There is always something out there that we can re-use to not re-invent the wheel and save ourselves some time. Most likely, you will find a tool we can use. You will have to play with it and plan on spending some time to assemble things together, deploy a server in heroku, have a database functioning, and most importantly, have a nice UI and user experience working.

## Project 2

**Project Title:** Animated icons and icon customization.

**Skill Level:** Easy

**Description:** EOS-icons delivers a set of icons in an iconic font that makes it really easy for web developers to implement into their products given that all they have to do it download (or CDN) the font and then simply use ligatures in their `html`. It also delivers a few animated icons. These icons were created with SVG with SMIL animation on top (pure code).

**Goals:** While an iconic font is really efficient for web platforms, installable software struggles more with this solution. For developers working on products like plugins or executable files it is more efficient to be able to get a `.PNG` or `.SVG` of the icon.
For animated icons we need to extend the number of icons available and also have a customization option to let users change the color of the exported SVG.

**Deliverable:** 
- Allow users to download a `.PNG` or `.SVG` of the icon of any of the available icons in EOS-icons (including the extended version). The user should be able to download the icon in the most commonly used sizes (please research and propose the best sizes), as well as in the color they wish (see https://www.flaticon.com/free-icon/home_25694?term=home&page=1&position=4 to get some ideas of customization).
- Create more animated icons. Research use cases, discuss it with the community and increase the number of animated icons using SMIL animation in SVG. The animated icons should be color customizable. Given that they are SVG vectors, users don't need the file in different sizes, only 1 size. Our designers will help you with the graphic design of the icon.

**Mentors:** [Cynthia Sanchez](https://twitter.com/cyntss), [Sorin Curescu](https://twitter.com/en3sis), [Kartikay Bhutani](https://twitter.com/kbhutani0001), [Abhinandan Sharma](https://twitter.com/abhinandan0659).

**Skills:** Python, Gulp, Pug.js, SCSS, Bootstrap 4, SVG SMIL, Javascript/Jquery.

**Get started:** Read about Gulp https://gulpjs.com/, 60% of the project will be around this library. Make sure your Javascript skills are good to handle real-time customization. Do your part of benchmarking by visiting and exploring https://www.flaticon.com/free-icon/home_25694?term=home&page=1&position=4 and their customization tool.

# Useful links:

- Basic instructions to setup and use GIT in open source:

https://gitlab.com/SUSE-UIUX/eos/wikis/GSoC-basic-git-instructions

- Javascript conventions we follow at EOS:

https://gitlab.com/SUSE-UIUX/eos/wikis/Writing-standard-JS-code

https://standardjs.com/rules.html

https://gitlab.com/SUSE-UIUX/eos/wikis/code-commenting-standards

- CSS conventions:

https://gitlab.com/SUSE-UIUX/eos/wikis/Editing-css-style-guide

https://gitlab.com/SUSE-UIUX/eos/wikis/CSS-structure

https://gitlab.com/SUSE-UIUX/eos/wikis/code-commenting-standards

- How to name your branches:

https://gitlab.com/SUSE-UIUX/eos/wikis/naming-conventions-for-new-branches