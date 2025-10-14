---
title : "Exploring Omarchy"
date : "2025-10-14T14:12:30-04:00"
dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", ""]
categories : ["",""]
showFullContent : false
readingTime : true

---
Over the past 25 years I've played with a lot of Linux distributions. Many of those distributions have fallen by the wayside as developers shift focus, companies fold or are acquired by other companies, and so on. At the same time, new distributions, by the dozens it seems, have popped up to replace them.  While I have always been curious about the various distributions I have increasingly begun to realize that for the most part the differences between them isn't that great. When you really look at them most of the "new" distributions are simply riffs on other distributions, usually -- but not always --  Ubuntu.

Now, that's not to say that these distributions are not unique in some way.  After all, if they weren't there wouldn't be an audience for them.  But the differences are often just not that great.

Taking a step back, we can see that there are basically seven "root" linux distributions (at least for computers): Arch, Debian, Fedora, Gentoo, Knoppix, OpenSuSe, and Slackware. Almost every other distribution is based off of one of these seven.  There are also a few niche distributions that are independently developed though they have very limited followings.  There are also several Android based distributions but I don't really address those here because I'm focusing on computer based, not phone or tablet based systems.

Of those seven, Debian and Arch are the most popular and have the largest numbers of derivative distributions, with Fedora following, though exact information on the percentages of each is difficult to obtain. With this information in hand it becomes easy to see that no matter what distro you choose, you're most likely going to be using one of those three base systems. And that means that while each distribution has been tweaked to meet some specific need or objective (easy to use, science-focused, education focused, etc) their actual use is unlikely to differ significantly from their root distribution.

More to the point, with the exception, perhaps, of advanced or "power" users, most people will be interacting with a Linux system through a Desktop Environment (DE) such as KDE, Gnome, or Cinnamon. And, again, while each distribution may make tweaks to those DEs, at the end of the day the user experience just isn't really that different.  In fact, when reading reviews of recently released distributions or updated distributions, those reviews tend to focus more on the DE experience than on the actual functioning of the distribution. To me that is telling.

### I Thought This Post Was About Omarchy!

Well, it is. But I wanted to provide some background before diving into my discussion on Omarchy.

So, first off, what is Omarchy?  Omarchy is a "distribution" of Arch Linux developed and released by DHH, the founder of Ruby on Rails and founder and CEO of [37Signals](https://www.37signals.com) and it has been highlighted by a rather large community of Linux writers, bloggers, and Youtube creators over the last few months. It has been described as a "beautiful, opinionated linux distribution. With all the hype, I thought I'd give a look-see to understand whether the buzz is worth it.

### The Technology

As mentioned earlier, Omarchy is based Arch Linux and uses Hyprland as the compositor and window manager. If you don't know what that all means, that's okay. For most users, that bit of information isn't really that important.  Just know that Hyprland makes the desktop experience really pretty and highly functional.

It is also described as "opinionated". Most linux systems are intended as general purpose machines and are therefore developed in a way that gives the user plenty of options during the installation process on what programs to install, how the system will be used and so on. Opinionated software or operating systems, on the other hand, make many decisions for you. In fact, there are almost no decisions to be made in the initial installation of Omarchy. And that is a point of contention for many Linux enthusiasts. I'll touch on that notion a bit more shortly.

In the meantime,  though, let me share with you a bit of my perspective on the OS itself. Mind you, I've only been using it a few days, so there is much that I still need to fiddle with, but this will give you a  fair idea of what I'm thinking.

Unlike most distributions that include a full DE, Omarchy does not include a DE.  Rather, it includes a window manager, which I rather like.  I've been using i3 on my Linux Mint device for a while and played a bit with Sway, as well.  Rather than the point and click design of a DE, window managers typically require that you use various keyboard shortcuts (called keybindings or just bindings) to access your programs.

Omarchy has a _ton_ of keybindings and it'll take a while to learn them all. But then again, you don't really need to learn them all. You just need to learn the ones you find useful. Many programs, including those on Windows 11 and Mac OS also use keybindings (as do those two OSes). Just as a few quick examples, SUPER+b (that is the windows key or CMD key on Mac) opens your default browser. If you are running Docker containers, SUPER+D opens LazyDocker, which lets you control your docker containers. SUPER+O opens the Obsidian notetaking app. If you want to see all the programs available to you, SUPER+Space will open your apps list and SUPER+F opens your file manager. Again, these are just a few examples, but using keybindings is much quicker and easier than constantly moving your mouse around and clicking through various menus to get to the program you want[^1].

From a functional standpoint, I don't really see any differences between Omarchy and any other linux distribution, though I will note that it runs really well on my Dell Wyse thin client with a Celeron J4105 processor and 12GB of memory.  No glitches so far.

### So What Programs are Installed on First Boot?

As I mentioned earlier, Omarchy is opinionated which means that the developer has made decisions about what programs are initially installed.
Here are some of the key ones:

*  The default browser is Firefox, though Chromium is also installed
*  Clients for X, WhatsApp
*  Spotify
* ChatGPT
* Discord
* Basecamp
* Github
* Figma
* Google Contacts and Photos
* LibreOffice
* Kdenlive
* and OBS Studio

And there are several others. In addition, the keybinding SUPER+ALT+Space 
opens a menu that includes an install option that lists multiple other available programs that are part of the Omarchy repository, such as Tailscale, Bitwarden, additional AI options, multiple editor choices, gaming options, programming tools, and much more. And, if what you want or need is not in the offered list you can also install from the ARCH package repositories and from the AUR which offers user created packages.  In other words, Omarchy is Arch Linux with some special add-ons.

### Some People Don't Approve

A fairly frequent comment I've seen about Omarchy is that it's just an installation script for Arch that dumbs down the installation process and limits the user. And to an extent that is true. But since Arch underlies it all, the question I have is: Does it matter?

The fact is not everyone needs or wants to do everything from scratch.  When there are literally hundreds of programs out there, how do you pare them down? Providing the user with a set of functional out-of-the-box options makes getting started in the OS much easier. It seems not to have occurred to those that complain about this that installing a DE does the same thing. And, to be honest, every distribution of Linux is the result of someone's specific interests and needs and is, therefore, opinionated. Some are just more opinionated than others.

Mostly the folks that complain, it seems to me, are the ones that think that using Arch should be reserved for the elite among us. That somehow going through the hard stuff to set up their system makes them better, smarter, more intelligent than the average bear. I disagree.  Smart in my mind means doing things in the most efficient way. Why recreate the wheel when you've got access to the car?

And, for many of us the goal is to have a functional, useful system for getting things done. If you want to learn, then taking the hard road is the best choice. But, if you want to be productive, do what makes the most sense for you and leverage the tools that are available to you.

### What Are My Conclusions?

Well, overall, I'm fine with Omarchy. As I mentioned early on, I don't really see a lot of differences functionally between this and my Linux Mint setup with i3. I'm able to do all the things I want to do without issue and haven't yet run into anything that I needed that I couldn't readily install.

Am I going to keep using it? Perhaps. I think, at least for now, that I'll keep Linux Mint on my laptop since I have it all setup to my liking. But should I get another laptop at some point, Omarchy or some other Arch based OS might well be an viable option. Opinions be damned!

[^1]: Similar keybindings are found in most window managers, e.g. i3 and Sway, and even in all of the DEs, as well as Windows and Mac OS.



