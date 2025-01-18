---
title: 'Updates on Technology Projects'
date: 2018-08-13
categories:
    - projects
tags:
    - websites
---
# Updates to Technology Projects

I've had several technology projects running for a while now and thought it was time for an update.

### Nextcloud, OnlyOffice, and the Like
Back in February I set up a Nextcloud server and incorporated OnlyOffice.  The concepts are pretty cool, but I have abandoned both of those projects.  In all honesty, having completed my dissertation, I write so little that requires a word processor that I've not yet found a need for OnlyOffice. And when I do need such <!-- more -->services, I have LibreOffice available on all of my computers.  MS Office is on its way out since I no longer need to power of a word processor for my writing and my licenses are beginning to expire. (I still have a couple of licenses that will be expiring soon.)

In terms of document storage, I haven't figured out what benefit Nextclod provides me over a simple document storage device such as my linux server.  I can access everything I need via the VPN.  This approach not only helps keep my data more secure by not opening it to the web, but just streamlines the whole process.

### Jekyll
Another project I started back in the fall was to use Jekyll for my website.  I am quite conversant in database design, management, etc and fully understand the benefits that a database e.g.  Mysql, postresql, etc can provide.  On the other hand, I also know how difficult it is to move your writing to another platform or to simply extract your work in a human-readable way.  The promise of Jekyll and other plaintext platforms is that you can write and store your writing in a human readable format that can easily be moved to different platforms, printed, or otherwise shared with ease. As you may infer from this site, however, I've moved to Grav, which is a bit more intuitive and easier to work with.  

Several factors led to that decision.  Probably the most signficant is that creating a new post required too many steps.  Not only did I have to write and store the document in a specific location, I then had to run a script that would recompile the entire site, then upload the entire site to the webserver.  That doesn't make sense to me. And, to accomplish this required that I either remember the various commands for compiling the site and uploading it, or remember where I put the script that would run the commands for me.  If it's been a while since I wrote a post, there was no guarantee that I'd remember these things. 

Grav provides an option to use the writing tools through the admin page of the website to write, or I can write off-line and simply upload the one file to the server.  No fuss, no muss, and the page is immediately live.  Grav may present a little bigger hit on the server itself as it processes the page, but probably no more so than would be seen if I was using a database driven site.

I did look at several alternatives, including YellowCMS, and Bludit.  I actually liked Bludit quite a lot and would have chosen it but for the fact that it lacked the ability to simply upload a page written offline.  It stores its page data in a JSON database file which would have required that I either write all my posts within the site, or manually update several JSON files in order to get everything set up correctly.  Not an appealing prospect.

### Self-Hosted Bookmark Site
Three projects that are rocking along well are the self-hosted bookmark, the RSS reader, and the read-it-later sites that I created.  Both of these run on a Raspberry Pi and work very well. In fact, I use all three relatively routinely.
#### Shaarli
After playing with several other scripts (Unmark, SemanticScuttle, and Shaarl, as well as a couple of others that I don't now remember) I settled on Shaarli.  I can't really say why, other than it seems to be the one that best meshed with how I work.  SemanticScuttle is still up and running and I do have bookmarks stored there, but I rarely send anything to it.  For this one, Shaarli wins the day.
#### FreshRSS
I don't think I really wrote about an RSS reader earlier but I played with several over the course of several months.  I realize that RSS reader use may be on the decline but I like being able to quickly scan headlines of my favorite sites.  I have to manually mark the entries read and to manually refresh the page to update the headlines, but that's okay.  I find FreshRSS useful and that's what counts.
#### Wallabag
Was there ever a question that Wallabag would persist? Not for me.  I'm not sure why I never really cottoned to Pocket.  It does the same thing as Wallabag, but for whatever reason I find Wallabag useful.  I try to keep my reading list there pruned so I don't end up with hundreds of unread pages.  But being able to save not only the bookmark to a page, but also the content of that page is quite useful.  I also like that the advertising is stripped from the pages and they are made more readable and easier to print if  I want to keep a hard-copy of a particular article.  Pocket may have those capacities (I'm sure they do) but Wallabag is the service for me and it runs on my servers, keeping things simple and ensuring that they won't suddenly disappear when the company goes under.


There you have it: updates to several of my technology projects.
