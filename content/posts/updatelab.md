+++
title = "Reorganizing My HomeLab"
author = ["Kevin Sauls"]
date = 2026-07-20
publishDate = 2026-07-20
lastmod = 2026-07-20T19:34:11-04:00
tags = ["homelab,proxmox,truenas"]
draft = false
+++

<div class="ox-hugo-toc toc">

<div class="heading">Table of Contents</div>

- [In the Beginning ...](#in-the-beginning-dot-dot-dot)
- [The Problem](#the-problem)
- [Where I am Today](#where-i-am-today)
- [My Equipment](#my-equipment)
- [Revisiting my OS choices](#revisiting-my-os-choices)
    - [Unraid Thoughts](#unraid-thoughts)
    - [My thoughts on Proxmox](#my-thoughts-on-proxmox)
- [The Changes](#the-changes)
    - [Why Truenas](#why-truenas)
- [And Proxmox?](#and-proxmox)
- [At the End of the Day ...](#at-the-end-of-the-day-dot-dot-dot)

</div>
<!--endtoc-->


## In the Beginning ... {#in-the-beginning-dot-dot-dot}

Like most homelabbers/self-hosters my setup has morphed over the years. I started, as most do, with a single machine that was built and rebuilt multiple times as I experimented with different technologies, software stacks, and so on.  I started back before the advent of Docker so I was literally building Apache from source or, if I was lucky, installing a .deb version. Most of the early work required a lot of setup, futzing around with config files and so on.  (If you've never installed Oracle from source you haven't lived!) The result was something of a Frankenstein setup.

I also played with Junohost and several other packages of that ilk, some of which are no longer around. That was a great way to learn. To some degree I mourn the fact that many younger labbers/hosters no longer have those opportunities to learn.  Docker is a great tool and one that I now rely on. But having that foundational knowledge and having to dig into the complexities of setting up software from source was just a great experience, frustrating, though, as it often was.


## The Problem {#the-problem}

But I digress.  Today, I have multiple machines that all served different purposes.  One was intended as a host for the services I rely on, e.g. FreshRSS, ArchiveBox, ReadDeck, and so on. And it was to serve as something of a NAS device as backup to my individual laptops and other desktop machines.

The other machine was intended as my "experiment" machine. That's my home lab. The machine where I  install software that I want to learn more about, play with to see if I want to include it in my list of relied upon services, or just want to figure out exactly what it does.

Notice, though, that I said "intended to". I get lazy. Over time, many of the programs that I played with ended up having content added that I didn't want to lose. As a result, well, my "experimental" machine ended up with production services on it. That's not good.

Now, what I _should_ have done was simply move those services over to the other machine but, like I said, I'm lazy and just never seemed to get around to it.


## Where I am Today {#where-i-am-today}

So, here I am today (well, actually a couple of weeks ago) with two machines that provide production level services and no machine to really play and experiment with. And, to be honest, that's okay. While I still keep an eye on the self-hosting forums to see what's new, I've reached a point where I'm mostly seeing derivations of the same products or similar products that seek to solve the same problems. And it's become increasingly difficult to see how they are different.

Take a look at almost any notetaking app and you'll see what I mean. They all look nearly the same, offer most of the same features, and fulfill the same need.

My needs and interests have also changed. I've settled into routines that rely on a specific set of services and, honestly, haven't found anything new that I felt would benefit me. Truth be known, I've got several services running that I rarely, if ever use!

So, a few weeks ago I decided to take a step back and carefully evaluate my current needs and where I'd like my setup to go. I came to the conclusion that I needed one machine to host my Docker and LXC containers. These are the services I rely on. And, I needed one machine to act as a NAS. My intent was to not run any services on that machine other than those that supported the NAS functionality: NFS and Samba. I also wanted this machine to serve as a Time Machine host.


## My Equipment {#my-equipment}

The two primary machines are:

-   An HP Microserver Gen10 Plus with  Xeon processor, 32GB memory, and four drives. At the start of this project I was running Unraid which allowed me to use mixed drive sizes.
-   an older HP EliteDesk G3 400 with 64GB memory. This machine, likewise, had mixed sized drives, including a 2TB 2.5 inch drive, a 4TB WD Red, and another 2.5 inch drive which, I think, was 320GB. That last one was my boot drive.  I ran Proxmox on this machine and it hosted four always-on VMs and maybe a dozen LXCs.

    I also run several smaller machines -- Dell Wyse 5070s -- that aren't included in the current reorganization. One of those devices serves as my Proxmox Backup Server. Another runs Frigate, though I've off-loaded much of my surveillance stuff to Scrypted which is running as an LXC on Proxmox.


## Revisiting my OS choices {#revisiting-my-os-choices}

In the beginning of my journey I relied on Ubuntu for almost all of my hosting needs. Overtime, as I got deeper into the self-hosting hole, I learned about other options e.g. Proxmox and Unraid. I loved that both gave me the opportunity to experiment in different ways.


### Unraid Thoughts {#unraid-thoughts}

But, Unraid is, at its core, a NAS operating system and I wasn't really using it for that. I was using it much like I was Proxmox: as a host for docker containers and VMs. One of the things I liked about Unraid was its use of a parity drive to help ensure data integrity.  The downside of that, however, proved to be a very lengthy parity check process that slowed down my system when it was running.

And, as I mentioned above, Unraid allows for mix-and-match drives, also known as "just a bunch of disks" (JBOD). This allowed me to use my existing hardware rather than having to invest in a set of new drives.

Overall, I liked using Unraid. I think the one thing that bugged me about it was that it is not open-source and is essentially a subscription service. Past the first year, you don't _have_ to buy a subscription, but if you need support, well ...

Besides the lengthy parity checks (which ran early every Sunday morninwg) the other frustration I had was that it could take several seconds to load the page showing the Docker containers I was running. I wasn't running that many, but it still took time. The same was true for the "apps" page .. it always took several seconds to load. Not a deal breaker; I don't have a problem waiting for processes to run. It just seemed rather excessive given the hardware and what it was actually loading.
Finally, I realized that while I had three data disks in the Unraid server, all of the data were being saved onto one disk rather than being spread across the available drives. That seemed pretty wasteful to me.


### My thoughts on Proxmox {#my-thoughts-on-proxmox}

Proxmox was an absolute godsend!  I love that hypervisor!  It is so easy to setup and manage an LXC or VM. It is my go-to for exploring new software.  I have yet to find anything harsh to say about it.

Like any new piece of software, Proxmox can be a bit confusing to set up initially (as can Unraid) but I fairly quickly got a handle on it. It has be great for learning more about LXCs, of which I now have many.

In my ideal world, all of my services would run on Proxmox.  Yes, I can do the same thing with a Debian base, but Proxmox just makes it all so much easier.  And, as I said earlier, I'm lazy -- easy is good.


## The Changes {#the-changes}

As I started looking at my setup I realized that I had four 4-TB drives but they were scattered across four machines: One in the MicroServer, One in the G3, and two in the QNAP NAS. That seemed somewhat wasteful. So, after I backed everything up, I rearranged the drives so that I had three 4-TB drives in the Microserver, and one in the QNAP. A 2TB drive along with a 320GB boot drive were left in the G3. I'll eventually get another drive in that one, so

I pulled the drives from the Microserver and replaced them with the three 4TB drives and then installed Truenas as the operating system. I did save the drives and the boot USB in the event  I decide that Truenas isn't right for me.

My plan is to use Truenas as my primary NAS, backed up to the QNAP server. I'll eventually either buy another 4TB drive for the QNAP , or upgrade to two 6TB or larger drives since the Truenas machine now has 6TB of storage. Those two drives will be mirrored.


### Why Truenas {#why-truenas}

Just to be clear, Unraid was serving me well, despite the issues I mentioned above, and I didn't need to switch. Part of my motivation for moving to Truenas was curiosity (a common driver for my decisions). I had played with it briefly once before but didn't have the requisite drive capacity to truly utilize it. And, it just seemed to be a little overkill for my needs. Now, though, switching to Truenas seemed to be a better use of my storage capacity and also from what I've read seems to be more performant. And, in considering my plans for making this machine a true NAS with NFS and perhaps even iSCSI shares, I figured Truenas might be a better fit. And, so far, I've been pleased with it.


## And Proxmox? {#and-proxmox}

One of the wonderful things about Proxmox Backup Server is that rebuilding a server is trivial. Reinstall Proxmox, making sure to use the latest version, connect your PBS to it, select the backups you want to install and BOOM! You've got a running Proxmox server.  I don't think I spent an hour rebuilding the server and much of that was deciding what hardware I wanted to use and which LXCs and VMs I wanted to restore. As usual, I had a number of containers and VMs that were installed but not active so I took the opportunity to be a bit more discerning in my restoration process.


## At the End of the Day ... {#at-the-end-of-the-day-dot-dot-dot}

As it stands right now, I'm pretty happy with my setup.  Despite my plans otherwise, I do have a few apps running on the Truenas machine, including Nextcloud&nbsp;[^1], Syncthing, and Hister&nbsp;[^2].  I chose to run those on the NAS simply because I suspect they'll use more storage than is available on the Proxmox machine (at least at this time.)

I'll give an update in the coming months on how things are going and what additional changes I make.

[^1]: I'm still on the fence about Nextcloud. In some ways I can see its utility, as it is similar to Google Drive or OneDrive. On the other hand, what does it offer me that can't be accomplished with a simple network share?
[^2]: Hister is a new addition and is an awesome web history search engine. I'll do a post on that one in the near future.
