---
title: "Plex Requests"
layout: post
date: 2015-03-11
---
![plex requests]({{ site.url}}/assets/img/plexrequests.png)
<p class="intro"><span class="dropcap">A</span>s I'm sure many geeky data hoarders out there know, <a href="https://plex.tv">Plex</a> is arguably one of the greatest tools to easily and reliably stream your media collection. Be it on your HTPC, your power house desktop, or your mobile phone on the go, it's easy to watch your movies and TV shows. With recent updates it's also just as easy to give close friends and family access to our ever expanding libraries. I know people who use my Plex are avid watchers of everything from the main stream content to quirky indie movies. As the individual hosting the main Plex Media Server the greatest annoyance however is the constant barrage of requests for specific content. Be it a new movie, a failed 1 season TV show, or just an old classic I don't have, the texts and emails never seem to end. This is where Plex Requests comes in.</p>

Plex Requests is my first attempt at actual web development and the application is in it's infancy but the idea is simple: provide an easy to use web application where people can go and search for content and put a request in for it. Those requests can then get automatically processed by content downloaders as well as send notifications to you with the request. This way requests come in and they automatically get searched for without any intervention on my part. My family can request all the Christmas movies they want and I don't have to lift a finger!

The main version of the app is currently written in Django/Python and provides some of the basic functionality with integration for [Couch Potato](https://couchpota.to/) and [PushBullet](https://www.pushbullet.com/). I have also created a simpler version of it written entirely in JavaScript. This simple one page application does not tie into Couch Potato or your current media collection but merely forwards requests on to your PushBullet account. It's much easier to host as it is a single HTML document with a CSS file for styling. I've a demo of it running on [GitHub Pages](http://8bits.ca/plexrequests-js/) to show how simple it is to host.

While Plex Requests is very much a 0.1 alpha, it shouldn't be too hard to get up and running inside a Django project. I've plans to modulate it properly as well as add additional services for other content and properly clean up the code. All the details for it can be found at the various links below!

[Plex Requests GitHub Repo](https://github.com/lokenx/plexrequests)

[Plex Requests JavaScript GitHub Repo](https://github.com/lokenx/plexrequests-js)

[Sample Plex Requests Site](http://8bits.ca/plexrequests-js/)

---

__Legal disclaimer:__ Plex Requests is in no way associated with Plex Inc., and I take no responsibility for what individuals do with it.
