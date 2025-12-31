---
title: 'Exploring Meshtastic and LoRa'
date: 2025-12-19T17:09:36-05:00
draft: true
categories: "Technology"
tags: ["meshtastic","communications"]

---
Many months ago I started hearing a good bit about a technology referred to as "Meshtastic". Meshtastic is a decentralized mesh communications network that uses LoRa radios to provide communications, particularly in situations where other technologies such as cell service are not available.

The first question, of course, is "what the heck is a LoRa radio?"

I'm going to avoid getting into the weeds here, but LoRa is a portmanteau of 'LOng RAnge' and refers to a technique to communicate over long distances. That technique involves "Chirp Spread Spectrum" to encode information in "chirps" or short pulses of data. Because much of the data transmitted by IoT devices is just a few bytes, LoRa is an ideal technology for IoT and, in fact, is often used for exactly that purpose. A LoRa device, for example, could be used to communicate with an remotely controlled gate, issuing commands to open or close the gate, or to check its status.

A couple of unique properties of LoRa is that it is capable of sending signals long distances (think kilometers rather than meters) and can acheive this using very low powered devices.