---
title: My History with Self Hosting
date: 2024-05-20
author : "Kevin Sauls"
publishDate: 2024-05-27
tags: 
  - projects
  - technology

---
# My History with Self-Hosting

My journey with Linux started in the summer of 2020 when I enrolled in an intensive course in IT designed for a specific ISP (which no longer exists). The course was provide through a state university in cooperation with that company and in conjunction with a state level push to encourage<!-- more --> tech companies to settle in Georgia.  I ended up not taking a job with that company. While was at the top of my class, the company decided not to extend an employment offer to me and so I moved on.  In retrospect, I think that was probably a good decision and the guys that were in the class with me all left that company and, honestly, I'm not sure where most of them landed.  Despite that, the class was still one of the most exciting and fulfilling experiences I've had. And, I left it with fairly sound skillsets in networking, programming (C and Perl, primarily), web development and graphics (which I still suck at).

In the intervening 24 years I've played with a lot of Linux computers and done a lot of interesting things. It was very shortly after completing that program that I begin self-hosting.  In those early days most of the sites where of the CMS variety -- Drupal, Wordpress, Joomla, MediaWiki, Dokuwiki, PHP-Fusion, PHP-Nuke, and the list goes on.  The challenge was that most of these required direct installation which almost invariably led to hours of trying to sort out the failed dependencies, troubleshoot a ton of issues and, in the end, nuking all that work for one reason or another.  While I absolutely loved learning about these different systems and enjoyed the challenge, in the end I really found that most of them were simply overkill for what I needed.  So, why did I do it?  Because I was curious about what made each system different and found the challenge itself fulfilling.

## Down the Self-Hosting Rabbit Hole
In the last five or so years, though, I've moved in different directions.  Rather than manually installing all of these different systems, I've moved toward newer technologies that make the process easier and allow me to try different things to find what works best for me. 
### Yunohost and Sandstorm
Probably the earliest packaged system was something like [Yunohost](https://yunohost.org). According to their website, Yunohost was created in 2012.  I probably installed my first version of it around 2014 or 2015 when I first starting futzing around with the Raspberry Pi. Yunohost, it seemed, was the perfect pairing to the RPI.  Along about the same time, I looked at [Sandstorm](https://sandstorm.io) which debuted in 2014. Both products do similar things -- making it easy to install web server apps on your local system.  Both had extensive app lists from which you could choose. The cool thing about both of these was that you were able to fairly easily install an app, see how it worked, see what uses you might have for it and, if it didn't excite you, easily blow it away.  The downside, of course, is there were fewer problems with the installs which eliminated some of the "fun" of learning and installing software 😀.
### Ansible-NAS
Over time I've expanded my computer stable from one desktop, one laptop, one server, and a couple of RPIs, to about a half dozen servers. This gave me the opportunity to muck around with Linux Desktop and to use "development" servers for play while not really disrupting the installations that I actually used.   As I did this I ran across another intriguing process option -- [Ansible NAS](https://ansible-nas.io) by David Stephens.  Whereas Yunohost and Sandstorm provided a GUI that allowed you to see the list of available apps and descriptions of what the apps did, Ansible-NAS used an Ansible script to set up your server and install the desired applications. To use it, you needed to learn a bit about YAML and how to edit Ansible scripts. I was back in my element of having to learn and figure crap out to make it work!  I loved Ansible-NAS!

Through mucking around with Ansible-NAS I started learning bits and piece of ansible.  Many of the scripts used in Ansible-NAS were based on work by Jeff Geerling, a fellow with a rather interesting resume.  [GeerlingGuy](https://jeffgeerling.com) authored a book on Ansible that I've only fairly recently starting studying.  I also follow his [Youtube channel](https://www.youtube.com/@JeffGeerling) as he does quite a bit with the Raspberry pi. 
### Then came Docker
My thirst to learn more, though, led me to Docker.  My early efforts with this technology was somewhat ... challenging.  I spent some time learning how to create docker-compose files and explored DockerHub but overall found the experience more confusing than anything else. Maybe that was because, as I recall, Docker didn't work well on the RPI at the time which was the only linux device I had available and Docker basically sucked on Windows and Mac (at least that's as I recall it).

Despite the early setback with Docker, I persisted and today I have somewhere in the neighborhood of two dozen docker containers running on two servers.  These containers provide everything from monitoring my IP cameras, to a Wordpress blog, a photography site, Calibre-web, my cloudflared instance, Jellyfin, and a host of other useful applications. The advent of management systems such as Portainer made managing the docker containers easier and accelerated my implementation of applications in Docker. Not all of the applications I use are in docker containers, however.  As I continued to play around with these newer technologies I ran into two other products that I *really* like: ProxMox and Unraid.

### Proxmox and Unraid Arrive on the Scene

[Proxmox] (https://proxmox.com/en/) was first on the scene for me.  I was intrigued by an OS that provided an overarching management structure for creating virtual machines, LXC containers, and general NAS type storage. In fact, while I had played with virtual machines for years through VirtualBox and VMWare, that was all done on my desktop system and while VMs were great for testing and playing with various distributions, I didn't see a lot of utility for daily use.  Proxmox, though, suddenly made the creation of VMs not only easy but quite useful. All of my docker containers running on the Proxmox box are running inside a VM.  When I'm learning something new, or testing out an new OS or whatever, it's easy to spin up a VM knowing that if I bork it, well, I just delete that VM and start over. No harm, no foul.

As I was delving into Proxmox, I also ran across [Unraid](https://unraid.net).  Unraid provides similar functionality to Proxmox with a few differences.  There are three primary differences between the two products:
* First is that while Proxmox is open source and free to use, Unraid has a free trial but does require a purchase in order to continue using the product past the trial period.
* Second, Unraid runs from a thumbdrive rather than from a hard drive.  As I understand it, once loaded, there is little to no activity on the boot disk (thumbdrive) so the thumbdrive allows you to use all of your storage disks for data rather than dedicating some or all of a drive to the OS.  That's a nice feature!  And, because my HP Microserver has an internal USB port, I can use that for my boot disk and don't have to worry about it being dislodged or lost.
* Finally, Unraid provides a host of applications that have presumably been optimized for the Unraid system that can generally be installed with a single click.  I believe that all of these apps are docker images, though I cannot be sure of that. Unraid also provides a variety of plugins that can be accessed from the web GUI.  If Proxmox has a similar feature, I haven't found it. (But, then again, I also haven't had a need for plugins, either.)

As it stand now, I have two machines,  an HP Gen10 Plus Microserver and a repurposed HP EliteDesk, acting as servers on my network.  The HP hosts the Unraid server and the EliteDesk hosts the Proxmox server.  Yes, I could probably consolidate everything onto one server. And, yes, it might be wiser to run Proxmox on one machine and have a second Proxmox as a backup / fallback device.  But for now, I'm happy with my current setup and they allow me some choice in where applications are hosted and expand my storage capabilities.

### What's Running, Where?
Proxmox:
LXCs:
* adguard
* motioneye
* shaarli
* vaultwarden
* wireguard (shut down at the moment)
* omada
* bookstack
* tillium
* dokuwiki
* tailscale

QEMU (VMs):
* Ubuntu server -- docker server with these containers
	* calibre
	* calibre-web
	* cloudflared
	* flame (a dashboard)
	* jellyfin
	* joplin sync server
	* KIWIX (this is a cool off-line Wikipedia and other server)
	* Navidrome
	* portainer
	* uptime-kuma
	* wallabag
* These are QEMUs but are generaly turned off unless I have specific need for them:
	* Fedora 
	* Windows 10
	*  Windows 11 

On the Unraid server:
VMS:
* Ubuntu server
* I spin up vms here as needed when I'm exploring something that does not have a docker image.
*
Docker containers:
* Agent-DVR
* apacheGuacamole
* Calibre (testing version)
* calibre-web (testing version)
* Excalidraw
* Freshrss
* Gitea
* Grav (local version of this website)
* homebridge
* Immich
* MariaDB 
* MongoDB (used for testing and will likely be nuked)
* phpmyadmin
* postgres
* raneto
* Redis
* Shinobi-pro-cctv
* StirlingPDF
* webtop (toying with this one for now)
* Wekan
* Wordpress

As you can see I muck around with a lot of stuff. And I'm still looking, exploring and adding new stuff along the way.  The one advantage (?) of Unraid is that the App store makes it easy to find new applications to install and explore.  More often than not, I'll install something, play with it a bit, then delete it, but sometimes I find something new and useful that becomes part of my everyday workflow.

What can I say?  I love playing with technology!
