---
title : "Learning Emacs"
date : "2025-08-12T08:18:39-04:00"
#dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "emacs"]
keywords : ["", ""]
#description : ""
showFullContent : false
readingTime : true

hideComments : true
---
# Learning Emacs

For some time now I've had a preference for using plaintext files where ever I can.  I explained in [this post]({{< relref "plaintext-preference" >}}) why that is, so  I won't repeat it here.  But in order to begin using plaintext it is necessary to have an editor that will support it.

Now, over the past few years I've preferred using nano, a simple, easy to use plaintext editor on linux (and other devices e.g. mac). Nano is just a basic editor and while it served its purpose, I was looking for something a bit more flexible. Prior to nano, I periodically turned to vi or its more recent incarnation, vim. Vim (or vi) is so deeply rooted in the unix-y space that, unlike nano, it does not need to be installed. It is part of the OS. The problem with vim, though, is that it is a modal editor.  Modal editing has its charms and its benefits but also creates a few, not obstacles, per se, but frustrations. Modal editors have different modes (hence "modal") and in order to accomplish different actions you find yourself frequently changing modes. Once you've worked with a modal editor for a while those actions become more or less automatic and I am slowly getting there. Still, it's frustrating to have to stop and think about what mode you need to be in in order to accomplish some action.

About a year ago (maybe two?) I hit on emacs. Now, I've tried emacs in the past and found it very confusing. But, I love to learn and love the challenges of learning so I trotted off to the used bookstore where I'd seen a copy of a book on GNU/EMACS. The book, it turns out, didn't help a lot in explaining the program.  In retrospect, I think the book actually did do a good job of explaining things, it just didn't do it in a way that my brain thinks. Each of us is different and so how we need information to be presented in order to really understand it may be different, as well. That seems to be the case with me. 

Anyway, the book kind of put me off of Emacs for the time being.

Fast forward to a couple of months ago and I rediscovered Emacs and decided that, come hell or high water, I was going to get at least a basic understanding of how to use the editor.  A lot of that was motivated by a number of videos and blog posts where writers had turned to Emacs as their primary writing tool because it can be configured to do pretty much anything you want it to do.  Want it to do email? No problem. Install mu4e. Want it to be your newsfeed reader? Install elfeed. Oh, want to do your web browsing within the program? Eww (very badly named package!) will do the job. You can even open a shell and work as if you're in the terminal!  No matter what you want, with over (I think) 1000 packages available, Emacs is a highly flexible editor.

So, in my usual ADD, dive into the deep end, approach, I started reading, searching, watching, and trying to learn Emacs. Now, there's alot of documentation out there. The problem is that not all of it is actually useful. Some of it is out of date, and some of it is just plain wrong. Still, I persisted.

In some of my readings, especially on Reddit and stackoverflow, others had suggested using Doom Emacs or Spacemacs, two "distributions" of emacs that incorporate a variety of packages that are designed to enhance the function of the program and, supposedly, make it easier for newbies to use. Uh. No. At least not in my view.  I'll discuss in more detail my reasons for thinking that these are not really good choices for a newbie in another post.  For now, I'll just say that I was put off more than encouraged by those two packages.

BUT ...

I am learning Emacs. This post and all of the posts for the last two months, along with a lot of writing that hasn't been published has been created in Emacs. The learning curve is steep and long. But I'm making progress. I'm beginning to see the patterns of keybinding and why they are what they are, and how to use them to accomplish my tasks. Still, I suspect I'll still be learning emacs for at least the next year. 

At the end of the day, the one question you might have is: Why go to that bother? Wny not just use something like Scrivener or Word or something to do my writing.

Fair question.

I use several different devices throughout the day. I write using whichever device is nearby. Sometimes it's my Macbook Pro, sometimes it's my Mac Mini, sometimes it's my Windows computer, and sometimes (often times) it's my linux laptop. The beauty of Emacs -- and why I have come to prefer it, I think -- is that it is available on each of those platforms and works absolutely identically in each of them. I have begun to configure emacs to my liking and so long as  I transfer those configuration settings to the other devices, I won't be able to tell which machine I'm on. No having to adjust for differences in machines. I don't know of any other program that I can say that about.  And, if I find myself at a machine that doesn't have emacs installed I can simply SSH into my server and work from there. So, no matter where I am, no matter what machine I'm on, I have access to my writing software and can easily keep working.

In coming posts I'll document some of the things I've learned not only to share with you, the reader, but for myself. 
