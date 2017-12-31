---
title: "Home Automation"
description: "Adventures in home automation"
repo: ""
tags: [home-assistant, python, bash]
weight: 0
---
# Introduction
I wanted to automate some basic things in my apartment.

Here are the things I have automated so far:

- Turning on the air filter at night and off in the morning.
- Turn on a bedroom fan based on the temperature and time of day.
- Turning on sensors and camera for some basic security.
- Notifications when a package has been delivered.

I will update this page as I make more progress and have something worth
sharing.

# Home Assistant
I am using <https://home-assistant.io/> to accomplish my automation.

Home Assistant provides a nice framework for creating your automations and the
flexibility to expand as you like. It has a massive 
[library](https://home-assistant.io/components/) of already built components.

## Ongoing work
The main work I have done to improve Home Assistant capabilities are the
following:

### Blink Camera Automation
I have one camera which I use as a basic "security" feature. At the time,
there was no component already existing to use this in home assistant. So, I did
some research and found someone had already 
[reverse-engineered](https://github.com/MattTW/BlinkMonitorProtocol) 
part of the API. I used this a base for my script to add some basic 
functions(arm/disarm/status).

Later, the blink platform was integrated into home-assistant by a contributer.
<https://home-assistant.io/components/blink/>

### Wireless Tags Automation
I have two of these [tags](http://wirelesstag.net/). They can used for
temperature, humidity, motion and more. I am currently using them to monitor the
doors to my apartment and temperature. I made a python script to interact with
the wireless tags [api](http://wirelesstag.net/apidoc.html). This includes
arming, disarming and reading temperature/humidity data.

Motion automations are:

- Turning on the sensor when we leave and off when we are home.
- Alert sent to phone when motion is detected.

Temperature automations are:

- Turning on bedroom fan.
