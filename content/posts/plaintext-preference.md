---
title: PlainText Preferences
date: 2024-05-20
author : "Kevin Sauls"
tags:
  - technology
categories:
  - technology
---
# PlainText Preferences

Over the last ten years there have been a couple of preferences that have driven many of my technology decisions.  One is a preference for using plain text rather than proprietary software. The other is a preference for flat files over databases.

## Let's Talk about Plain Text

My move toward plain text came about for several reasons.

First, I just wanted to take notes that I could quickly create and reference as needed.

Second, I  wanted to be able to focus on writing, such as an essay or blog post, without worrying really about formatting, etc.  What more distraction-free writing environment is there than the command line?  

Third, I wanted small, easily accessed files.  None of the proprietary word processors come close to that.  

Fourth, I wanted to be able to do access and edit the files on any device I happen to be on. 

And, finally, I wanted them to be available 20 years from now (why I'll still need them at age 85, who knows, but still ...).  

Now, that all may sound nice, you say, but is it really practical?  I think so, particularly with the advent of Markdown.  Markdown allows me to provide some basic formatting as I write (think section headings) while minimizing the cruft.  The fact is, if I need to put a document into a particular format, let's say Microsoft Word, I just need to copy and paste the plain text into the word processor and I'm off to the races.  On the other hand, trying to get a clean copy of that document *out* of Word ... well, good luck with that.  The point is I can use *any* processing software to pretty up my work while keeping a clean copy available for the future.

### And Then There Are Flat Files

Closely allied with plain text files is the use of flat files.  I have come to prefer flat files for pretty much the same reason I like plain text -- easy of access.  

Now, full disclosure, I spent quite a bit of time over the last 24 years learning databases. I have created and managed many, many databases over that time and absolutely have nothing against them, per se. In the right environment and the right data they are phenomenal and, of course, are the best choice.  For my personal needs, though, databases seem to be overkill.  The right tool for the right job.

Storing data in a database is very useful with large datasets.  In fact, it is really about the only way to work with very large datasets.  Storing my writing in a database, though, poses several issues. The first, obviously, is that the use of a database program to store a file makes little sense.  It adds an unnecessary level of complexity and creates an opportunity for failure.  More importantly, if the database should become corrupted the I lose all of my work.  Not an appetizing prospect.  Again, given the small quantity of work I do, the complexity and bulk of a database is simply overkill.  Running a database to store even one hundred blog posts is more work than needed.  To me, though, the most important reason is that to get my work out of the database requires a lot of extra effort.  If, for example,  I decide to move to a different computer, or a different web server, or use a different blogging platform, transitioning from one database system to another is a challenge.  

Flat files allow me to bypass that complexity and have everything I need easily available.  The order of the day, if you haven't already guessed is to minimize friction in my workflow.  The less complex, the better.  It doesn't get much simpler than a simple plain text file.

So, my current workflow is to use Obsidian to write my notes, blog posts, etc. Obsidian saves all my files as simple flat files in plain text.  I copy those files over to my web folder where I run my Static Site Generator[^1] to create my website, then rsync those files up to the server.

[^1]: I'm in the process of evaluating which SSG to use.  I want my website to be static, as well with minimal extra stuff (think [Brutalist Web Design](https://brutalist-web.design)) so I'm looking around to see what fits me best.  I'm leaning toward either Hugo or MkDocs right now. But that is subject to change!
