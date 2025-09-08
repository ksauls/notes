---
title : "Revisiting_OpenBSD"
date : "2025-08-13T10:58:53-04:00"
#dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : ""
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "technology","OpenBSD"]
keywords : ["", ""]
#description : ""
showFullContent : false
readingTime : true

hideComments : true
---
# Revisiting OpenBSD

Roughly six months ago I documents my efforts to install [FreeBSD]({{< relref "freebsd" >}}) on a Lenovo X250 that I bought for that purpose. In that post I noted that the one problem I had with FreeBSD on that device was that the suspend/resume feature did not work. Since this was a laptop and my plan was to use it as a dedicated writing machine that I could take with me on the go, the inability to suspend and resume the device made the whole process a no-go. Yes, I could shutdown and reboot as needed, but I'm lazy and that just didn't work for me. Moreover, often times I'm just shutting the lid for short periods of time and so the shutdown and boot up for those short periods seemed a bit much.

Although I didn't document it at the time, I had tried other BSD based products, including NomadBSD and OpenBSD. NomadBSD also suffered from the suspend/resume issue, but OpenBSD, as I recall, did not.  Why I chose not to work with OpenBSD at the time, I don't remember. Somewhere in the back of my cluttered mind it seems to me that there may have been other issues that stopped me. I do recall thinking that OpenBSD was more challenging to configure and perhaps that's why I didn't continue on with it. 

Now, I bought the laptop specifically as an experimental device for trying FreeBSD.  With that experiment concluded, I decided that a great use for the machine was as a dedicated writing device and one that I could confidently take with me anywhere.  It was not expensives (less than $65 USD) so if I lost it, dropped it, or it got damaged there was no great loss.  All of my data are backed up to other devices so even my files were safe.  With all of that in mind, I dropped back to Linux Mint which is what the reseller installed on the device.  

Overall, LM is a great Linux distribution. It's easy to use and is highly reminescent of Windows which is why the reseller installs that particular distribution -- they focus on selling to folks that can't really afford a new computer. I like LM because it "just works". So, with no other use for the device, I set it up as a writing machine.  

My discussion on [emacs]({{< relref "learn_emacs" >}}) is based on using emacs on this device.

With that bit of 'history' out of the way, though, lets move on to today's real story.  I decided to revisit OpenBSD on this device. As usual, this decision was prompted by some comments on Reddit about OpenBSD that piqued my interest and reminded me why I wanted to use FreeBSD to begin with. So, I popped open the laptop, pulled out the LM disk, dropped the drive on which I had previously installed FreeBSD, downloaded the latest version of OpenBSD (7.7) and I was off to the races!

Now, one of the things to recognize about OpenBSD is that it installs a fairly minimal version of itself.  Unlike Linux distros that install a dekstop environment (DE) such as Gnome, XFCE, or KDE, OpenBSD installs FVWM which is, from my perspective pretty useless. So one of the first things I did was to install i3wm.  Now, I love i3 because it is very flexible, allows you to have multiple open windows which can be put into different workspaces so that you essentially have a distraction-free environment. If I need to pop out to the internet, a couple of keystrokes takes me to the workspace in which I keep an open Firefox browser. Another couple of keystrokes takes me to my Emacs screen which, again, is always open. A third workspace contains my shell so that if I need to do something from the commandline, it's just a key stroke away.

But, I also wanted to see about other DEs and so I also installed XFCE4. Works great! Everything pretty much works exactly as I would expect it to and the bonus is that SUSPEND/RESUME works correctly!  While I was never able to get suspend/resume to work with FreeBSD, apparently because of TPM and the locked bios, OpenBSD seemed to have no problem with this. I could never quite wrap my head around why TPM was a problem for FreeBSD with this, becuase Linux never seemed to have a problem with it. 

So, so good!  OpenBSD was doing all that I wanted it to do and I started thinking that maybe I'd leave it on the machine and move my work over onto it from LM.  Still, the experiment was not without its challenges.

Challenge #1:

Wireless internet on BSDs can be a challenge. OpenBSD is known for its compatibility with wireless cards and my install had no problem identifying the wireless card. That said, I couldn't get it to connect. After some digging around and some trial-and-error, I was finally able to get it to work. Now, many folks claim that the documentation for OpenBSD is great. I'm not so sure. I followed the instructions in the manual but couldn't get the wireless to auto connect on boot. I kept getting an "inet: bad value" error. And I could find nothing online about this particular error. 

All of my instructions said to configure hostname.iwm0 as:
``` 
join <SSIDname> wpakey <password> inet autoconf
```
And, that didn't work. Digging a bit further I found other recommendations to add different parameters, etc. None worked.

The confusing part was that if I initiated the connection from the commandline with 

``` 
doas ifconfig iwm0 join <hostname> wpakey <password> autoconf up
```
it worked.

Finally, I thought, "well, the error is related to inet and the only value given to inet was autoconf. I knew that autoconf *had* to be there, so I figured I'd remove the ``` inet ``` and, sure enough, that did the trick!  Now I can automatically connect to my wireless network.

Related to this, though, is that there is apparently no way to connect to a network from a list. In linux, you have a Network Manager that will identify all of the available wireless networks and allow you to choose the one you want to use.  This is extremely useful if you're moving around a good bit. Say, for example, that you're going to a new coffee shop and want to connect to their network. On Linux, this is trivial. Not so on OpenBSD. To do this on OpenBSD you need to
```
doas ifconfig iwm0 scan
```
Identify the correct network, then add that network to your ``` /etc/hostname.iwm0 ``` file. That's a lot of work simply to connect to a wireless network!  Once it's added, though, connecting is no problem. But, if you're only there for the day, adding the network to your file seems a bit overkill.

As of now, OpenBSD is still looking pretty good and I may stick with it for a while just to put it through its paces and see how well it works. There are quite a number of folk who have turned to OpenBSD as their daily driver and have found it to be ultimately as easy to use as any other OS. 

I guess I'll find out!


