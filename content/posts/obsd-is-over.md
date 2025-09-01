---
title : "My OpenBSD Experiment Is Over"
date : "2025-09-01T13:44:23-04:00"
#dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : ""
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "technology"]
categories : ["",""]
showFullContent : false
readingTime : true

hideComments : true
---
# My OpenBSD Experiment is Over

Well, this is a day that  I really wasn't quite expecting.  I had high hopes that I would be able to use OpenBSD for quite a while before moving on to another OS but, alas, that was not to be.  I am writing this on Linux Mint, having returned to that after my experiment. To say that I'm a bit sad about this state of affairs is an understatement.

So, what happened? Well, there was nothing Earth shattering that led to this decision. Rather, it was just an accumulation of little annoyances and challenges that finally forced me to rethink my approach.

I came to OpenBSD having initially set out to install FreeBSD on the 10 year old Lenovo X250 that I bought for that purpose. That is, I had initially set out to experiment with FreeBSD on a laptop. That effort and the challenges I encountered are chronicled in [this]({{< relref "/posts/freebsd" >}}) post.  As I noted in that post the biggest challenge was the suspend/resume process when closing the lid on the laptop. While FreeBSD would suspend correctly waking up was a different experience. It wouldn't wake up, requiring a hard reboot.  Not a good plan!  OpenBSD, however, had no problems with its suspend/resume functions which is why I made the move.

And, on the whole, I liked OpenBSD. It worked well, was stable, I found it easy to navigate and to configure as I needed and, if I ran into an issue, or wanted to do something and wasn't quite sure how to do it, there was pretty good documentation and a helpful community on which to call.  All was good so far.

But there were also a few obstacles along the way. 

**Bluetooth** OpenBSD simply does not support bluetooth, nor do they intend to. Their decision was based on security concerns (it was actually removed from the OS several iterations ago) and I can understand their concerns. That said, sometimes having an external bluetooth keyboard or mouse is really helpful when working for extended periods. The mouse especially was an annoyance and one that I'll touch on in a moment. It's also nice occasionally to be able to pop my BT earphones in and listen to music or watch a YouTube video without disturbing those around me.  

Now, in fairness, I could use a wired keyboard or earphones, but that's simply not always the most convenient option.  

**MOUSE** Probably the biggest issue for me was the touchpad/mouse situation. I'm not really sure what happened, but I started having significant issues with the touchpad not rejecting my palm. I'd be typing along and suddenly realize that my mouse was somewhere else and I was either editing parts of the post I didn't want edited or was in a completely different part of the screen and my typing was doing nothing. With a bit of digging, I was able to figure out how to toggle the touchpad off and on. With the Thinkpad, I could use the little red button in the keyboard (Do they really call it a nipple?) to move the cursor even with the touchpad turned off. But manipulating that little red button is a whole skill set in itself and one that I, frankly, didn't want to take the time to develop. But on the whole, having to constantly toggle the touchpad off and on any time I wanted to use a browser was a major aggravation.  Again, I could use a wired mouse and if I was working at a desktop that would definitely be an option. Using a laptop on the go, though, made the mouse a bit more inconvenient.

**Missing software**. By and large, OpenBSD and BSDs in general, have a good set of software available. And, honestly, I could get just about all the tools I needed through the OpenBSD package system. And I was generally happy with the available options. There were, however, a handful of programs that I've come to rely on that aren't available on OpenBSD. The most important is probably Obsidian. That's the note taking software that I use for collecting topics for writing, documenting what I plan to write, what I've written but not yet published, as well as what I've actually published. The more I write the more important it becomes to keep track of these things. Often I'll write two or three posts in a day but don't want to publish them all at the same time, so I'll schedule them. Then I need to keep up with what is scheduled to publish when. Obsidian is what I use for tracking that. 

There are alternatives, of course. I could use a Google Spreadsheet, or some other online spreadsheet or note taking software, but that adds a level of complexity to the process. It's much easier to simply open a program and start writing than it is to open a browser, all the URL, sign in, then start writing. By that point I've lost the thought I wanted to capture!  I've also played a bit with VimWiki and Org-Mode for capturing these ideas. Both work actually quite well but they lack the availability on multiple platforms that I require.  I want to be able to capture my thoughts to a single place whether I'm on a Linux machine, my Macbook Pro, or my iPhone. Obsidian gives me that option together with some organization.  

I'm still building my skills in org-mode with the goal of eventually moving over to it completely. But my skill set isn't there yet and so I need something that is immediate and easy to use.

**SD Card issues** Another issue I ran into was reading SD cards. Because this is a cheap, old computer, I plan to take it with me traveling. That way, should it be lost or damaged, I'm out $65 not $650 or more. All of my data are backed up to other devices and there's no sensitive data on this device, so if it's lost or damaged there's no real risks.  But I take lots of pictures, using three different cameras (A Canon M50 Mark II, DJI Action 4, and A DJI Pocket 3). I want to be able to pop the SD cards from those devices into my computer, dump the day's photos onto the computer, then sync those to my server back home. That doesn't work so well, on OpenBSD. 

I initially ran into issues with accessing the SD card. That was fairly easy to overcome (I haven't document that, yet). But that created another problem. The SD cards I use are SDXC cards. They can hold a lot of images and videos. The cards are formatted as exFat which allows or larger files sizes.  Once I got the computer to read the card, I got gobbledygook instead of valid files. Turns out I needed to make changes to the file format on the card. After a bit more futzing about I was able to successfully access the data on the card. Awesome!

Then I moved on to the DJI devices. Now, those cards are apparently formatted using exFat, as well, but for what ever reason the computer would not read them. After playing around a few more hours, I finally decided that it simply wasn't worth my time to keep trying to figure it out.  It was at this point that I decided that it was time to move on from OpenBSD.

I suspect that many of the issues I encountered above may not be issues with FreeBSD, NomadBSD, GhostBSD, etc. But none of those have a working suspend/resume process (all are FreeBSD based). So, while I _could_ look at those, the lack of suspend/resume would not make it feasible, so it was back to Linux Mint. 

All of the issues above are non-issues with Linux Mint. So, much to my consternation and disappointment, I have returned for the time being to LM.  

I'm still very much interested in building my knowledge, skills, and experience with the BSDs and will continue to use them on one of my desktop devices. In the meantime, though, this old laptop will get to keep Linux Mint a while longer.

