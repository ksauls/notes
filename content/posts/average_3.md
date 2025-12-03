---
title : "A Few Less Common but Still Useful Alternatives"
date : "2025-10-31T14:45:19-04:00"
dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["", ""]
categories : ["",""]
showFullContent : false
readingTime : true
series: ['Linux for the Average User']
---

This is part 3 of an ongoing series on moving away from Windows and onto Linux.  In this post we'll explore several more alternatives for the most common  programs that the average user is likely to use, along with a few of their pros and cons.

---

To be honest, the average user most likely does little more on their computer than write a few documents, surf the web, and check email. Given this, the software I covered in my [previous post]({{< relref "/posts/average_2.md" >}}) are more than sufficient to meet those needs.

However, there is a another set of folks, still average, but a little more specific in their needs, who do a bit more than just those few basic things. These folks might edit photos, create or edit videos and audio recording, create illustrations, and so on.  So today I want to touch on the Linux based tools that can meet those needs.  As a caveat, while I do work with these tool periodically I am by no means and expert so my evaluation of these tools is, of necessity, fairly limited. I am relying on the the internet community for helping me identify the pros and cons of these tools.

With that in mind, let's get started.

#### Photo Editing

Now, photography is one of my hobbies, so I do work with photo editing software at times. The "gold standard" for most people is Adobe Photoshop. It's a good tool and is part of the Adobe Creative Suite. It's also expensive and requires a subscription.  For people like me who are not professional photographers and don't edit on a regular basis, the costs of the subscription is just really hard to justify. Fortunately, there are some free alternatives.

[*Darktable*](https://www.darktable.org) is a great alternative to Adobe's Lightroom for basic photo cataloging and editing.  It's not as refined as Ligthroom and it isn't quite as easy to use. As one reviewer noted, Darktable doesn't hold your hand in the same way Lightroom does. But as with most software, once you start working with it, you quickly learn how to achieve your outcomes and from what I've read and what little work I've done with it, it holds its own against Lightroom in most situations. As with all open-source software, it's important to keep your expectations in check.  You're not going to get the exact same experience using free software that you will with paid software simply because corporations have more money to invest in the software and more dedicated developers. That said, the developers of this software (and most specialty open source software) are dedicated because they use the software they develop. They are motivated more by their own interests than simply getting a paycheck.

Another alternative to Ligtroom is [DigiKam](https://digikam.org). I've not really worked with Digikam but user seem quite pleased with it and form all I've read, it appears to offer a similar experience to Darktable.

There are several alternatives to Photoshop: GIMP, and Krita being the most commonly cited alternatives. We'll take a brief look at each of these.

*GIMP*

[GIMP](https://www.gimp.org) is the OG of photo editing software on Linux.  It is a very powerful program that is actually pretty much on par with Photoshop, though Photoshop has features that many photographers may not use such as graphic design and illustration (there are other open source tools for those actions if you need them). So GIMP is really focused on photo editing and nothing more.

That said, it is not all roses and teddy bears. GIMP currently does not support RAW files. That's where Darktable or another program called [RawTherapee](https://rawtherapee.com) comes in. They can convert your RAW files which can then be edited in GIMP.

GIMP is also missing features like generative fill, and AI related actions but if you're 'old school' and like to do your own work rather than letting a bot fix your photos, GIMP works.

Probably the biggest complaint with GIMP is the interface. It is not pretty but it gets the job done and it does so without subscription fees!

## Audio Editing

If you're into creating podcasts or editing audio recording for school, church, or wherever, Linux can meet your needs. There are a number of audio editors out there for Mac and Windows.  On linux, the 'old standby' is [Audacity](https://audacityteam.org) in a way that make sense.  Working with audio files is not difficult at all and, in fact, when I first started using it, I basically just jumped right in an started editing!  No major challenges.

As an alternative, [Ardour](https://ardour.org) is the new kid on the block. It's interface is beautiful and is well laid-out.  I haven't used Ardour myself, so I can't speak to how easy it is to work with. But other users seem quite pleased with it.  I will note that the general consensus is that Audacity's toolset isn't quite as robust as Ardour's. And this is apparently true even with the available plugins. In general, Ardour is seen as a more complete digital audio workstation for professional work whereas Audacity, with its simpler toolset, is geared more toward the occasional audio editor.

Regardless of which audio editor you choose, you'll end up with a quality end product with a great sound.  That said, software alone won't make a great product. Much of that comes down to the skills of the editor, but a good toolset can make that process easier and more efficient. Again, either tool will meet that need.

## Video Editing

The two key players here are [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve) and [Kdenlive](https://kdenlive.org). Both are great tools for editing video.  I need to note, however, that DaVinci Resolve is free to use for personal use and works great on Linux, it is NOT open source. If being open source is important to you, then you'll want to use Kdenlive instead.  There are also other options, including [OpenShot](https://openshot.org), [Shotcut](https://www.shotcut.org), and [Blender](https://blender.org). Each of these options have their pros and cons.

For example, if you're a beginner, only occasionally edits video, or just someone who want to learn abit about video editing, OpenShot or ShotCut are your best options.

For the more seasoned editor or someone who creates complex video projects, DaVinci Resolve is considered the industry standard and has many, many options even in the free edition. All of my reading suggests, too, that the hardware available from BlackMagic (the company behind DR) works well with Linux.

I'm not going to get into the details of these programs just yet. I have plans to make specific posts that go into more details on many of these programs later on in the series.

### Illustration (Graphics) Software

Adobe has Illustrator, a powerful vector graphics program. If you don't know that that is, then this section is most likely to be of little value to you.  In short, Illustrator allows your to create detailed graphic designs and illustrations (hence the name). As is the case with the other Adobe products, Illustrator is considered the standard.

Linux offers several options that will meets the needs of the vast majority of graphics people, especially those with limited skills -- that is, the average user.

*Inkscape*

On Linux, [Inkscape](https://inkscape.org) is the standard and the grandaddy of them all.  It is a vector graphics program and has a full set of drawing tools, can be used with tablets (e.g. Wacom) and can do pretty much anything the average illustrator would need. I'm not an illustrator so I've only touched the program a few times. One Youtuber notes that she uses Inkscape for all of her thumbnails and seems quite happy with the program.

*Krita*

[Krita](https://krita.org) is more along the lines of MS Paint or other drawing programs. It is a raster graphics program as opposed to vector graphics.  What's the difference? Raster graphics are made up of pixels. That is, you're manipulating the pixels in an image.  Raster graphics programs can be used to edit photos, for example, because you're addressing the pixels in the image. While raster graphics are great for details, they don't scale well so your images become less detailed and more pixelated as you increase the size of the image. Vector graphics, on the other hand, uses mathematical formulas for drawing paths the create the images.  This allows you to scale the image almost infinitely without sacrificing details.

Both raster graphics and vector graphics have their strengths and if you're an illustrator (or illustrator wanna be) then you might want to have both in your toolbox.

### Wrapping up

As mentioned in the opening of this post these programs are not as commonly used by the average user as, say word processors. But there are still a significant number of folks who *do* use these programs and if they're switching from Windows to Linux they'll want to know about their options.

Hopefully, this short post will provide some foundational guidance.
