+++
title = "Media Setup"
date = 2026-01-03
draft = false
+++

## Introduction
I recently got pretty pissed off at my TV.
Network television gives such a limited selection of what to watch and has infomercials every few minutes.
Streaming services aren't much better and if you get the cheaper versions, you're still watching ads on a limited selection of media.
I hated paying for multiple streaming services and having to ***STILL*** watch ads.
I thought to myself about how fucking retarded this was and cooked up a bit of a solution.


I wanted to be able to watch `any media` `for free`, `without ads`, `on a TV`.

## The Play
### Getting Free Media
My friends put me on [`free media heck yeah (FMHY)`](https://fmhy.net).
This allows you to [**:pirate_flag:PIRATE:pirate_flag:**](https://www.youtube.com/watch?v=FDF4Tj8JPc0) all the media you could ever want ... for free ... without ads.


At this point you have a choice:
![Comedic image of morpheus offering red and blue pills.](/img/morpheus.png "Morpheus Decision Meme")

The choice is yours, and I know which one I am picking.

### TV Setup
The only thing missing at this point is to get it set up with the same TV experience you get anywhere else.
My solution was to use a `raspberry pi 4b` and a `wireless keyboard and mouse (KB&M) combo`.

Parts I used to build this divine setup:
* Raspberry Pi 4b - $70
  * HDMI cable
  * USB-C charging cable
  * Micro SD card
* Logitech K400 Plus Wireless Touch Keyboard - $30
* Old Samsung TV
* Power strip with switch

Steps for setup:
1. Install raspberry pi OS on the SD card and insert it into the raspberry pi.
2. Connect the PI HDMI output to your TV (HDMI handles sound too).
3. Plug in the USB for the wireless KB&M combo into the raspberry pi.
4. Power the TV and the raspberry pi from the power strip.
5. Hide all of your cables behind the TV so it looks incredibly clean.
6. Access the PI's web browser and start watching your free media.

Troubleshooting:
* If sound doesn't work on the TV, edit the sound output on the raspberry pi to go through HDMI.
* You can use the TV volume and control the volume through the KB&M unit.


### Result
Finally, after you have done everything, you should be left with an upgraded setup like the following:

Front view:
![Front view of TV setup](/img/front-tv.jpg "Front View")
Side view:
![Side view of TV setup](/img/side-tv.jpg "Side View")

## Expansion Ideas
* Access other services like Youtube with an ad blocker or a custom client.
* Torrent whatever you want to watch and host it on your homelab.
  * Have the raspberry pi access the media from there.

## Conclusion
Streaming services and network TV are a pain in the ass and I am always looking for ways to save a quick buck whenever I can.
With a bit of technical knowledge, you can get a better media experience for free or very cheap depending on the hardware you already have.

