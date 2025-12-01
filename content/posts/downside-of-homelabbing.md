---
title : "The Downside of Home Automation"
date : "2025-09-03T10:48:53-04:00"
#dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "technology"]
categories : ["",""]
showFullContent : false
readingTime : true

hideComments : true
---
# The Downside of Homelabbing and Home Automation


I love learning about home labbing and home automation. I've been homelabbing now for about 10 years.  My fascination with home automation goes back even further to the late 1990s when I first ran across the X-10 technologies. Today you read and hear almost nothing about X-10, even though it is apparently still around.[^1] I didn't do well with X-10 and at the time didn't really have a lot of opportunities or money to play with the technology. More recently, though, I've gotten more into the home automation space. I'm by no means an expert: I just like to tinker. But as I've automated more and more of my home -- lights, HVAC, garage door, etc -- I've also begun to see a downside with all of this. I'll get to that in a moment.
### A Bit of Background

What brought me back to the idea of home automation was my interest in home labbing and self-hosting. One of the more common services that is self-hosted is something like Home Assistant, which is a service for managing your home automation systems. One of the challenges of home automation is the plethora of different technologies and protocols that are in use. It seems like everyone who builds devices for home automation wants to recreate the wheel by also creating their own network or technologies for managing those systems.  From a business perspective that makes sense -- you want to create a situation where the customer chooses (or is forced) to use all of your proprietary systems in order to have a unified system. From the customer perspective, of course, this absolutely sucks because no system is perfect, there are always use cases that require devices not available on a given proprietary system, and so on.  This means that you end up having multiple 'networks' within your home. Home Assistant and its community work hard to minimize that friction and bring everything under one roof.

But I didn't start my home lab journey with home automation. That came later. I started my journey with simple technologies such as web servers, and a few services (rss aggregator, read-it-later apps, and so on) that I found useful and didn't want to pay a company for.  And, as many home labbers argue, I didn't want to trust my data to some unknown entity that may be here today and gone tomorrow. The idea of building a collection of websites or documents or whatever with the intent of using that collection as a resource or knowledge base only to have it disappear because the company went belly-up (or in the case of Google, just deciding to end the service) just didn't set well with me, so managing my own services just made sense.

Starting with a single computer on which I tested or ran a couple of services, today I have a Proxmox server that runs seven or eight LXC containers, as well as a couple of virtual machines. While most of those virtual machines are really just for exploring different operating systems or learning about a specific new technology, at least one of them runs a significant set of Docker containers.  In addition, I run an Unraid server that provides additional Docker containers that provide various services on which I rely. So far, so good.  The truth is, with one or two exceptions, none of those services is critical to anyone other than myself.  But nobody really knows that.

### The Problem

My wife, although she's fairly tech literate, has no clue what services I'm running or on what machines. She knows I have multiple computers in my office and that I've built a fairly robust and complex network, she has no idea how to manage any of this.  Some of this, of course, is my fault. I should be teaching her along the way. But, she's not terribly interested and if she's not working with it regularly isn't going to remember what she's been taught.  And that lack of knowledge is a problem.

You see, I have the lights in the living room, main bedroom, and back porch on a schedule. Should something happen to me, she won't know how to change those schedules. She won't know that the Hue hub in my office controls the lights and, if she unplugs it won't likely 'connect the dots' on why the lights suddenly don't work. For that matter, she won't even recognize it as Hue hub! That's not a diss on her; it's simply that she doesn't know how the system is designed.

She doesn't know what services are running on which computers and won't know which ones she can safely turn off without disrupting the household. And, even if she did have that knowledge, she might not remember how to get into those systems in order to manage them (assuming she wanted to, which I know she does not.) You see the home lab is **my** hobby.  And the setup I've created is for my use and benefit. Again she neither knows, nor wants to know, anything about the systems. And that's a problem.

I strongly suspect that others who have gone down the home lab path or who are becoming increasingly involved in home automation are likely in the same boat.  THEY are interested and engaged but their spouse or significant other is not. As a consequence, they are creating a problem for managing those systems should something happen to them. 

### Is There a Solution?

Well, I'm not really sure. Ideally, your significant other is equally invested in learning about home labbing and automation. In reality, that's unlikely. You can, of course, create guiding documents to aid them in understanding the system, what is running on what computer, what systems can be shut down without affecting the household, and how to manage the systems that do affect the household. But, I'm not sure that's realistic. After all, from day to day, my systems change. I add, delete, and reconfigure my systems fairly often. Documenting all of those changes is a challenge. If you're into labbing at all, I suspect that you do the same things. 

Even if you are keeping up with all your changes and your documentation is up-to-the-second updated, will they know (or remember) how to access that documentation? Will it make sense to them? From years of teaching I know that what makes perfect sense to me may make absolutely no sense to someone not as well-versed as I am in the intricacies of the topic.

Again, I'm not sure what the solution is. But it is something that any home labber should be giving thought to.


[^1]: [X10.com](https://x10.com)

