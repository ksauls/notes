+++
title = "First Impressions of MangoWM"
author = ["Kevin Sauls"]
date = 2026-08-07T00:00:00-04:00
publishDate = 2026-08-07T00:00:00-04:00
lastmod = 2026-08-07T15:09:05-04:00
tags = ["technology"]
draft = false
+++

For a good while now I've been using Niri as my go-to window manager on my CachyOS laptop.  This is the laptop on which I do essentially all of my writing, including this post.  I initially started with Niri after realizing how heavy some of the full Desktop Environments (DE) were and, too, given that I wanted the machine solely for writing, all of the extras that a full DE included was simply bloat. The fact is, at this stage in my tech life, I want to be able to have more control over the software that I use and avoid loading my machine with stuff I don't use.

This approach is part of my realization that in most cases, we don't need nearly the computing power or capacity that everyone thinks we do.  In other words, I don't need a new computer with the fastest processor and highest graphics and largest disk space in order to write. Writing is a slow process and one that requires very little processing power or, for that matter, storage. So long as the characters show up on the page as I type them, I'm good.  In an [earlier post](https://iamcuri.us/posts/revisiting-wordstar/) I talked about professional writers who continue to use long-abandoned software such as WordPerfect or WordStar to write.  The reason why the do that, and the reason why they _can_ is because writing doesn't require a great deal of processing power. And if your primary goal is to get words 'on paper' all the extra crap today's word processors include is simply that: Crap. Crap that requires more power, more storage, and adds nothing to the creative process of _writing_.

That realization is also what led to the realization that even very old computers (this one is from 2015!) are more than sufficient for the task of writing. The challenge, though, is that while I can use very lightweight software for writing such as a text editor, the Desktop Environment, often owing to all the fancy graphics and eye candy the developers are adding to make their product appealing to the masses, requires more processing power, more storage, and, again, often includes crap I simply have no need for. So, I started looking for alternatives.

In truth, I don't even need a window manager or DE.  But for the occasional need to open a web browser either for a quick bit of research or to validate that my finished product -- this blog -- rendered as I intend it to I could work entirely from the command line.  In fact, I have done that on multiple occasions. But, because I do need that browser periodically, some window manager that will render the browser is needed. Yes, I could use EWW that is built into Emacs, but unfortunately it won't render many web pages correctly and that would slow down the process. I have enough distractions without my workflow creating them.

Over several momths I tried several window managers. I3 came the closest to what I was looking for. Then I found Niri. It was, in a word, "AWESOME". It behaved exactly as I wanted it to and it allowed me to tweak it in ways that made it even more suited to my needs. I loved being able to easily create keybinds (shortcuts) that opened my preferred software. I loved being able to assign specific programs to specific windows and to easily and quickly flip between them as needed. I found that you could even set it up to open my required software on startup.  This meant that I simply logged into the computer and went to work, no having to start up programs first!  Like I said: AWESOME!

But, I am a tinkerer, too, and I try to keep abreast of what's happening in the tech world and periodically run up on something that sounds like an improvement, so I'll take the time to check it out.  That's how I found [MangoWM](https://mangowm.github.io).

On the surface, MangoWM looks and works a lot like Niri. It is a tiling window mananger that allows you to control how your windows are tiled. One of the features I most liked about Niri is that all of your windows are presented as a scrollable ribbon.  Need to go to another window? Just scroll left or right. You can also use CTRL+ a number to jump quickly between windows. All of this is, or at least can be, controlled strictly from the keyboard.  And that was, to me, one of the killer features.  So far as I can tell, all of these same features are found in MangoWM. There are, however, some differences.  While Niri opens all windows next to each other, creating that scrolling ribbon, by default MangoWM opens them in tiles on the same screen. You can rearrange them, open one to full screen, make a window float, and do a lot more with them than Niri allows (at least so far as I am aware). And, of course, you can create the same scrolling effect that is found in Niri, though it requires the use of a keybind to accomplish that. Now, that's okay, but is an extra step that is, in my mind, unnecessary.  I haven't figured out how to set scrollable by default. 

So, what's different? It's early in my exploration, so I cannot be definitive. Instead, I'll share a few "first impressions".

First, MangoWM seems a bit easier to configure. Niri is highly configurable but the syntax can be a bit ... confusing. Once you start working with it, it begins to make sense, but initially it is a challenge. MangoWM, though, seems to have a much simpler process.
Here's the difference between defining a keybind in MangoWM and Niri:


In MangoWM it looks like this:

```cfg
bind=SUPER,b,spawn,firefox
```

In Niri it looks like this:

```cfg
MOD+b hotkey-overlay-title="Open Browser: firefox" {spawn-sh "firefox"; }
```

Bit of a difference there, huh?

Another factor in MangoWM's favor is that it just looks visually more appealing out of the box.  I'm confident that  I could make Niri look just as appealing, but, hey, I'm lazy!  Why spend the time working on something that isn't functional if it's already been done for me?

Now, to be sure, I'm not that invested in the eye candy. As I said, I'm fine on the command line. But, having an appealing window to look at doesn't hurt, either.

I'm still in the very early stages of evaluating MangoWM. Much of today has been working to set up keybinds, re-assign MOD keys so that I can leverage muscle memory from Niri rather than reinventing the wheel, so to speak, and setting up keybinds to open my favorite programs. I'm also going to explore having my favorite programs open on start up. I'm not sure that can even be done, but I'ma gonna try.

Keep an eye on this space to see if I stay with it.
