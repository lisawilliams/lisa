---
layout: post
title:  "Building Web-Ready Slideshows With Reveal.js"
date:   2018-03-04 13:35:39 -0500
categories: tech
---

As someone who teaches and does public speaking frequently, I'm often faced
with a problem after I give a talk or a workshop: an inbox and Twitter dash
full of requests from people who want slides and resources associated with my talk.

Often, this involves sending dozens of emails with three or four files apiece.
I regret to say I don't always do the best job -- I would love to say that I
have always responded to 100% of the people kind enough to be interested in my work,
but I know I have missed folks.

After seeing <a href ="http://maptimeboston.github.io/d3-maptime/#/">this web slideshow from a talk on the data visualization framework D3.js</a>, I was impressed by how it worked.

Turns out it was based on Reveal.js, a framework for building HTML slideshows.
Reveal.js allows you to create a single HTML file, from which Reveal builds
an entire slideshow. Unlike Powerpoint, you can nest slides, and using Github Pages,
you can host the entire thing on the web with its own url.

![Reveal.js slideshow showing nested slide controls](https://raw.githubusercontent.com/lisawilliams/email/gh-pages/Reveal-JS-Screenshot-Slide.png)

*Reveal.js slideshow showing nested slide controls -- see the down and left arrows?*

The fact that it is itself a website, and that I can use HTML, means it's easy for me to embed links to resources. Now, when someone asks me 'can I have your slides and handouts'? all I have to do is send them one nifty URL.

Slideshows in fullscreen look exactly like a Powerpoint or Keynote deck, without the browser URL bar, and pressing ESC shows a deck overview.

![Reveal.js slide deck overview](https://raw.githubusercontent.com/lisawilliams/email/gh-pages/Reveal-JS-Screenshot-Overview.png)

I publish and maintain my slides by writing HTML in my favorite text editor (Atom) and pushing them live using git/Github.  That means there's automatically two copies -- one locally and one as a repository associated with my Github account. Not only that, I can use the local webserver utility `grunt` to preview slides locally before pushing them live.

If you'd like to get started using Reveal.js to build your own slideshows, I highly recommend Chen Hui Jing's [excellent tutorial on doing slide decks in Reveal.js](https://www.chenhuijing.com/blog/revealjs-and-github-pages/#%F0%9F%91%9F) to get started.

[Here's the presentation I ended up creating with Reveal.js](http://lisawilliams.github.io/email). It's about creating great email newsletters with user research and data science. 
