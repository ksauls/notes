+++
title = "Writing Hugo Posts in Org-mode"
author = ["Kevin Sauls"]
date = 2026-07-06T00:00:00-04:00
publishDate = 2026-07-06T00:00:00-04:00
lastmod = 2026-07-06T11:11:20-04:00
tags = ["emacs,", "writing"]
draft = false
+++

<div class="ox-hugo-toc toc">

<div class="heading">Table of Contents</div>

- [Limits to Hugo's Native Org Support](#limits-to-hugo-s-native-org-support)
- [Enter Ox-Hugo](#enter-ox-hugo)
- [Why Did I Change?](#why-did-i-change)
- [The Experience So Far](#the-experience-so-far)
- [The Final Question](#the-final-question)

</div>
<!--endtoc-->

For the past year I've written almost all of my posts here in Emacs. My workflow has typically been to create a new file in my content/posts directory with the command \`\`\`hugo new posts/filename.md\`\`\`. Notice that the file has a ".md" extension.  I prefer writing in markdown which is one of the reasons I settled on Hugo to start with. It made sense, then, to create a markdown file to write my posts.

Recently, as I've started revisiting Emacs and digging  a bit deeper into it I realized that Hugo actually supports .org files natively. That is, I _could_ write my post in org-mode and have Hugo directly translate it into a markdown file which it can then convert to HTML for upload and presentation. As I was reading about that option, however, I learned that there were some limits to this approach.


## Limits to Hugo's Native Org Support {#limits-to-hugo-s-native-org-support}

Apparently Hugo doesn't support the full range of options available through org-mode. For example, it might support very basic tables but if your table is a bit more complex ... forget it.  Hugo also requires some specific frontmatter. It apparently does not convert org frontmatter to proper yaml and embedding yaml into the org file seems to confuse both programs. Links to other files and sites also seems to be problematic. But I don't want to spend a lot of time troubleshooting the tools I use for writing.


## Enter Ox-Hugo {#enter-ox-hugo}

Ox-Hugo is a plugin to Emacs that converts your .org file into proper markdown which Hugo then parses into html. Emacs, of course, has the ability to publish straight to html, but then you don't have the "next" and "previous" links and the site isn't neatly tied together. What you have is a bunch if independent webpages that are not linked in any way. Stepping through the process to convert either markdown or org files into html via Hugo is the only way to build a fully functional static website. (Yes, I know that there are myriad other static site generators, but we're talking about Hugo here ...)

Now, I had read about ox-hugo previously but didn't know much about it and, at the time, thought that it might be more trouble than it was worth. I was already being productive using Emacs with the .md files and saw no real reason to change my workflow.


## Why Did I Change? {#why-did-i-change}

So, why did I?  Well, partly out of curiosity. Having read about it, my curiosity was aroused, particularly after reading many webpages and Reddit posts about how useful it was. And, I wanted to see for myself if it would be useful for my use case. I also hated the additional steps of having to issue that \`\`\`hugo new posts/title.md\`\`\` (which I can never remember for some reason!) command, changing into the posts directory, finding the file to open so that I could actually begin writing. Being able to simply open a .org file, use a snippet to enter the frontmatter (I'll talk about that in another post) and start typing definitely had an appeal.  Finally, I'm simply trying to use more of Emacs' capabilities. I've found Emacs to be extremely useful for writing, though with quirks, to be sure. As my skill level builds -- and with it my confidence in using the Emacs -- I find that I really like the _"Emacs Way"_.


## The Experience So Far {#the-experience-so-far}

This is the first actual post I've written with the intent to publish via ox-hugo.  I did create several test posts to familarize myself with the process and ensure that it actually did what I wanted and expected it to do. Those posts, of course, were deleted but I was very pleased with the outcome of those tests.

I did run into some problems getting ox-hugo to load on startup. Those issues were more my lack of knowledge in setting up Emacs than with the plugin itself. I'm still learning Emacs and, in particular, how to configure it. Challenges are expected. And that's how I learn.

That said, so far, I can say that the experience has been very good. Once I sorted a few things out in the installation process and ensured that ox-hugo actually loaded on start up, the actual process of _using_ ox-hugo has been pretty seamless.

I was concerned that editing might be a problem. The markdown used by Emacs is different from the 'standard' markdown that I normally use (and which Hugo expects). But, even that has not been a challenge. It makes more sense to me to use forward slashes to indicate _italics_ than a series of asterisks or underscores to indicate, well, <span class="underline">underscoring</span>. (Can you even underscore in markdown? I'm not sure!)

cI'm going to give ox-hugo a fair shake, using it for the foreseeable future.


## The Final Question {#the-final-question}

At the end of the day, I think the question that I have to answer for myself, and you may need to answer for yourself, as well, is whether there is any real benefit to using ox-hugo over the standard approach using .md files. That question remains to be answered. Hopefully the next few weeks will provide more insight.
