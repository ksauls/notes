---
title : "Self-Hosting for 'Tech Independence'"
date : "2025-09-15T09:52:44-04:00"
dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["100days", "technology"]
categories : ["",""]
showFullContent : false
readingTime : true

---
As I've noted in several prior posts I self-host a fair number of services on my local devices. Now, there are any number of reasons why someone would choose to self host. For some people it is the challenge of learning new skills. For others it's about having a sense of control over your data. For others, still, it's about ensuring the future availability of services as it's well known that many services fall to the wayside overtime and nothing is more frustrating than to become accustomed to using a particular service only to have it disappear one day.

Still others hold little trust in the corporate services such as Dropbox, OneDrive, iCloud, Google Drive and the like. That lack of trust takes the form both of never being sure that the service will exist long-term and that the service is not somehow leveraging the documents you put into their vaults for marketing and other purposes. 

Now, I can't speak to whether there is any veracity to the concern that these companies are actually accessing your data to paint a more complete picture of you for marketing and other purposes. I simply don't know.  But it does concern me, somewhat, that they are willing to provide significant amounts of storage for free.  As the old saying goes, if you're not paying for a product, then you are the product. Again, whether that's actually true or not I have no way of knowing. 

And, of course there are also concerns about security.  Huge organizations like Microsoft, Apple, Google and the like are huge targets for those nefarious folk that take up the challenge of breaking the security of these sites. Thus, while the company itself may not be accessing your data, there's always uncertainly as to whether others have breached that security and gained access to your stuff.

In response to those concerns, though, many people do choose to host their own services either locally or on some other platform which they pay for.  They believe, perhaps rightfully, that doing so increases the security of their data and ensures that the services on why they rely are always available.

### Advantages of Self-Hosting

As suggested above, there are several advantages to self-hosting.  

#### 1. You have complete control over your data and your services.

If you are hosting all of your data and services on equipment that you own and control -- that is you have the computers in your own home -- you can be confident that the data are secure.  At least so long as you don't allow access from outside your network. Once you open your network to external access, there is no guarantee that your data will remain secure.

Now, there are ways around this issue. A VPN, for example, can provide access to those with the correct credentials to access your files from outside the network. I use tailscale and only I have the credentials for accessing my files.  Should I choose to grant access to others, I can limit what they can access. For example, I run an Immich server for my photos. I can limit access to just that server if I so choose. Similarly, I can create a file-sharing folder and limit external access to just that folder. Thus, even if a nefarious actor were to somehow access that server that would be all they could access. No harm to the rest of my system.

#### 2. You can ensure you have on-going access to services.

It is not at all uncommon for services to shutdown or simply disappear.  Often, some of the most useful services are niche services that are never able to generate the critical mass of users needed to be self-sustaining. Or, they never figure out how to monetize the service to cover its costs or to pay developers to continue to revise and improve the service. And, sometimes it's just a matter that they are one among many similar services and, while they may offer unique benefits, those benefits aren't sufficient, or sufficiently well known, to offset the competition. As a result, they falter and die. Or, as if often the case with Google, the company simply decides that the product is outside their core focus and choose to shutdown the service even though it may have thousands of happy users. 

Whatever the reason, many services do fade away over time. Sometimes without warning. For those who have come to rely on those services, or who have entrusted their data files to the service, this is a huge frustration and can be quite damaging if critical files were stored on the now defunct service.

To avoid this, many folks choose to host those services locally since many of these are open-source projects with the source code readily available.  Even if an open-source project is no longer maintained (not an uncommon situation) so long as the application continues to work the self-hoster can continue to use it. This, at least, will give them time to find a suitable replacement.

#### 3. You can save money with open-source projects

A third reason some choose to self-host (and I think I fall into this category) is that open-source projects that can be self-hosted are often free of cost.  There are some absolutely awesome programs available for self-hosting that are extremely well thought out, well designed, and generally meet my needs.  In fact, because many developers create their own versions of programs to meet their specific needs, it's likely that even if one program doesn't quite work for me, another will. Off-hand, I can't think of a single software need that I have that I haven't been able to find an appropriate open-source option for. 

** Financially support the services you use. ** Just to be clear, though, if you find a program that meets your need, support it financially. It costs money and time to develop a program and the developers deserve to be compensated for that time and effort. To me one of the great values of open-source is that you aren't spending money up front to purchase a program that may or may not meet your needs. Open-source allows you to "try before you buy". But once you've determined that it meets your needs, show your appreciation! 

But, wait, Kevin. If you're saying to pay for the services but also saying that open-source can save money. Isn't that contradictory?

Well, yes, in a way. There are two differences, I think. First, you're not paying for a product that you find, only after the fact, doesn't meet your needs. So, you're saving the costs of experimentation. Second, for most open-source projects, there is no set price. Thus, you can pay whatever amount you feel is appropriate.

#### 4. Security

By holding all of your data in your home, you're able to limit who has physical access to your devices. Beyond simply securing the network, physical access is a significant consideration in securing your data. Knowing who has access and when, can be helpful in ensuring that your data are secure.  Relying on security for a data center may or may not ensure that the data are safe. After all, all it takes is one pissed off employee to do significant damage.

### Disadvantages to Self-Hosting

Just as there are advantages to self-hosting, there are also some downsides to consider.

#### 1. Cost

On the face of it, self-hosting should be cost efficient. After all, you're not paying for those cloud services (assuming you're not using the free versions). But, there are still costs.  Unless you already a spare computer lying around, you'll need to purchase a computer and the necessary hard drives for data storage. That is a one-time cost, but can be rather pricey. 

Also, unless you're solar powered, you're going to be paying for the electricity to run those services. Now, in my area, I'm paying something like 12 cents per kWh. So those costs are not huge. But in other areas, cost of electricity may absolutely be a factor.

Don't forget, too, that while computers are generally pretty reliable, they can and do fail. So you may have maintenance costs either in repairing or replacing equipment. Power outages and electrical storms to wreak havoc on a computer system!

#### 2. Required skills

While self-hosting today is significantly easier to accomplish than it was even just a few years ago, there is still a learning curve involved. Most services are available as docker images but you need to have the knowledge and skills to set up those services in docker. 

Some products, such as CasaOS, Yunohost, etc have aimed to make the process easier, but I've yet to use one of those products that didn't end up having some issues that required troubleshooting. If you lack the skills for troubleshooting network and/or software issues, then self-hosting is going to be a challenge.

#### 3. Data security and integrity concerns

Under advantages I noted that security is a benefit of self-hosting. It is also disadvantage. Why? Unless you are skilled in the basics of network security, you may inadvertently expose your data to the the internet eliminating any security benefits.

From an integrity stand point, unless you have implemented a secure backup plan and make regular backup both on-site and off-site, your data cannot really be said to be secure. Hard drives do become corrupt for a variety of reasons, including those power failures and electrical storm issues I mentioned above.  And, if you are using an off-site backup target, you are now providing an opening for security concerns.

And then there's the simple concerns around theft or fire.  Someone breaks into your house and steals your computer, well, there goes your data!  The same is true if your house burns down. I read a lot of folks who do back ups but they store them on local devices. Having copies on two devices is better than none, unless all those devices are in the same location.

#### 4. Hosting off-site as an option

Periodically I run across articles that walk you through how to set up a VPS on an external service like DigitalOcean, Vultr, or Hetzner (and a host of others) that you can use for your offsite storage. These are great solutions, particularly for the concerns around fire, etc.

Often, these options are posited as ways around using Google Drive, iCloud, etc. While creating a VPS and storing your data there may be a better alternative to the more corporate services, I'm not sure they're really any more secure and, it seems to me, contradict the whole idea of not trusting outside sources with your data. Aren't you simply shifting your trust from, say Google, to whatever service that's hosting your VPS? Is that really any more secure?

Possibly. After all, your small VPS isn't likely to be target for nefarious hackers in the same way Google might be. So there is some 'security through obscurity'. And, that also presumably eliminates the likelihood that your data are being mined for information about you. This is especially true if you encrypt your data and use SSH to access your files. But, again, this requires skills that you may not have.

### So, What Am I Saying?

At the end of the day, I love self-hosting many of the services I use. I self-host as much for learning purposes as I do for any other reason. Am I particularly concerned about data security? Not really. The data that I feel are important I store on my local device only. Then, again, there is almost nothing that I have that is so important that it cannot be replaced. 

For those that are concerned with privacy and want to feel good that their data are not being mined, keeping your data local only, or creating a VPS with encrypted storage may be the way to go (assuming you have the skills for it). I'm just not convinced that the need is really there and that it justifies the costs of renting a VPS.

