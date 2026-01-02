---
title: 'Exploring MeshTastic and LoRa'
date: 2026-01-04
draft: true
categories: ["Technology"]
tags: ["mesh_networks"]

---
Many months ago I started hearing a good bit about a technology referred to as "MeshTastic". MeshTastic is a decentralized mesh communications network that uses LoRa radios to provide communications, particularly in situations where other technologies such as cell service are not available.

The first question, of course, is "what the heck is a LoRa radio?"

I'm going to avoid getting into the weeds here, but LoRa is a portmanteau of 'LOng RAnge' and refers to a technique to communicate over long distances. That technique involves "Chirp Spread Spectrum" to encode information in "chirps" or short pulses of data. Because much of the data transmitted by IoT devices is just a few bytes, LoRa is an ideal technology for IoT and, in fact, is often used for exactly that purpose. A LoRa device, for example, could be used to communicate with an remotely controlled gate, issuing commands to open or close the gate, or to check its status.

A couple of unique properties of LoRa is that it is capable of sending signals long distances (think kilometers rather than meters) and can achieve this using very low powered devices. These properties make it possible to use LoRa for remotely controlling gates, monitoring and controlling temperature and humidity and farm and other industrial type buildings, and for a host of other purposes all using relatively inexpensive low-power devices.

The ability to send short bursts of data over long distances is also useful for communications using SMS type messages.  This is where MeshTastic and its younger cousin MeshCore come in. Using small, very inexpensive devices allows users to communicate with each other no matter where they are. No cell service needed. This communication can be either short text messages or even GPS coordinates so that the user can be located should an emergency occur. The overall idea is very cool and  I can see some definite uses for the technology.

While there are a (very) few self-contained devices that allow you to create and send/receive messages from the single device, in most cases two devices are needed: The LoRa device which is a small $30-ish radio device and your cell phone. You install an app on your phone which communicates via Bluetooth with the radio device and provides the interface for creating messages.  It's important to note that this is text only; there is no option for voice messaging. And, while some of the radio devices include GPS (at additional cost) the devices can use the GPS in your phone to provide location data.

To make the technology even more useful, these devices can create a mesh network (hence the name!) to extend the range well beyond the reach of a single device or to overcome physical obstacles such as mountain ridges and so on.  Many users install repeaters intended to help create the mesh network. This removes the reliance on other users to be within range for the network to work as repeaters are often located at the highest points in an area.

Being a tech nerd, I became quite interested in the technology and began exploring it.  Despite the fact that it's actually a pretty simple technology, I'm still experimenting to understand its ins-and-outs.

As I mentioned, there are currently two implementations of the technology: MeshTastic and MeshCore. Both are based on the same underlying LoRa technology but implement the technology slightly differently.  As I'm still learning, some of the information here may not be quite accurate, so bear with me.

Both technologies have the same purpose: to provide a means of communicating when no other infrastructure is available. The biggest differences from what I can tell, is in how the technologies are implemented.

Both products use "hops" to transmit a message. Suppose you send a message to your friend who is several miles away. It is possible that you might send that message directly to them because the two devices can connect. On the other hand, your friend may be out of range but there is an intervening device, either as another user or a repeater, that can pickup and forward that message. This is a hop.  MeshTastic allows for a limited number of hops. This can potentially limit the reach of your message. MeshCore, on the other hand, does not limit the number of hops. This can dramatically increase how far your message can reach.

MeshCore uses a more structured approach to building its network while MeshTastic is more ad-hoc in nature. MeshCore relies a lot on repeaters while MeshTastic utilizes adjacent client nodes to convey the message. That said, MeshTastic does utilize repeaters. Repeaters for both technologies can be located on maps: [MeshCore](https://meshcore.co.uk/map.html) or [MeshTastic](https://meshmap.net)

In general, MeshTastic is easier to set up and use and provide a good general use network. MeshCore on the other hand, is intended to provide a more robust managed network.

### Where I'm at in Experimenting

I've been playing with both technologies and have yet to decide whether either technology can actually be of use to me or not. And, if I decide that I do want to dig more deeply into it, which technology to implement. There is, of course, the possibility of using both, though it would require some additional hardware. Like any other technology, though, the more options you have the more challenging it becomes to use. When heading out, a decision has to be made on whether to carry the MeshCore devices or the MeshTastic devices. Unfortunately, they do not interconnect.

As I learn more I'll share my learnings here.

In the meantime, check them out for yourself. It is a lot of fun!