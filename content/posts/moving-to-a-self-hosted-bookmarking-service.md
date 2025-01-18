---
title: 'Moving to a Self-Hosted Bookmarking Service'
date: 2018-01-06
categories:
    - projects
tags:
    - technology
---
# Moving to a Self-Hosted Bookmarking Service

There's a hint that bookmarks are going away.  Services like Delicious that used 
to provide great web-based book marking services have closed down.  In their 
place are the likes of Instapaper and Pinboard and the like that break stuff 
into different types. Instapaper to store sites that you want to read later, 
Pinterest for images you like, and so forth.  That doesn't work well for me, 
though.  I want everything in one place.  That's also why I decided to try a 
<!-- more -->

couple of web-based products.  I realized that I had bookmarks scattered over 
three different browsers, on three different computers. How confusing can it 
get?

## Why Self Hosted? ##

With a variety of services already available on line, why do I want to 
self-host? After all, that's a lot of work to get things set up and to keep 
things running correctly.  It would be much simpler to use a series that 
already exists.

The primary reason is safety.  That is, These services like to shut down without 
a lot of notice.  I don't want to collect lots of bookmarks only to have the 
service shutdown, taking my links with them. I want them to persist.  By hosting 
my own, the only risk is that my computer will die.  I back things up for that 
reason. 

Another reason is privacy.  It's not so much what I'm bookmarking. I don't 
really care if you know what I bookmark.  But I *do* care that you don't try to 
market me, or sell my information to someone else who will market me. When using 
another service, that risk is real -- they do have to make money.  But, by 
hosting my own, I know that can't happen. And, if it does, I get the financial 
proceeds :).

## What Services Am I Using? ##

As I said, these services are falling to the wayside, so there aren't a lot of 
scripts that are still available and being actively maintained.  I found 3: 
SemanticScuttle, Unmark, and Shaarli.  I installed all three so that I could try 
them out to see what works for me.  I'm not sure which one I'll settle one. But, 
I'm already sure which one I won't be using.

Before I get into any specifics, though, let me give you a little background on 
what I prefer. And, where I'm likely going.

*Tags* have been around for a while now and I've rarely used them.  I'll touch 
on that in another post.  I'm a bit old-fashioned and a little linear in my 
thinking.  I like being able to save a bookmark to a specific folder so that I 
can quickly find the list of bookmarks related to a specific subject. Yes, I 
know tagss allow that, and more and, again, I'll talk about that in another post.  
but bear with me for right now.  I wanted something that would allow me to 
import my current bookmarks, maintaining the current structure. None of the 
available scripts allowed this (there is one, but it tried to be too many 
things, I've tried it in the past, and its interface is hopelessly outdated).  I 
also wanted 
to be able to quickly and easily remove duplicates.  And, of course, it had to 
be easy to access and use. Let's take a quick look at the three 
I installed.

## Unmark ##

As I mentioned above, none of the three I found supported folders; all supported 
tagsging, so I ended up going through and tagsging all my bookmarks.  Unmark held 
a lot of promise. I read a lot of good things online about it.  IN practice, I 
wasn't impressed. The biggest issue is that Unmark wouldn't import the tagss 
associated with the links.  That meant I'd need to go through and re-tags all 
those links.  That didn't impress me.  Moving forward, of course, it's less an 
issue.  But, initially, at least, Unmark failed. I've also has some issues with 
Unmark not loading correctly after signing in.  

## SemanticScuttle ##

SS imported bookmarks and tagss without issue.  So far, too, it's been easy to 
use.  I'm still using this one to try to see what it's limits are. So far, 
though, I'm impressed.  The one drawback is that it depends on a MySQL database.  
Now, I've worked with DBs for years and don't' automatically discount a script 
that uses one.  But, I think for my uses, a DB is simply overkill.  It requires 
a lot of resource for little added benefit.

## Shaarli ##

Shaarli and SS are running neck and neck in the which one does Kevin use race.  
From the user perspective, the two are identical.  And, like SS, Shaarli 
imported tagss without issue.  Sweet.  The other thing about Shaarli that I like 
is that it doesn't depend on a database.  It uses a simple XML file to store its 
data.  That not only makes backing up the data dead simple, it also means 
minimal resources.  I could literally copy the files to a new computer and just 
keep going. That is an awesome feature.  Shaarli also allows you tom make short 
notes, or even use it as a pastebin kind of service.  

## Which One Do I Recommend? ##

I don't know yet.  Unlike some folks that spend a day or two playing with a 
service and then making a pronouncement about how good (or bad) it is, I want to 
work with them a while to see which fits into my work flow best.
