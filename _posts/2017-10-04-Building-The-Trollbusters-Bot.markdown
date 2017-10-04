---
layout: post
title:  "Building The Trollbusters Bot"
date:   2017-10-04 11:15:39 -0400
categories: tech
---


<a data-flickr-embed="true"  href="https://www.flickr.com/photos/lisawilliams/23645931338/in/dateposted-public/" title="Trollbusters-Bot"><img src="https://farm5.staticflickr.com/4503/23645931338_dd982df9fd_b.jpg" width="420" height="501" alt="Trollbusters-Bot"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script><br>
*The Trollbusters bot in action*


[Trollbusters](http://troll-busters.com) is the brainchild of Michelle Ferrier, a distinguished journalist and journalism professor. The service offers "just in time pest control for women writers."

*"Almost two-thirds of women journalists polled have experienced intimidation, threats or abuse in relation to their work. More than 25 percent of “verbal, written and/or physical intimidation including threats to family or friends” took place online."*

Both Michelle and I have personal experience with threats and intimidation for our writings. You can read more about what led Michelle to create Trollbusters in
[this interview](https://www.dailydot.com/irl/troll-busters-online-harassment/).

My partner Heather died in March of 2017 of a sudden cardiac arrest. She was an artist, and after I posted an essay about her life and work to honor her online, I recieved horrible threats and abuse.

After my partner died, I took the summer to recuperate and took a 12-week web development intensive offered by [General Assembly Boston](https://generalassemb.ly/). Since then I have created several things on my own or with others, including the [Hurricane Harvey Senior Homes Tracker](https://lisawilliams.github.io/lisa/tech/2017/08/28/Hurricane-Harvey-Senior-Tracker.html), and my latest project, the Trollbusters Bot. The Trollbusters Bot helps women experiencing online harassment find the resources Michelle has created at Trollbusters as quickly as possible.

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

Initially, I'd hoped to use a solution that would provide us with an independent codebase; one that we could pass on to a team of developers should we decide to go further, and one that would provide both independent intellectual property for Trollbusters and insulate the organization from the risk of using a tool from a startup that may disappear. I was also interested in expanding my own skills.

I was initially really enthusiastic about [Botpress](http://botpress.io), an open-source bot-building framework written in Node.js. While I hope to go back to Botpress, I wasn't able to achieve some of our basic version one features with the framework, and deployment was a bit rocky. I did get excellent help from Sylvain Perron, one of the founders of the project. You can see a number of fledgling bot project repos in [my public repositories](http://github.com/lisawilliams), if you'd like to browse some code.

Ultimately, I went back to [TARS](http://hellotars.com), a bot designer tool that Michelle had suggested early on. Creating a branching structure of yes/no questions, which we needed to do for this project, was very easy to do with TARS. As with Botpress, I found that initial deployment and integration with Facebook was a little tricky. Members of the community, including TARS founder Ish Jindal, provided just-in-time help me get deployment details right.

<h3>Future Directions</h3>

The bot is currently in review for approval at Facebook. Once it is deployed, it will be available to people who visit [Trollbusters' Facebook page](https://www.facebook.com/onlinetrollbusters/) by clicking the "Send Message" button. I also hope to deploy it on the web to Trollbusters' website. We would love to find ways for the bot to operate directly within Twitter, where a lot of the incidents Trollbusters responds to happen.
