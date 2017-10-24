---
layout: post
title:  "Building The Trollbusters Bot"
date:   2017-10-04 11:15:39 -0400
categories: tech
---


<a data-flickr-embed="true"  href="https://www.flickr.com/photos/lisawilliams/23645931338/in/dateposted-public/" title="Trollbusters-Bot"><img src="https://farm5.staticflickr.com/4503/23645931338_dd982df9fd_b.jpg" width="420" height="501" alt="Trollbusters-Bot"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script><br>
*The Trollbusters bot in action*


[Trollbusters](http://troll-busters.com) is the brainchild of Michelle Ferrier, a distinguished journalist and journalism professor. The service offers "just in time pest control for women writers."

<h3>Why Trollbusters?</h3>

*"Almost two-thirds of women journalists polled have experienced intimidation, threats or abuse in relation to their work. More than 25 percent of “verbal, written and/or physical intimidation including threats to family or friends” took place online."*

Both Michelle and I have personal experience with threats and intimidation for our writings. You can read more about what led Michelle to create Trollbusters in
[this interview](https://www.dailydot.com/irl/troll-busters-online-harassment/).

My partner Heather died in March of 2017 of a sudden cardiac arrest. She was an artist, and after [I posted an essay about her life and work online](https://lisawilliams.github.io/lisa/art/2017/03/26/eulogy-for-a-fairy-princess-heather-adels.html), I recieved horrible threats and abuse. They included homophobic slurs, threats of violence, and conspiracy theories.

<h3>Why a bot?</h3>

Bots can provide faster triage and routing, getting people who are the targets of online harassment to relevant resources faster. In addition, a bot can be available 24 hours a day. Online harassment isn't a 9 to 5 business; many incidents happen late at night or in the early hours of the morning. Having a bot available to take users through a triage process to help them get to responses we know work 24 hours a day is something that's useful.

<h3>Planning the Project</h3>

As I do with most projects, I sat down and wrote a project plan to present to Michelle as the head of Trollbusters. My goals were to understand and nail down the following:

* Platform Options
* User scenarios (What do we expect users to do? What do we think they want?)
* User roles (what can each type of user view and do?)
* Wireframes (since this was going to be dictated by Facebook, these were quite minimal)
* Feature list
* Roadmap (what has to be in our "SLC" version, and what might be nice for future versions)

<H3> Platform Choices</H3>

![Vendor choices chart for Trollbusters bot](https://farm5.staticflickr.com/4506/37453468066_fa832c4600_b.jpg)

I'd hoped to use a solution that would provide us with an independent codebase; one that we could pass on to a team of developers should we decide to go further, and one that would provide both independent intellectual property for Trollbusters and insulate the organization from the risk of using a tool from a startup that may disappear. I was also interested in expanding my own skills.

I was initially really enthusiastic about [Botpress](http://botpress.io), an open-source bot-building framework written in Node.js. While I hope to go back to Botpress, I wasn't able to achieve some of our basic version one features with the framework, and deployment was a bit rocky (due in large part to my own skills!). I did get excellent help from Sylvain Perron, one of the founders of the project. You can see a number of fledgling bot project repos in [my public repositories](http://github.com/lisawilliams), if you'd like to browse some code. I'd definitely like to go back and learn more about Botpress when I'm not working toward a deadline.

Ultimately, I went to [TARS](http://hellotars.com), a bot designer tool that Michelle had suggested early on. Creating a branching structure of yes/no questions, which we needed to do for this project, was very easy to do with TARS. As with Botpress, I found that initial deployment and integration with Facebook was a little tricky. Members of the community, including TARS founder Ish Jindal, provided just-in-time help me get deployment details right.

<H3>The Bot Voice</H3>

Many bots are scripted in such a way that they're, well, funny; their creators give the bots a self-deprecating sense of humor, perhaps to distinguish chatbots from the "press one for account information" phone systems that nobody seems to love.

However, Michelle and I both felt that the Trollbusters bot had to have a voice that was reserved, calm, professional in tone. I also made a deliberate choice to keep the bot's questions to users almost exclusively yes/no questions, and made lots of use of predefined buttons that users could click to respond, rather than expecting them to type. Online harassment is upsetting and can be very frightening; I didn't want a user to have to think of how to describe their experience or what to do next. I wanted to keep it as simple and clear as possible.

<H3>The Bot Building Experience</H3>

After tooling around three separate bot platforms for this project, here are a few observations:

* **Deployment and Facebook Integration Are The Hardest Parts of the Project** Regardless of what platform I chose, the hardest parts of the project had nothing to do with the actual core code that defined the interaction between a bot and a user: the hard part was deployment, particularly Facebook integration. Of course, the Facebook API is a moving target, which is challenging for bot platform developers. It reminds me of my experiences with data visualization and data journalism: I often spend more time on data cleanup and setting up an app environment than I actually do making the visualization itself.
* **Heroku is really great, once you get the hang of it.** As part of experimenting with Botpress, I had to deploy a Node.js application to Heroku and hook a Postgres database to it. As I mentioned above, deployment can be the toughest part to master. One of the reasons for this is that often bot tools have features or plugins that don't work on every platform you'd want to deploy on. So when I installed Rivescript, a plugin that allows for faster scripting of bot interactions, I was disappointed to realize that the scripts I'd uploaded disappeared each time I ran `heroku restart` because Rivescript was looking for its own pSQL database, and there were no docs to try to figure out how to get the deployed application on Heroku to have two databases (also, a single app with two databases...for a simple app this just seemed like a bad idea). That said, the ability to quickly provision a new server and connect it directly to an existing code repository, and be able to push new changes to a deployed server with a few keystrokes is pretty amazing. It's also great to have a localhost server and a development server, so you're not pushing changes to the live version all the time; I could try out something locally and only push it when I was sure it was working.

<h3>Future Directions</h3>

The bot is currently live and available at [Trollbusters' Facebook page](https://www.facebook.com/onlinetrollbusters/) by clicking the "Send Message" button. We also have the option to deploy it on the web to Trollbusters' website. We would love to find ways for the bot to operate directly within Twitter, where a lot of the incidents Trollbusters responds to happen. We're also [keeping an issue queue](https://github.com/lisawilliams/TrollbustersBotQA/issues?utf8=%E2%9C%93&q=is%3Aissue%20) to track user feedback and have a place to hold on to ideas for potential enhancements for the bot. If you've got ideas or suggestions, feel free to file an issue.
