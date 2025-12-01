---
title: Connecting the MacBook to the Edgerouter VPN
date: 2018-02-02
author: "Kevin Sauls"
taxonomy:
    categories:
        - projects
    tagss:
        - technology
---

# Connecting the MacBook to the Edgerouter VPN

Today I fixed a problem that has vexed me for some time.  Reading through the 
search pages, it seems it has vexed quite a few others, as well.  I thought I'd 
share my solution to this problem so that others might benefit.
<!-- more -->


What's the problem?  I've setup a VPN server on my Ubiquiti Edgerouter-X. The 
VPN works great with my Windows clients, but I've not been able to get my 
MacBook or iPhone to connect. Until today.  The problem turned out to be quite 
simple, though it took a bit of reading to figure it out. 

There are dozens of articles and posts on the discussion boards about similar 
problem and a multitude of solutions have been proposed. I turned on logging for 
the firewall that provided exactly zero useful information I did a tcpdump 
watching ports 500, 1701, and 4500 while I tried to connect. Lots of data, but 
nothing useful.  Finally, I ran across a single post -- I don't remember on what 
board -- that provided the solution.  The 
only one 
that 
worked, though has been this one.  I make no promises that it will work for you, 
but it is certainly worth investigating.

So, what's the solution?  When you're setting up your VPN you need to open three 
ports: 500, 1701, and 4500.  Take a look at the NAT tab in the Firewall settings 
of your GUI.  Is there an entry that points to a destination of 4500?  If so, 
delete it.  It seems that some UPNP process hijacks port 4500, which is needed 
to the MacBook to connect.  Deleting that entry frees up the port and allows the 
VPN connection to complete.  Everything has been working just fine since I 
deleted that pesky entry.

One word of caution: Be sure that the UPNP entry isn't required by some process 
that you want to use.  In my case, the rule pointed to a destination in a 
192.168.x.x network.  I don't use that network. My network is a 10.x.x.x.  I 
knew that I could safely delete that entry.  Before deleting yours, double check 
what it might be serving.  So far as I know, you can't change the ports for the 
VPN, the client determines that.  But, you might be able to change the port on 
the UPNP device, if you need to free up port 4500.

YMMV; good luck!
