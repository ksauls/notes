&#x2014;
title: Experimenting with FreeBSD on a Laptop
date: 2025-06-25
tags:

-   technology

&#x2014;
Introduction
Way back in the day (circa 2000) I was introduced to Unix-like operating systems in the form of Sun Solaris running on a Sun Sparc server.  I was intrigued. And wanted to know more. Of course, at that time running a Unix-like operating system at home, on an x86 machine, meant Linux, not true Unix.  Why? Well, to start, Unix simply didn&rsquo;t run on x86.  It has been ported to x86 in recent years, but at thetime it wasn&rsquo;t. So, I started playing with Linux and have spent the last quarter century mucking my way around that system.  And I think I&rsquo;ve got a reasonably good handle on it.


<a id="org1573670"></a>

# Motivation

Well, then, you say, if you&rsquo;re comfortable with Linux, why spend time playing with FreeBSD (or anything other than Linux)? The answer is probably more complex than I&rsquo;ll describe here (or perhaps less. Who knows?)  Part of the reason is simply that I like learning new things (or, in this case re-learning something from long ago.) Truth be told, I never really learned a lot about Unix back in the day. Rather, I learned how to get around in the system and do what I needed to do, but didn&rsquo;t really learn anything about the system itself, how it was organized and why.  I didn&rsquo;t know the philosophy behind that organization, either.

One of the challenges I&rsquo;ve had with Linux through all these years has been understanding where programs and their configuration files are installed.  Most often congifuration files are found in /etc.  That&rsquo;s all well and good, but some Linux distributions seemd to mix system level config files, that is those required for the system to function, with config files for programs that I as the user have installed.  This can become especially challenging, I think, when you&rsquo;re not clear exactly what files a particular program has installed since they&rsquo;re often not named consistent with the program.

In Unix-like systems e.g. FreeBSD, the applications and configuration files that I install (LibreOffice, for example) are stored in the *usr/local* directory.  On a clean install, for example, there may be nothing in the */usr/local/bin directory*.  Another great example is where files for a webserver are stored.  In Linux, I&rsquo;ve found the root directory for the webserver in *opt and in /var*. And in some cases, I&rsquo;ve found that the actual root folder is tucked away somewhere else which makes it *very* difficult to track down where to put your files! So, there&rsquo;s not a lot of consistency.  In FreeBSD the server files will be in */usr/local/etc/www*. And, so far as I&rsquo;ve seen that&rsquo;s the only place they go.  That&rsquo;s convenient and consistent.

Another motivation for exploring FreeBSD is gain a better understanding of the philosophy behind Unix.  I&rsquo;m not getting into that here; there are plenty of resources that you can use to learn more (for example, [Basics of Unix Philosophy](https://cscie26.dce.harvard.edu)).

Finally, and this is really what prompted this whole journey, I read an [article](https://stevengharms.com/longform/my-first-freebsd) about creating a &ldquo;Just focus&rdquo; laptop for writing. That article got me thinking about the process.  I had been considering building a Linux laptop for travel but that article inspired me to consider FreeBSD instead.


<a id="org704b364"></a>

# Process

Of course, the first step in building a FreeBSD laptop is to obtain a laptop.  I had only one: a new Macbook Pro.  Not messing with that one, so I had to look around for another option.  I had considered buying an inexpensive new laptop from Wally World, or wherever, but really didn&rsquo;t want to spend a lot of money on something that was, for all intent and purposes, an experiment. Then I remembered that we have an organization nearby that takes in and refurbished used IT equipment.  Their goal is really two-fold.  First, to effect the environment by minimizing ewaste and, second, to make computing available to people who might otherwise not be able to afford it.  In essence, they take in donations of used equipment, refurbish it, load Linux on it, then sell it at ridiculously low prices.  In addition to the hardware side of the plan, they also do a lot of education on how to use computers and the software that comes with it.  It&rsquo;s a great idea and one that I wholeheartedly believe in.
So, I hopped over to the store a few Saturdays ago (they&rsquo;re only open for a few hours on Saturday and Sunday) to try my luck.  Now, shopping at stores like this is really a crap shoot.  Maybe they&rsquo;ll have what you want, maybe they won&rsquo;t. In this case, I lucked up on finding a 10 year old Lenovo X250 that looked to be in pretty pristine condition.  My previous employer supplied Lenovo laptops for our work, so I&rsquo;ve used them for more than 10 years and have always found them comfortable to work on and rarely encountered problems with them. For less than $75 I got myself a 10 year old laptop with a 512 GB SSD hard drive and 8 GB memory.  To my surprise the batteries for the computer still have greater than 75% life in them.  So, I feel like I got a pretty good deal and was on my way to building that portable BSD based laptop.


<a id="org4d2341f"></a>

# Challenges

To be honest, there were surprisingly few challenges.  If you do a bit of research on the internet about FreeBSD you&rsquo;ll find that there is a lot of conflicting information out there. One of the things I read quite a lot was that it&rsquo;s a pain to get going on a laptop. For me, at least, that turned out not to be true. Installation was a breeze, all of the hardware was recognized and &ldquo;just worked&rdquo; and I was able to install all of the software that I needed.

To get there I followed the steps found in the article I linked aboe. I hadn&rsquo;t worked with Wayland before, but figured I&rsquo;d give it a go. I did have to do a bit of internet sleuthing to get everything configured, but that wasn&rsquo;t difficult and within an hour I had a functioning FreeBSD laptop!


<a id="org1a58943"></a>

## The One Challenge

I was busy patting myself on the back at how successful I had been. Then I closed the lid. The computer didn&rsquo;t go to sleep.  Well, as it happened, a bit more sleuthing and that issue was resolved but then it revealed another: It would go to sleep, but wouldn&rsquo;t wake up.

That issue was a bit more vexing. None of the research revealed a solution. After a couple of *days* of digging, I finally figured out that the issue was TPM in the BIOS. No worries; should be an easy fix.

Except it wasn&rsquo;t.

It turns out that the BIOS on my particular machine had an administrator password set. I couldn&rsquo;t make changes to the bios because I didn&rsquo;t have that password.

A bit more digging and I learned that this would be a lost cause: There is no way to reset the administrator password on a Lenovo laptop.  I would need to send the motherboard to Lenovo who would replace it.  Well, there were two problems with that:

First, I wasn&rsquo;t going to pay to have this problem resolved since it would likely cost more than I had paid for the device to start with. And, since it was an experiment anyway, paying to replace the motherboard didn&rsquo;t make sense.

Second, even if I was willing to pay it is unlikely that Lenovo would still have a stock of these 10 year old motherboards on hand with which to replace it.

So ends my FreeBSD experiment on this laptop. :(


<a id="org63ebabc"></a>

# Final Thoughts

Wrapping things up. On the whole, I think this experiment was quite successful. I really do like working with FreeBSD and am aiming to do more #+attr<sub>html</sub>: :width 500px it.

But not on *this* laptop. Having to shutdown anytime I step away from th e computer is a no-go for me. For now, this computer (which, btw is what I&rsquo;m writing this post on) gets reloaded with Linux.

Still, the process was pretty easy and free of significant challenges. FreeBSD was quite speedy on this device. If I&rsquo;m able to score a second laptop that does not have a locked bios I will definitely be trying again!

