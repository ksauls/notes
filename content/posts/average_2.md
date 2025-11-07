---
title : "Linux For the Average User -- Getting Work Done"
date : "2025-10-29T19:24:42-04:00"
dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "linux", "technology"]
categories : ["",""]
showFullContent : false
readingTime : true

---
This is part 2 of an ongoing series on moving away from Windows and onto Linux.  In this post we'll explore several alternatives for the most common  programs that the average user is likely to use, along with a few o their pros and cons.

___

If you watch most of the Linux related videos on Youtube it becomes apparent pretty quickly that most of those videos are aimed at "power users".  That is, they get pretty deeply into the inner workings of the operating system, often using a range of commandline tools to get work done.  The average user, particularly the new ones coming from Windows aren't really interested in those details. They want to know how to get things done. Preferably, using tools that are similar to, and as easy to use, as the one's they've become accustomed to on Windows.

If this describes you, then hang around. We're going to take a look at the most common programs most users need together with a few more specialized tools that an average user might want. And, we'll briefly look at some pros and cons of those tools.


## Office Suites

Let's start with probably the most common tools: Office Suites. Most people use Microsoft Office (or now Office 365). It's a great set of tools and one that I used for years both in my working and personal lives. There are a few problems with O365.

First, it's not cheap. Today you're expected to pay a subscription to continue to use those tools. Forget to pay your subscription and you'll lose access to the documents you've created. My wife discovered this when she went to look up some info she had stored in an Excel spreadsheet only to learn that because she had canceled her O365 account, she could no longer access that data. Bummer!

Second, your information is stored in the cloud. For some people, that's okay. For others, not so much.

Third, for most people Office 365 is overkill.  The suite includes programs that I'd wager most people never use and, in fact, have no idea _how_ to use them. Nor do they have a need for them.  But you're paying for them, nonetheless. Even tools that you might routinely use such as Word or Excel has far more functionality than probably better than 90% of people never use and, again, have no idea how to use or even why you'd need them.

In some ways the tools I'll discuss here are not dissimilar to O365.  They, too, have functionality that you don't necessarily want or need. But, with a couple of exceptions, you're not paying for those extras.

### LibreOffice

First up is [LibreOffice](https://libreoffice.org).  The general consensus is the LibreOffice is the best alternative to O365. The LibreOffice suite consists of Libre Writer (Word), LibreCalc (Excel), LibreBase (Access), LibreDraw (Diagrams), and LibreImpress (PowerPoint).

For most documents, LibreOffice is fully compatible with MS Office documents. That is, it can open, read, and edit documents generated in the MS office products. Similarly, documents created in LibreOffice are easily read and edited in MS Office.  Issues generally only emerge when documents are highly complex, have special formatting, or include Macros.

The user interface for LibreOffice is not as fancy or as "modern" as O365 but, instead, is more reminiscent of the older version of MS Office. And, while most of your tool bar options are the same, and even in the same locations, there are a few that are not where you'd expect.

Overall, though, LibreOffice is as easy to use as MS Office and produces the same quality output. Windows users will experience little friction moving from Word or Excel to LibreOffice Writer or LibreOffice Calc. Your remains only on your local computer unless you choose to upload it to a cloud service e.g. Dropbox, Google Drive, etc.

LibreOffice is Free and Open Source Software, meaning that it is free to use, share, and modify. That said, if you use it regularly and like it, please donate to help support the project.

### OnlyOffice

Like LibreOffice,[ONLYOFFICE](https://onlyoffice.com) is a great option. And, like LibreOffice, it is free and open-source, though unlike LibreOffice which is owned by the non-profit organization,_The Document Foundation_, ONLYOFFICE is owned by the Latvian software company, Ascensio System SIA. Ascensio has chosen to offer both an open source community edition which is free and an enterprise edition.  For personal use, there is no advantage to the enterprise edition.

ONLYOFFICE has great compatibility with MS office documents though, like LibreOffice, special or complex formatting, some spreadsheet formulas, macros present issues.  For most home or personal users, these are unlikely to be stumbling blocks, but I would be remiss in not mentioning them.

ONLYOFFICE can do Optical Character Recognition (OCR) allowing it to translate most PDF documents into editable text. In addition, you can annotate and edit PDFs directly, though the outcome isn't always what you might expect. This isn't really ONLYOFFICE's fault, as PDFs are highly complex documents and there are very few programs outside of Adobe that can consistently convert PDFs.  That said, you can also import pictures of documents and ONLYOFFICE will convert them.  Pretty nice feature, that.

As a suite, ONLYOFFICE can create and edit documents, spreadsheets, and presentations. You can also fill out forms, edit PDFs and create diagrams. In other words, just about all the same things you can do with any other office suite.

The interface for ONLYOFFICE is clean, easy to read, and well-organized and it has actually become one of my favorite editors.

### Other Options

There are other options for office suites, as well, including [WPS Office](https://wps.com), and [Softmaker](https://softmaker.com) office. While these packages include all of the programs you would expect from an office suite, they are not as popular. They offer free versions but you'll get your best bang out of the retail versions. I must also note that neither is open source.

## Email clients

One of the most common activities for most people is checking email. With the advent and proliferation of cell phones and the ubiquity of web portals for email, the need for a dedicated email client on you computer is fading. That said, there are a few email clients that remain popular. Unfortunately, they are also a bit outdated and, in my opinion, are overkill. Still, let's take a look at a few. Note that I've not routinely used any of these in quite some time.

#### Thunderbird

[Thunderbird](https://thunderbird.net) is a Mozilla project (the same as FireFox!) that has been around since, well, it seems forever. It was, in fact, my go-to email client for quite some time back about 10 years ago.  I haven't used it in a while, but it always worked well.  The interface is reminiscent of Outlook, so you should feel pretty much right at home.

Like Outlook, it incorporates calendar, notes, and task (todo) functions out of the box.

Setup is generally fairly straight forward, though I've encountered challenges getting my email provider set up on it. The exact reasons for this I'm not sure. One thing to note, though, is that many email providers are now requiring app-specific passwords in order to connect to email clients (Mine does!) making setup a bit more challenging.

Overall, though, Thunderbird is a solid option.


#### Evolution

Like Thunderbird, [Evolution](https://help.gnome.org/users/evolution/stable) has been around a long, long time and has seen many revisions.  I've come to the conclusion that most GUI type email clients are pretty much the same, offering email, calendar, notes, and todo functions.  Evolution is no exception so it comes as no surprise that the setup and function of the client is similar to Thunderbird.

Like Thunderbird, the interface is similar to Outlook and, while both of these clients used to have outdated looks, today the interfaces are fairly clean and well-organized.

#### Geary

[Geary](https://wiki.gnome.org/Apps/Geary) is a bit different from the two above in that it is a mail-only app.  No calendars, notes, or todo lists here.  So if you're someone who prefers separate apps for those things, Geary might be right up your alley.  The interface is clean and straight-forward. In a phrase, it "just works".  I'm rather partial to Geary from the last time a used it a few years ago.  But like the others, setup can be a challenge, particularly if your provide requires two-factor authentication or you need to create an app-specific password.

#### Other options.

Frankly, most people today use their phones for accessing their email and that is actually what I recommend. While you can use any of the above clients with ease, it may be just as easy and convenient to use your provider's web portal for email.  If you don't want to have to open a browser and type in your URL, etc. You can create what's known as a Web App on your desktop and it's actually pretty easy. Some Linux distributions include an app to assist you in this process making it fairly trivial to accomplish.


### Getting These Programs

While I have included links to all of the key programs mentioned, most are available for download through your desktop's Software Manager program. Of course, if you're a command line person, you can also download them via your package manager (though if you know _how_ to do that, you already know you _can_!).

---

This post is getting a bit long (almost 1600 words at this point) so I'll say "adios" for today.  Next time I'll cover a few more alternatives for software that the average user might find useful.
