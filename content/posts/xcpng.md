---
title : "A Brief Test of XCP-ng vs Proxmox"
date : "2025-09-22T11:22:35-04:00"
dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "technology"]
categories : ["",""]
showFullContent : false
readingTime : true

---

For the last year or so I've been running a Proxmox server that hosts several virtual machines (VM) one of which, itself, hosts multiple docker images for services on which I rely. In addition to the VMs, I also run several LXC containers on the Proxmox server that provide some additional resources I frequently use.

While watching some videos a few days ago  I ran across a video where the presenter was demonstrating the use of XCP-ng. If you're not familiar, XCP-ng is similar to Proxmox in that it is a type 1 hypervisor. A type 1 hypervisor is the operating system that allows one to run multiple VMs as if they were on the bare metal. 

The two biggest differences between Proxmox and XCP-ng are:

A: XCP-ng is designed for enterprise use and, therefore, does not natively support LXC containers
B: Proxmox is designed more for consumer use and it DOES support LXC containers

XCP-ng is based on the venerable XEN Project which has been around since 2003. Somewhere along about 2008 or so I gave Xen a try on one of my systems. At the time there wasn't a lot of documentation that I could find, and so I ended up frustrated and gave up. Of course, that was early in its life-cycle and I wanted to see how well it had improved in the interim.

Proxmox has been around since 2008 and is based on Debian Linux. There are some other differences but, to me, these were the most significant. Both hypervisors can host a variety of guest systems. While I haven't tested XCP-ng with more esoteric OSes like Haiku I have done so with Proxmox and encountered no issues.


All of that said, I decided to give XCP-ng a go and see whether it might fit better into my workflow.

Installation was pretty simple. XCP-ng, it seems, will install on just about any hardware. In this trial, I used a Dell Wyse 5070 with a Celeron J4105 processor and 8GB ram. It took me a bit to figure out the TUI for the program but then remembered that there is a built-in web-based management interface (XO lite). XO Lite is a less complex version of the Xen Orchestrator software that can be used to manage any number of hosts as well as all their guests.

Now, this was a rather preliminary test so I didn't spend a ton of time on the system. I did spend enough to know that there are limits that Proxmox doesn't appear to have. (I admit that I did not dig deeply, so there may be ways to work around these limits.) The biggest one for me was provisioning memory. 

Proxmox allows provisioning memory in a way that essentially sets a limit on the amount of memory a particular VM can consume. This means that if the VM doesn't require all of the assigned memory that memory is available for other VMS. Similarly, if a specific VM requires additional memory for some event, it can take the memory needed -- up to the specified limit.  XCP-ng, however, does not appear to allow this. Memory that is assigned to a specific VM is no longer available for other VMS. This limits the number of VMS you can run at a given time. (Memory is released if the VM is shutdown but this also means that if another VM takes up that memory, you cannot restart the first VM. So, if you shutdown VM "A" its memory is released so that when VM "B" starts, it can take that memory. However, VM "A" can no longer start because there is no available memory. As I mentioned above, there may be work arounds, I did read something about dynamic memory allocations but couldn't quite sort that one out in the time I gave myself to play with the program.

In terms of performance,  I didn't really note any differences though, again, this was a very limited test with just a few VMs (due to memory limits). 

In terms of managing the system, both provide -- or at least have available -- web-based management. With Proxmox that management interface is built-in and is pretty comprehensive, though at times a bit confusing. XCP-ng actually has two options. First is the XO Lite I referenced earlier. In addition you can apparently download the source code for Xen Orchestra, which is a much more complete and complex interface though it allows you to do pretty much anything you want to do with your system. Once downloaded you'll need to have the tools and knowledge needed to build the app from source, though the instructions are clear so that shouldn't be a big problem.

You can also, of course, buy a pre-built version of XOA (Xen Orchestra Virtual Appliance) from the Xen Project, though it is a bit on the costly side and not something the average home labber would choose to do.

So, after a short test, what did I think? 

I really liked the feel of XOA and felt that the system, overall, worked well and seems to be easy to manage. Since it is clearly aimed at the Enterprise market, I'm confident that it can handle anything I throw at it.  

That said, I'm sticking with Proxmox for now mainly because  I feel like XCP-ng is simply overkill for my needs. And, too, I really like using LXC containers. Yes, I could set up a guest VM to host the LXC containers, but that seems to over complicate things (though I'm going to give this a try before I dump the system.)

