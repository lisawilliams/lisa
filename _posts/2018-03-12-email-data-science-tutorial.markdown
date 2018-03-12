---
layout: post
title:  "Email Data Science Tutorial: Setting Up & Using The Shorenstein Notebooks"
date:   2018-03-12 01:31:39 -0500
categories: tech
---

Most email analytics are, to put it mildly, not very good.

The guidance given to us by numbers like open rate or click-through rate often encourage a kind of passivity: too many of us watch our numbers like they are the weather -- just something that happens to us.  Or, if we are acting in response to our analytics, we are going on very slender evidence that we know why a particular day's numbers were good or bad.

In 2017, along with a team at WBUR, I launched The Magic Pill, an audio newsletter that won the Edward R. Murrow Award for Excellence in Innovation. We chose email over other delivery platforms because we knew that email would give us much more data about who our listeners were and what they liked than iTunes did. Still, at the time, I would have loved to have known more about subscriber behavior than I was getting at the time from Mailchimp.

That's why I was excited to read The Shorenstein Center's paper [Using Data Science Tools for Email Audience Analysis: A Research Guide](https://shorensteincenter.org/wp-content/uploads/2017/10/Data-Science-Tools-for-Email-Analysis-Research-Guide.pdf?x78124), by Jacque Boltik and Nicco Mele. I was even more excited to see that they had provided a set of tools so that we could do the analysis they talked about in their paper with our own data.

This post is intended to be a guide to setting up and using those tools. It is especially aimed at the technologically curious person who works on an email product, but has little experience with data science tools or coding. Beginners welcome here!

### Tools We Will Use

This guide is written from my POV as a Mac user, but many of the basic tools will work on Windows, and of course on Linux. I regret that I can't give line-by-line instructions for those platforms, however.

**Terminal** We will be using the command line for this tutorial.

**Git and Github** The files we use to do our data science experiments are located on Github.com, a code sharing and collaboration site, and we will use the version control system, Git, to get them down onto your computer.

**Anaconda** The Shorenstein Notebooks use Python, so we will download a distribution of Python.

**Jupyter Notebooks** These can read the Shorenstein notebook files. It comes with Anaconda.

You will also need a modern web browser. I am using Chrome Version 65.0.3325.146 as I carry out the steps of this tutorial.

### Getting Started

#### Download and Install Anaconda

If you don't know if you have Anaconda installed, open up Terminal. You will find Terminal in the utilities folder. Type `conda --version`. If Anaconda is installed, it will give you a response like `conda 4.3.30`. Check on the [Anaconda website](https://www.anaconda.com/download/#macos) to see if you have the latest version. If you get no response, you'll need to [download Anaconda](https://www.anaconda.com/download/#macos) and install it.

#### Get a free Github account

If you do not have one already, you will need a free [Github.com](https://www.github.com) account.

#### Download and install Git

First, check to see if you already have Git installed. Back in Terminal, at the command line, type `git --version`. If it is installed, you'll get a response like this: `git version 2.11.0 (Apple Git-81)`. If you don't have it, it will prompt you to install it.

#### Fork and Clone the Shorenstein Notebooks and Sample Data files

If you've never heard the phrase 'fork and clone' before, don't be worried. It just means you're going to make your own copy of the notebooks on your Github account, and then 'clone' those files down onto your local computer using Git.

Visit the [email-data-science-tutorial repository](https://github.com/lisawilliams/email-data-science-tutorial) I set up on Github. This repository contains Jupyter Notebook files created by the team at the Shorenstein Center, as well as sample data files of email list subscriber data. In the upper right hand corner, you will see the Fork button:

![Fork button](https://git-scm.com/book/en/v2/images/forkbutton.png)

Click the Fork button. You'll notice a cute animation, and then you will be taken to your own copy of the repository. You'll know if it worked if the URL for the page is `http://github.com/yourusername/email-data-science/`

Once you arrive there, you will see another button that reads 'Clone or download.' Click that, and then copy the URL you see in the window that pops up:

![Clone and download from Github](https://raw.githubusercontent.com/lisawilliams/email-data-science-tutorial/master/clone-and-download.png)

#### Unzip the Sample Data File

At the command line, type `ls`. You should now see a folder titled `email-data-science-tutorial`. To change into that directory, type `cd email-data-science-tutorial` at the command line and hit return.  Once you are in the folder, type ls again. You will see the notebook files and the sample data files. One of the sample data files is quite large, and you will need to unzip it before continuing. The file is called nb2_anon.pkl.zip.  If it works, you will get a response like this:

```
Archive:  nb2_anon.pkl.zip
  inflating: nb2_anon.pkl
   creating: __MACOSX/
  inflating: __MACOSX/._nb2_anon.pkl

```
Type `ls` again at the command line, and you'll notice you have a file called nb2_anon.pkl.

#### Run Jupyter Notebooks

It's time for the magic! Type `jupyter notebook` at the command line. Your browser should open a new tab, and if all goes well, you should see something like this:

![Jupyter Notebook open screen](https://raw.githubusercontent.com/lisawilliams/email-data-science-tutorial/master/Jupyter-notebook-open-screen.png)

Click on the first Notebook file. You'll get a new tab that looks like this:

![Shorenstein Notebook #1](https://raw.githubusercontent.com/lisawilliams/email-data-science-tutorial/master/Jupyter-notebook-open-screen.png)

#### Scroll and Explore

Scroll down to explore how the notebooks slice and dice the data. Be sure to open both notebooks -- they show very different views of the same subscriber data! For a full explanation of what you're seeing, read [the accompanying paper from Shorenstein](https://shorensteincenter.org/wp-content/uploads/2017/10/Data-Science-Tools-for-Email-Analysis-Research-Guide.pdf?x78124) for a full explanation

#### Shut down your notebook kernels before leaving

At your notebook home screen -- the one with the list of files -- you'll see a tab called 'Running'. Click this. Shut down any running kernels or they will run in the background and take up your CPU.

Then, visit the command line and shut down the Jupyter Notebook application by typing `Ctrl-C`.
