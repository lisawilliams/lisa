---
layout: post
title:  "Creating a companion RSS reader for my blog"
date:   2017-09-02 11:15:39 -0400
categories: tech
---
![Companion RSS reader for my blog, created using TinyTinyRSS and Heroku](https://farm5.staticflickr.com/4361/36809067462_a9c334467f_b.jpg)

I started blogging in 1999, well before the word 'blog' was commonly known. I remember saying 'blog' to people and having them respond "What?"

One of the things I learned from those early experiences was that writing a good blog came from reading widely. Inspired by [Dave Winer's River of News](http://scripting.com/river), I wanted to create my own river of sources, just like I used to have.

I had hoped to make mine public, the way Dave does. I haven't quite got there yet. The codebase I'm using as a starting point, TinyTinyRSS (ttrss) reminds me a lot of FeedDemon, my longtime favorite desktop RSS app -- it's just that it's hosted on the web. I have to log into it to see anything. The use case is one user reading the most recent updates from their favorite news sources privately. Still, I did manage to get a web-based RSS reader up and running by forking, cloning, and setting up the codebase myself, and I thought I'd document how I did it.

 For those of you who have not heard of RSS, it is a file format that has a machine-readable version of a blog or other online news source's stories. The feed for this blog looks like this:

![screenshot of RSS feed for my blog](https://farm5.staticflickr.com/4341/36145304664_a0f90fe2e9_b.jpg)

Now, that's not something you'd want to read in your web browser -- it's , but it's a structured version of the content of this blog that an application can read.

I chose [TinyTinyRSS](https://git.tt-rss.org/git/tt-rss/wiki), (ttrss), an open-source web-based RSS reader. Since it's web-based, I needed somewhere where the app and my reading list of sites to be. I was hoping not to shell out any additional $$ for hosting, so I was thrilled to find [ttrss-heroku](https://github.com/serl/ttrss-heroku), which allowed me to set up the application on Heroku, an application hosting service with a generous free tier for hobby users and small projects.

After putting it on Heroku, it was, *ta-da!* [live on the web](https://my-fancy-ttrss.herokuapp.com). I began adding a few feeds. One thing I have yet to tackle is automating the update of those feeds; ttrss needs to go read the feeds I subscribe to and fetch any new items for me to read. I'm not totally certain that the automated job scheduler I set up on Heroku is actually working, but I do know how to tell ttrss to update the feeds manually from the command line.

Honestly, I find even that kind of satisfying. Both this blog and my ttrss setup are highly manual. If they were a vehicle, they'd be a dune buggy. I write my entries in a text editor, and commit and publish them from the command line. I enjoy it, and I think I'll enjoy going back to even more of my old-school ways of blogging and reading, just as I did so many years ago. It's good to escape from the massive platforms like Facebook and Twitter, and have a simple and independent existence, thinking and writing out here on the open web. I feel liberated by it. It all still works, and it's all still good.

*Update: the scheduled update task I created on the Heroku server is updating my subscriptions. That's good too ;-)*

*Update update: When I tried to reload my RSS reader, it hung at 'Loading, please wait' until I ran `heroku stop <dyno-name>` and then `heroku restart`. Fascinating.*
