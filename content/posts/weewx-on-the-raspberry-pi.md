---
title: 'Weewx on the Raspberry PI'
date: 2017-11-04
categories:
    - projects
tags:
    - weather
---
# Weewx on the Raspberry Pi
I've always loved gadgets.  When the first Raspberry Pis came out a few years ago, I was pretty confident that eventually, I'd get one.  About three years ago I decided I wanted to build a media server and the RPI seemed the perfect tool for the job.  While it works, it didn't do all that I had hoped.  It wasn't the device's fault; the software just didn't quite match up with my particular use case.  So, the device sat idle for a while.  5}
<!-- more -->


Eventually, though, another use came along in the form of a VPN server for my internal network. For this I used the excellent [SoftEther VPN](http://softether.org) software.  If you have need for a VPN server to access your internal network, I strongly recommend this software.

Along the way, though, other uses for the little device began to emerge.  One 
such use is to provide some of the weather data that I couldn't provide via my 
[Meteobridge](http://www.meteobridge.com/wiki/index.php/Home) device as I 
outlined in [this post](../changes-in-my-weather-station).

While the Meteobridge device could provide almost all of the data I needed to serve the weather website, it cannot generate NOAA-type files in order to feed some of the scripts I run on my website. So, I started looking for alternatives.   In keeping with my motivation for moving to the Meteobridge, I didn't want to have to run a Windows machine. Rather,  I wanted another small, low-power device.  the RPI came to mind.  After doing some digging around I discovered [weewx](http://weewx.com), an opensource software that did exactly what I wanted.

In truth, the RPI running weewx can do everything that the Meteobridge can do 
and a whole lot more.  Had I started a bit earlier, I might have chosen to use 
only weewx rather than Meteobridge. I believe that the Meoteobridge license 
comes up for renewall in a year or so.  I may chose to drop it in favor of 
Weewx.  

The one thing holdimg me back, though, will be the really nice imaging that 
Meteobridge provides for webcams.  I do have a webcam that I include on my 
website.  Having that really nice, clean banner across the bottom of the image 
makes for a very nice looking presentation.  

I guess I'll have to ponder that one a while!
