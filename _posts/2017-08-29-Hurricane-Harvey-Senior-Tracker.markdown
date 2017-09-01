---
layout: post
title:  "Building The Harvey Senior Homes Tracker"
date:   2017-08-28 10:51:39 -0400
categories: tech
---

**What is it?**

The [Hurricane Harvey Senior Homes Tracker](http://f.benlk.com/harvey-senior-homes/) is a sortable, embeddable list of nursing home facilities in areas under evacuation notice or affected by Hurricane Harvey. It can be embedded in any web page and is free to use.

![Harvey Senior Home Tracker Screenshot](https://farm5.staticflickr.com/4382/36131071154_1832661c27_z.jpg)

**Can I contribute?**

Yes, absolutely! You also don't have to be technical to contribute. Ben and I concentrated on getting the app and data up and running, but we need people who want to do the outbound calls to to confirm the statuses of the facilities. If you'd like to help, read about how to do it [here](https://github.com/benlk/harvey-senior-homes/blob/master/contributing.md).

If you are a developer, we have a handy tab of issues that you can dig into right [here](https://github.com/benlk/harvey-senior-homes/issues).

**Who built it?**

I noticed [Ben Keith talking about building a web app to track the status of senior homes on the 25th](https://twitter.com/benlkeith/status/901151245456551952), and offered to help. Ben works for the Institute for Nonprofit News, where he helps develop Largo, a Wordpress framework that has been used by dozens of news organizations. I offered to help.

You can find Ben on Twitter [here](https://twitter.com/benlkeith), and me on Twitter [here](http://twitter.com/lisawilliams).

**I work in a newsroom, how can I use this?**

The Hurricane Harvey Senior Homes tracker can be [embedded in a web page](http://f.benlk.com/harvey-senior-homes/embedding.html). It's completely free to use.

Ben and I are not near the affected areas, and have been focusing on getting the app up and running and getting the base data (list of facilities, locations, etc) up and running. We have not made a lot of calls to confirm the statuses of the facilities on the list. That's where you come in, I hope!

You can add information to the tracker -- both adding new locations and updating their status by following the instructions [here](https://github.com/benlk/harvey-senior-homes/blob/master/contributing.md).

**How was it built?**

Ben used the [NPR Apps Template](https://github.com/nprapps/app-template) to bootstrap the project. The project also uses Google Sheets as a backend. You can see the complete source code here. I did work on the back-end data, getting data from Medicare.gov and cleaning/reformatting it for use in the app.

The source code for the project is [here](https://github.com/benlk/harvey-senior-homes).

**Where does the data come from?**

The source data comes from Medicare.gov. You can find more information about the data source [here](https://github.com/lisawilliams/harvey-senior-homes/commit/977698ac1738d0f27c87680b87009fe72e49a208), and if you're interested in how we approached integrating the data into the app, you can read [here](https://github.com/benlk/harvey-senior-homes/issues/2).


**Are there important things I should know before my newsroom uses this?**

So glad you asked! Yes, there is.

*Heavy traffic warning:* Ben and I built this in our spare time and Ben is using his personal web hosting for this. The tracker is not currently set up to handle huge traffic loads and might crash. If you expect to use it in a high traffic situation, contact us (my email is at the bottom of the page) and we'll see what we can do. It is possible to run your own version of the tracker on your own web host, and the source  code is available [here](https://github.com/benlk/harvey-senior-homes).

*Understanding the Data: The Medicare.gov dataset:* I used as the base data has a column on "ownership." Most facilities seem to have seven to ten entries, sometimes more, in this column. The column reflects anything from people who sit on the board, work at the facility, are investors in it. The column contains both the names of individuals and of management companies that own and operate facilities. If you are calling, or want to write stories based on this, it is up to you to dig deeper and understand the relationship of the organization or individual to the facility you are writing about. For more information about the data, read [here](https://github.com/lisawilliams/harvey-senior-homes/commit/89de8d7aef69d4f370404d4d15b212b468ef54ae).
