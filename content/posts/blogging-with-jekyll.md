---
title: 'Blogging with Jekyll'
date: 2017-10-30
categories:
    - projects
tags:
    - writing
    - websites
---
# Blogging with Jekyll

Over the past nearly 10 years I've tried numerous times to maintain a 
blog.  I enjoy writing and figured it would be a good way not only to practice 
the skill, but to share my thoughts with others.  I don't really care whether 
anyone reads my work, to be honest; I just want to write. <!-- more -->

The problem is that, while I don't care so much if I'm read, I do want 
to be able to keep my files and refer back to them from time to time -- 
something 
of a journal (which is what the blog was originally conceived to be). That means 
that I need the writing in form that is easily saved and retrieved. Another 
concern has been that I be able to write from essentially any computer, any 
where.  I started, as most folks do, on Blogger, then moved to Wordpress, each 
time abandoning my work and the platform, as I moved to another. That's not what 
I intended.  Making the process more difficult is that the writing is stored in 
a database. This makes retrieval of the raw data difficult, particularly if 
you've forgotten the password, or the database is corrupt, etc.  And, to be 
honest, those platforms are simply more complex than my needs. What I needed was 
a simple, easy to use platform that allowed me to maintain a file of my work.  

## Flat files

A year or so ago I became aware of flat-file blogging systems such as 
Grav, HTMLy, Pico, and the like.  These were awesome!  They allowed me to write 
my entries in plain text or Markup, upload the file to my server and, Viola!  I 
had a blog.  These were awesome -- and still are. On the whole, these systems 
meet my needs but, being the curious soul that I am, I wondered if there were 
other ways.  Wouldn't it be nice if my setup didn't depend on which PHP version 
I was running?  Wouldn't it be nice if the system didn't break every time 
something changed on the back end?

## Amazon Web Services

A few weeks ago I started playing around with Amazon Web 
Service (AWS) 
S3 storage.  One of the things you can do with S3 is serve static websites.  
Cool.  the kicker is, of course, that the site must be static.  Static websites 
have some advantagses.  First, any webserver can serve html files, no special 
resources or support files needed.  HTML is the reason webservers exist and was 
the standard for early websites. Another advantagse is that a static site is not 
subject to server-side scripting issues. This means that it doesn't matter 
whether you have the right version of PHP or PERL installed; the site will 
simply work.  A third advantagse is that if you ever decide to move your site, 
you simply copy the files to another server and you're in business, no fiddling 
needed.

To test out the AWS webserver with S3 I started with the website 
automatically created by Weewx, a linux based weather software to serve data 
from my local personal weather station.  I uploaded the files and, lo and 
behold, it worked like a charm!  There was just one problem: To keep the weather 
information current, I needed to upload the files every 5 minutes.  This 
identified one of the problems with static websites -- all files get uploaded 
every time.  I was uploading somewhere around 85 files every 5 minutes.  In a 24 
hour period that was about 24,500 files. Each file is a PUT, in AWS terminology, 
so I was uploading a boatload of files every day.  S3 allows up to 2,000 puts 
per day and charges &#36; 0.005 per 1000 files after that.  It would end up 
costing 
me 12 cents a day to maintain that site.  That's not unreasonable -- less than 
$4 a month. But not necessarily cheap either.  I can buy full support web servers 
for about that price and not worry about upload, storage, DNS (AWS charges for 
DNS services, too), or bandwidth costs. But, there are other uses that wouldn't 
cost as much.

One such use is the blog. Now, Grav, Pico, and such, all require PHP, 
which is not available in S3.  So, to do a blog on S3, I needed a static site 
generator that would create the site locally, then upload them generated files 
to the server.  [StaticGen](https://www.staticgen.com) is a great site that 
lists dozens of static site generators, together with basic information about 
them and their relative popularity.  Jekyll is, by far, the most popular. Also 
pretty popular is Hugo.  I've played with and like both.  Unlike Jekyll, which is 
written in Ruby, and interpreted language, Hugo is written in Go, which is 
compiled.  This means, generally, Hugo should be faster for rendering larger 
sites.  I can't speak to their speed, given the small number of pages I've 
created so far.  

### Trying Them Out

Just from early use, I generally like Hugo better.  I can't put my 
finger on why, though.  Initially, I found Jekyll a bit confusing to use.  While 
the documentation is extensive, it is not terribly user friendly in my view.  
Even while I'm actually fairly conversant in computerese, I didn't feel that the 
documentation got to the point in providing a new user with the resources needed 
to really get started.  That's one place where, I think, Hugo was better.  So, 
why did I end up using Jekyll?  Mostly because of themes.

I tried a dozen or so themes on Hugo.  Some worked; most didn't.  I'm 
sure it had much to do with user error, but I didn't want to spend the time to 
troubleshoot.  The themes I tried in Jekyll just worked.  So, I went with 
Jekyll.

### My Plan

My plan is try Jekyll for a while and, if I do end up changing, it 
shouldn't be be that big of a deal.  I suspect, though I haven't tested it, that 
the files should be easily converted between the two; they both use Markdown. 
