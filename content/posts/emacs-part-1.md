---
title : "Emacs Part 1"
date : "2025-08-20T09:55:08-04:00"
#dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : ""
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "projects", "Emacs"]
keywords : ["", ""]
#description : ""
showFullContent : false
readingTime : true

hideComments : true
---
# Learning Emacs Part 1

Emacs, if you're unfamiliar, is a text editor that has been around since the 1970s. It was originally designed for editing macros in early computer systems. The most popular version, and the one that dominates the space today is GNU Emacs which was developed by Richard Stallman somewhere around 1976. I'm not going to get into the nitty-gritty details of its history but knowing that it has been around for nearly 50 years and remains a very popular editor, particularly among developers and others, like me, who are interested in exploring different technologies and appreciate the extensibility and utility of the program gives you a sense of why you might want to consider it.

Emacs can do pretty much anything you want it to do. It has, according to [Wikipedia](https://en.wikipedia.org/wiki/Emacs) some 10,000 built in commands. Did I mention it is extensible? And fairly complex?

With that many commands it certainly seems that the program would be damn near impossible to master.  The reality, though, is that a few dozen commands, which can be learned with reasonable practice, will meet better than 90% (probably more) of your needs.  By far the majority of those 10,000 commands are for specific use cases which the average or casual user would likely rarely, if ever, need.

Now, besides the challenge of learning something new, the primary reason I chose to learn Emacs is that it is, so far as I've seen, available on every platform and is absolutely identical on each of those platforms. This means three things for me: 

First, no matter which computer I'm on -- Apple, Linux, OpenBSD, or Windows -- I can jump in a get to work. I cannot think of any other editor or word processor that has that kind of availability.

Second, because the program works identically on all platforms I don't have to worry about converting files or changing my work flow. I haven't used MS Word in a while, and certainly not on my Mac computers, but I don't think it works exactly the same way on Apple as it does on Windows. [^1] 

Third, its files are simple plain text. No fancy formatting codes, no extra clutter in the file (I'm looking at you, MS WORD!) This means that I can take a file created with Emacs and edit it in damn near any other editor and it'll be just fine.

All of that said, learning Emacs can be quite challenging. To me there are three keys to learning Emacs. 

First, start slowly and simply. It's tempting to try to eat the whole elephant in one go. Jump into a book on Emacs, read through everything, try all the examples, become overwhelmed and give up. 

No. Instead, decide what you want to use it for. For me, I simply want to write essays, short stories, etc. By identifying what your use case is, you can focus your learning towards those commands that help you fulfill that purpose. Learning how to enter text, move around in the text you've written, edit that text, and save your file should be your first steps. Initially, moving around in the text can be as simple as using the arrow keys. Later on you can learn how to use keybindings (shortcut key combinations) to move forward or backwards one word at a time, one line at a time, or one sentence at a time. Similarly, editing text may be as simple as learning how to delete characters, words, lines, or sentences.  We're talking maybe a dozen commands here.  

The second key to learning Emacs is practice. Like any skill the more you do it, the easier it becomes. As you work with the program and build your skills you can (and naturally will) add more commands to your skills list. Muscle memory has begun to kick in and I have been amazed at how how quickly I've picked up new skills!

The third key is to keep it simple. When I first started exploring Emacs I ran across a ton of articles and posts that encouraged new users to use Emacs variants such as Doom Emacs or Spacemacs. These are good variants, but are not, I think, really helpful for the new user.  Why? Because they more complex.  Each of them has been configured with a ton of extra packages that increase the utility of the program. But that comes with increased complexity for learning. They also generally include packages that may not be necessary for your use case.  Now, there's nothing wrong with having those extra packages available, but it does make it more challenging to learn, to filter out what is important and useful for you, and to configure the program to better meet your needs. 

Those programs also alter the way the program works, changing keybindings (shortcut key combinations) and even how text is entered. Both variants default to "Evil Mode" which changes text input to modal, similar to Vim. For folks that already know Vim, that can be a good thing as it lubricates the transition. For folks that are not familiar with Vim, it just adds another layer of complexity to the learning.

I landed on plain, vanilla Emacs. Before I started to customize my version, I wanted to learn the basics.  How does Emacs work out of the box? I felt that once I learned those basics and had mastered the vanilla keybindings I would be better positioned to see where and in what ways I might want to customize the program to my specific needs.

Another reason for choosing vanilla is that by starting with the simplest configuration I could more easily learn _how_ to customize the program. Weeding through a complex configuration file (init.el) quickly becomes confusing. It becomes more difficult to understand exactly what is happening, and what commands are doing what tasks. By starting with a basic init.el file then adding one or two changes at a time I can more easily learn what does what and how to make the changes I might want to make.  I'm just going back to the idea of "keep it simple".

Okay.  So, now you have an idea of what Emacs is and why I want to learn it. And why you might, too. But at the end of the day, it isn't just about learning the program. It is about being productive with it.

If you're like me you generally want to open the program and get to work. With just a little bit of effort you can make that happen.  In my next installment (whenever that is) we'll get into the mechanics of actually using Emacs to get some writing done!


[^1]: I could be wrong here since it's been a while since I used MS Word.
