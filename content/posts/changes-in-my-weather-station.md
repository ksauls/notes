---
title: 'Changes in my Weather Station'
date: 2017-11-01
categories:
    - projects
tags:
    - weather
---
# Changes in my Weather Station

For the past 8 years I've managed a personal weather station consisting of a 
Davis Vantagse Pro and a Windows computer running the excellent Weather Display 
software.  Last December I decided that the inexpensive computer I was running 
the scripts on may well be coming to its end-of-life and went looking for 
alternatives. Another goal of this move was to lower my cost of operations.  The 
Jetway computer I was running didn't use a lot of power, perhaps 25 W, but if I 
could do better, I would. After all, at 25 watts, that's about 219 kW or $26.25 
annually.  With the growth of small computers such as the Raspberry Pi, I knew I 
could do better. <!-- more -->

After some mucking around, I found Meteobridge.  Meteobridge is software that 
gets flashed onto a TP-Link TL-3060Mr (and some other similar devices).  While 
not nearly as full-featured as Weather Display,  the Meteobridge software works 
well and sends the data to my website without problems.  Best of all, the total 
price was about $100 and will use about 0.6 W, that's about 5.256 kW or a 
whopping 63 cents per year!  The whole shebang will pay for it self in about 3.5 
years.  Sweet!

But the Meteobridge has a couple of caveats.  One is that it doesn't store data, 
so a separate device is needed for that (it does have the ability to save to a 
mysql database hosted elsewhere). Nor does it generate the NOAA style reports 
that are needed for some of the calculations and webpages that I generate (for 
example, the freeze data -- first and last freeze dates for the year, number of 
days below freezing, etc). Another caveat is that the updates are available only 
for two years, then you have to buy an update license.  Having not had to do 
that yet, I don't know the cost.  Perhaps another caveat is that the product is 
dependent on the Meteobridge server.  The OS is not actually stored on the 
device but is downloaded each time the server reboots. Now, my server has run 
for as many as 133 days without a hiccup, so that doesn't happen often. But it 
could.  This can be mitigated by including a USB stick on the device so that the 
data are saved, together with a copy of software for those eventualities when 
the MB server isn't available. Good to know!

So, for now, I'm sticking with the Meteobridge.  Overall, I like it and have 
found workarounds to the issues that have cropped up.  One of those is the 
Raspberry Pi and weewx.  I'll deal with that in another post.
