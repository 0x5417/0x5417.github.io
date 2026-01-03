+++
title = "Digital Estate"
date = 2026-01-02
draft = false
+++

## Introduction
Recently, I read a book about `trust administration` and `will probate` which are ways to choose what happens to your [***:sparkle:stuff:sparkle:***](https://www.youtube.com/watch?v=xBGH_--x4Ng) when you die.
One interesting thing mentioned in the book, is a person's `digital estate`. A digital estate includes everything a person has online.
This encompasses all digital records, photos, online accounts, and more.
Because the law is slow to change relative to the progress made by technology, court orders are often required to get a family access to their decedant's digital assets (if not handled properly).
This got me thinking about how online digital life is organized and how to make the most badass and functional digital estate possible.

## Requirements for a Strong Digital Estate

### Organization
A digital estate should be organized such that it can encapsulate all uses of technology in an individual's life.
This means, it should consider how a person uses each of their `devices`, which `services` they use on each, `how they interact`, and more.
It should allow for each individual device to have complete access to the services it needs and exclude everything else (single responsibility).

### Ease of Use
A person should be able to easily access all of their digital information immediately when they need it without having to jump through any hoops.
Once configured, a digital estate should `manage itself` and be `extensible` for when new assets need to be stored.

### Security
A digital estate will likely be required to manage serveral online accounts.
With modern security measures, account management becomes more than just remembering a username and password and sharing it between sites.
Online services will have obscure `password` requirements, `two factor (2fa)` requirements, `email confirmation` requirements and in the future, possibly physical `security key` requirements as well.

### Privacy
Similar to how the dealings of a physical estate are not open to the public eye, the `operations` of a digital estate should `remain private` as well.
In the digital world, you can't put a "no trespassing" (example shown below) sign on your accounts, and any actions of a similar fashion will likely have the opposite result resulting in spam, unwanted ads, harassment, or any other unfavorable uses of technology.

![Comedic No Trespassing Image](/img/no-trespassing.png "No Trespassing")

### Brief Summary
So a good digital estate must be `usable`, `extensible`, `secure`, `private` and `organized`. Let's build it. 

## Building a Digital Estate
I will assume the reader has some existing online presence in the form of accounts, storage, personalities, banking and more.
Erasing data online is a difficult task so requesting for it to be deleted and simply not using any old accounts is the best bet moving forward.

### Requirements

I assume the reader would like to use their devices as follows:
```
Phone: Personal messaging, online banking, navigation, listening to music.
Laptop: Browsing the internet, shopping, reading mail, programming, work related instant messaging, more.
Home Server: Host movies, game servers, media and music.
Public Server: Host a blog or another personal website/service for friends and family.
```

How these devices work together:
```
The phone must share images, videos and files with the laptop and vice versa.
The laptop must be able to access both the home server and public server from any network.
The public server and home server should not communicate.
```

### Necessary Technologies

#### KeePassXC/DX
KeePass is a free and open source `password manager` which allows users to create hierarchical password entries in a `secure database file`.
These entries are not limited to passwords however and can contain many other types of information.
KeePass can also handle `OTP two factor` authentication as part of an entry in a database.

#### Syncthing
Syncthing is a free and open source program which allows devices to `securely share files`.
Devices must both add eachother in order to become connected.

#### Tailscale
Tailscale is a `free VPN software` which allows your devices to `connect securely` to eachother.
It runs on top of the popular wireguard protocol and can allow cross-subnet communication between your devices.
It runs using tailscale's central routing servers but can be replaced with a selfhosted `headscale` for full sovereignty. 
The client is completely open sourced whereas the server code is not.

#### Mail Service
Hosting a mail service is not worth the hassle for the average internet user so using a publicly avaiable option is a must.
I have been using `proton mail` which claims to be privacy focused but many features are locked behind a `paywall` which is something to consider.

### Tying It Together

1. Make a KeePass database which follows this generic heirarchical structure and adapt it to your needs:
* Root (Manages other emails)
  * Banking (Financial Services)
  * Entertainment (Spotify, Netflix, ...)
  * Shopping (Amazon, Target, Kroger, ...)
  * Social Media (Instagram, X, ...)
  * Public Contact (Allows random people to contact you)
  * Private Contact (Allows employers to contact you)
2. Connect the laptop and phone with Syncthing and share this KeePass database between them.
3. Add the laptop, home server, and public server to a tailscale tailnet and configure the firewall rules as desired.
4. Sit back, light a fuckin ciggie, and celebrate the start of a new organized digital life.

### How This Solves Every Problem Mentioned Before
You have now created a secure, extensible system for storing your digital assets which can be accessed from multiple devices seamlessly.
You can access all the services you want on the devices you want. Your devices can securely communicate with eachother.
You also will not recieve ~~any~~ ***much*** spam in places you don't want it and can create simple filters to isolate each task you want to complete.

### Further Expansion and Ideas
* Advanced email forwarding & filtering
* Detect which services sell your data to advertisers
* Mess around with hardware security keys and fit them into this
* Explore similar alternative services and new technologies

## Conclusion
Digital life will only get more complex as time goes on, requiring the use of new services and technology.
It's important to adapt to changes and make the best of these new situations as they arrive.
There will likely be a time in the near future that this setup won't be enough, but for now, I am content with it.
