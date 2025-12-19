---
title: 'What the Hell is a PoC Radio?'
date: 2025-12-19T11:35:16-05:00
draft: false
categories:
tags: ["technology", "radio"]
---
In my previous post I noted that I was getting back into Ham Radio.  For those not familiar, Ham offers a ton of opportunities for experimentation, learning, and exploring new ideas and concepts.  Part of what brought me back to radio was messing around with Meshtastic, a technology that allows for unlicensed communication between devices. It is commonly used for IoT type scenarios, but can also be used for messages ala SMS. Unlike SMS, though, Meshtastic and similar "LoRa" technologies don't rely on an intact infrastructure. That means that it can be used for areas that don't have cellular access and for those times when the cellular network may be down.

As  I began educating myself a bit more about this technology I ran across a number of other, related, technologies, all of which piqued my interest.  I'll get into those in later posts.  For now, though, I want to examine a newer technology which, quite frankly, I'm not quite sure  I fully understand its "why".

I'm talking about "Push-to-talk over Cellular" or POC radios. Now, one of the challenges of traditional radio is that it is generally line-of-sight. That is, the range of almost all radios is limited to, at most, a few dozen miles. There are exceptions to this but those exceptions apply only to licensed radio operators using HF bands or to specific atmospheric situations that allow for "tropospheric ducting" that creates conditions for longer-distance radio communication. In other words, long-distance radio communications are not for the average user.

PoC radios, on the other hand, can communicate across great distances.  If, for example, you are visiting in California and you want to talk with your spouse who is back home in North Carolina, and you both have a PoC radio, you can contact them as easily as pushing the "talk" button on your radio. That can be very convenient. You accomplish this because the radio takes advantage of the same cellular network used by cell phones. Rather than relying solely on radio waves, as traditional radio does, these radios rely on a combination of radio waves that are picked up by a cell tower, transmitted via the internet or other wired backbone, then re-transmitted to the receiving radio. Just like a cell phone does.

It's all a very intriguing idea. But I see questions and just can't seem to quite wrap my head around the need for this except in very specific scenarios.

My first question is, if these radios rely on cell service, why not just use a cellphone instead of spending a couple of hundred bucks on a device that you would need to carry around in addition your phone. And, by the way, these are essentially single-function devices and can only be used for voice communication[^1]. There is only one situation where I can see a valid use case for individuals: communicating while driving.  Most states have "hands-free" laws that prevent the use of cellphones while driving. Most allow for use of radios, so being able to communicate using a radio keeps you in contact with "home base" while staying within the law.

For businesses, particularly truck drivers, this can be a very useful tool. This would allow a company to communicate directly with a driver no matter where in the country that driver might be. the PoC providers also tout the use of theses devices for warehouse communications and so on. Living in an area with a large number of huge warehouses, I can see that as being useful. On the other hand, most warehouses have a lot of metal which typically blocks cell signals. Businesses can purchase business class radios and obtain a license that allows them to use specific, dedicated frequencies to accomplish the same thing, generally at a much cheaper overall cost and these will work even if the cell network is down.

Or, they can use MURS radios for internal communication at even less cost. When you see workers at Walmart and other big-box stores talking on the radio, chances are good it's a MURS radio.

The problem with using PoC here is that it relies on cell service. If there is no cell service in a given area, well, there's no PoC service, either [^2].

A second problem I see is that it is not a general purpose radio.  With traditional radio, I can send out a message and it can be received by any number of individuals. Even those unknown to me. If there's an emergency, for example, and I need help I can send out a general call and get that help mobilized fairly quickly. And locally.

PoC radios are paired. This means that when I push-to-talk, I'm reaching out to the specific radio that is paired with mine. You can program multiple radios to respond to your radio by setting up talk groups, but those are still limited to only those that you've specifically designated and not all phones can be programmed that way.

So I'm still on the fence on the utility of these radios. There's a part of me that does see some legitimate uses. The other part of me thinks it's a solution in search of a problem. And I think it's rather telling that this technology was developed and marketed in the 1990's by Nextel. It clearly never took off and Nextel, at least in the US, no longer exists.  








[^1]:I have read that some phones may have web browsing capability, but I haven't been able to confirm that. 
[^2]: Some producers of PoC phones state that you can still use the phone "off-grid". I'm at a loss to understand how this can be true given that it relies on cellular service to function. 