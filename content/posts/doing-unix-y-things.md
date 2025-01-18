---
title: 'Doing Unix-y Things'
date: 2024-06-17
tags:
 - technology
---
# Doing Unix-y Things

In an [earlier post]({{< relref "my-history-with-self-hosting" >}}) I noted that my foray into Linux began when I started an intensive program in network administration, etc  back in 2000.  That's not precisely true.  That course did not teach me *anything* about Linux.  I don't even recall it being mentioned.  What it *did* teach me was Unix.  Sun Solaris Unix, to be precise, running on a Sun Sparc server (rest their souls). Linux came along a bit later.

I remember, even today, our introduction to the commandline.  I don't really know why, but that black screen, devoid of anything other than a dollar sign and a blinking cursor reminded me of some bottomless pit.  It seemed the whole internet universe was opened up and I was staring into the abyss.  It was a weird feeling.  And, I got over it pretty quick. And I wanted more.

I found that I was intrigued by Unix. The problem was Unix at that time was not cheap and required specific -- and expensive -- hardware. Now a couple of my classmates were rather competent at the commandline and introduced (I should say re-introduced) me to Linux. Unlike that time around 1995 when I got a Linux disk in some PC magazine, popped the floppy disk into the drive, fired up the computer and stared at a blank screen with no idea what to do next, this time I had some inkling of what to do at the commandline. In fact, I felt fairly confident in those unix-y things.

So, for the next twenty or so years I've bounced around the Linux world trying out various distros, figuring out how to do what I wanted to do, and how to make things happen.  I've said a lot of bad words along the way and threw more than one item across the room in frustration. But I learned. And I continue to learn.  Sometimes I amaze myself at how much I've learned. Am I an expert[^1]? Not by any means. but, I'm pretty damn confident in getting things done, or at least knowing where to look to get the answers. All that said, in truth, though, I've mostly stumbled through my efforts to get a handle on Linux.

Recently I revisited an old friend. Unix.  In the form of FreeBSD.  Now, to be legal, I must say that FreeBSD is not Unix.  It is Unix-like.  Why? [The Open Group](https://www.opengroup.org/) owns the trademark to Unix. They set the standards and provide certification for Unix systems and, therefore, they get to say which systems can call themselves Unix. Systems, such as FreeBSD, which function almost identically to Unix (and that pretty much include Linux, too, I suppose) may say they're "Unix-like" but cannot use the actual title of Unix.  Potayto, potahto, in my view. I imagine there's some serious money mixed in there somewhere.

The BSD experience is both quite familiar and quite different from the Linux experience.  It's familiar because much of the work is done at the commandline and the commands are generally the same.  On the other hand, there are generally fewer problems with getting software to work in BSD because the entire system is designed to work cohesively.  There's a handful of programmers that oversee the entire process and only software packages that are fully compliant with the overall design find their way into the ecosystem. BSD systems (yes, there are several) each have specific philosophical approaches and they adhere quite tightly to those approaches.  In short, they don't try to be everything to everybody. They try to tailor their systems to the needs of specific groups.

Because BSDs are more focused, their individual markets are smaller which, in turn, means that fewer programs tend to be developed for a given system.  And this is where BSD really diverges from Linux.  Linux, being a more generalized system, and having thousands more users, has literally thousands of applications[^2] that will run on that platform (though not without significant issues at times, it must be noted).  And part of that is the draw of Linux. Versatility.

 Linux powers a lot of servers on the internet.  So does Unix.  In fact, some of the pretty big names on the internet, such as Netflix, use FreeBSD.  The challenge for me is that there are dozens of flavors of Linux, each with their unique take on what is important and how to go about getting things done.  That's not necessarily bad but it does make working on different systems a bit challenging.  And, at least from my point of view, doesn't really make a lot of sense.

So, back to the topic at hand.  Why did I decide to revisit Unix?  I wanted to revisit those roots.  I wanted to recall what the true Unix experience is about. I wanted to add to my knowledge base and understanding of operating systems And, I was curious if I could run all the things I'm now doing on my linux devices on a BSD system.  The jury is still out on that, by the way, as I'm still learning and playing.

Rather than take a fly-by-the-seat-of-my-pants, also known as a learn-by-screwing-up, approach I decided to actually take the time to learn, in a more or less systematic manner, the BSD system.  [Michael W Lucas](https://mwl.io) has written a great book on FreeBSD called *Absolute FreeBSD*.  I have to admit that it is probably the single most easily read and digested tech books I've seen. And I've read a bunch of them.  I'm only about half-way through the book at this point but already I have a much clearer understanding of a lot of concepts that I was aware of but didn't fully understand.  And, because both FreeBSD and Linux share that common Unix foundation, much (but not all) that I've learned is transferable to the Linux environment.  I'll probably do a book review on this one when I'm done.

I like the Unix-y way of doing things.  I like the philosophy that underlies the BSDs. And, I like the knowledge that there are no corporate overlords looking for ways to squeeze more money out of my pocket.  I mean, I read recently that Microsoft is looking at including ads in the start menu. Seriously?  And, I like the fact that the data on my computer, sitting in my office, is confined to my office.  No one is trying to get me to store my data in the cloud (OneDrive, anyone? Oh, and Google, what can I say?)

The BSDs are run by volunteers and not-for-profit organizations rather than corporations.  They are not out to make a gazillion dollars for their stockholders while screwing their customers. And they're not turning their customers into the product.  

And I kinda like all that.




[^1]: Remind me sometime to tell you about my response to the question, "do you consider yourself an expert" as posed by one of my dissertation professors.
[^2]: Do we *really* need all those thousands of applications?  How many of them are just tweaks to earlier programs?
