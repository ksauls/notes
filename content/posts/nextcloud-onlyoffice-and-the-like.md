---
title: 'Nextcloud, OnlyOffice and the Like '
date: 2018-02-25
categories:
    - projects
tags:
    - websites
    - technology
---
# Nextcloud, OnlyOffice, and the Like

Every once in a while I get this notion that I need to move my data off of sites 
like Dropbox, OneDrive, and so forth. When I do, I start playing around with 
self-hosted services such as NextCloud, OwnCloud, and so forth. I'm currently in 
one of those cycles and have been playing around a good bit with Nextcloud.  

I've even coupled it with OnlyOffice so that I can edit documents in the 
<!-- more -->"cloud".  As I began playing with this stuff, though, I struggled with my "why".  
Here's where I am right now.
## My Current Setup ##
Let me say upfront that I use OneDrive for most of my document storage. That 
came about partly because I use a Microsoft Surface, as well as a Windows laptop 
that doesn't have a large storage capacity.  Being able to write a document in 
Word and send it straight to the cloud service, and then to have that document 
available from any computer I work on (I have several) is a great convenience.  
Now, it's important, here, to note that I actually have two OneDrive accounts: 
The 5 GB free one and a 1 TB paid service through my Office365 account. I 
actually use the paid account as my Exchange server more than for file storage, 
but that option is available to me.

Most of my documents, though, are saved to a Linux-based local network file 
server. All of my computers are attached to that file server so that I can 
access my files from that machine. The OneDrive folder that is synced to to 
cloud service actually lives on that local server and is mapped to a drive on my 
Windows laptop.  This ensures both that I have local access and have a backup of 
those files I consider critical. (They're also backed up locally to another 
computer.)  Ensuring that those critical files are backed up off site is 
important 
and one of the arguments I have against self-hosted "cloud services". What is 
the point of "self-hosting" if you're then going to back up those same files to 
an online backup service?

One of the arguments that I frequently hear is that these services allow me to 
access my files from anywhere. This is true.  And, if I'm not on my own computer 
( a rare occurrence), this can be a very important, even critical, feature.  In 
my case, though, I have all of my mobile devices set to access my local network 
through a VPN. My Ubiquiti Edgerouter X made setting up that VPN almost trivial 
and works flawlessly.  So, so long as I have one of my mobile devices, I can 
access my internal network and all the files available there.  No need for a 
webservice to provide that intermediate layer.
## Privacy Concerns ##
In most of the online discussions surrounding these types of self-hosted 
services, the primary reason for moving from a "cloud host" to a self-hosted 
solution is privacy.  After all, we don't want those big, bad companies mining 
our files for information.  As I considered this argument, though, I had to come 
to the conclusion that it didn't really matter to me.  First of all, there's 
really nothing in my files that I feel is so important that it needs to be 
secured.  If I have such files (various bills and statements come to mind), I 
don't put them in my Dropbox or OneDrive folder.  They live in a local folder. 
Most of what I store in the online services are downloaded PDF files or 
documents that 
I received through my educational experiences.  Those are already generally 
publicly available. And, while they might provide some insight into what 
interests me, they would hardly provide anything that could be considered 
compromising.  So, privacy, at least for me, isn't much of an issue.

Now, having said that, I do have to concede one area that could become 
problematic from the privacy perspective.  I write a lot.  Most of it is for 
working out my own thoughts and ideas.  Some of it is part of various projects 
that I'm working on (stories, or my dissertation, for example). Although not 
sensitive in the sense of compromising my privacy, these writings do involve 
some levels of 
copyright.  Should my online account at one of these big providers be 
compromised, my claim to copyright on these documents could be compromised.  The 
likelihood of that occurring is minimal, but it is, nonetheless, a risk.
## Security ##
Security, to me, is part of, but separate from, privacy.  A secure service 
protects my privacy, to be sure.  But what I'm referring to here is protecting 
my work from loss.  If I have files that I truly do not want to lose, I want to 
ensure that I've got them saved in multiple places so that I can be sure that I 
don't lose them.  As I mentioned earlier in this post, I have taken measures to 
ensure that my important files are backed up to another computer in the event 
that my server or hard drive crashes.  But, if my house burns down, I'm still 
out of luck.  Except that I've also saved those files to my OneDrive account.

The issue with saving them to an outside vendor, whether it be Dropbox, Box, or 
OneDrive, is that those companies might, at any given moment, decide to simply 
disappear from the face of the Earth, taking my important files with them.  

Alternately, they may sell out to another company that doesn't take the same 
precautions, or that decides to hold my data hostagse.  Not an enticing scenario 
and, hopefully, an unlikely one. But, taking that risk is ..., well, a risk.
## Storage -- The Defining Factor ##
Perhaps the biggest draw for using a service like Nextcloud is available 
storage. Unlike the online providers, all of which limit storage, storage for 
your self-hosted Nextcloud account is limited only by the available storage on 
the server in your home.  Need More? Add another drive, or upgrade to a larger 
one. 

As I mentioned earlier, my free OneDrive account is limited to 
5 GB of storage.  Dropbox is currently limited to 2GB and will cost you $100 for 
a 1TB option. Box offers 10 GB storage with their free plan and $120 a year for 
a 100GB plan.  Oh, and all these have upload caps, so if you're uploading big 
files, you might be out of luck.  As I mentioned earlier, I have Office365 
account that provides my Exchange services, as well as 1TB storage.  I'm 
probably good there (I don't remember if there are upload limits, though I'm 
sure there are!) But, I've have that account for about 6 years, during which 
time I've watched the provided services change and generally decline.  I would 
not be surprised if, on my next renewal, the amount of available (paid) storage 
diminishes. And, that is the risk with all of these services, particularly the 
free services: At any time the provide can choose to lower their limits and 
suddenly you're locked out of your data, or required to pony up cash to keep the 
account usable.

Again, this is not really an issue for me. Part of the reason is because I do 
have that 
1TB of 
paid-for storage, but more importantly because I have several TB of storage on 
my local server, without upload limits, and have easy access through my VPN.

## So, Where Am I Truly At? ##

For right now, I'm leaving the Nextcloud and OnlyOffice servers running.  
Whether I will use them is a question that only time will answer.  I'm intrigued 
by the ability to do on-line editing much as Office Online and Google Docs can 
do.  In fact, I don't really see any differences between the various online 
editing services based on my general use cases.  I'll continue to play with them 
to see whether they meet any specific need that I might have not yet identified.  

As I wind down my dissertation work my needs for high-powered writing tools 
diminishes, as does my need for document storage. In that light, Nextcloud may 
provide all the services I need for daily work.  Time will tell that tale.
