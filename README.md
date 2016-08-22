# comm-setup
How to set up reasonably secure communications with friends and family.

<center>
![Use Signal. Use Tor](https://pbs.twimg.com/media/CqF-yfCXgAAL91i.jpg:large)

*Image credit [@xor](https://twitter.com/xor)*
</center>

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">.<a href="https://twitter.com/Snowden">@snowden</a> OPSEC guide:<br>- use Signal<br>- use Tor<br>- use full disk encryption<br>- use a password manager<br>- use two factor auth<br><br>Solid basics.</p>&mdash; the grugq (@thegrugq) <a href="https://twitter.com/thegrugq/status/668767879299399682">November 23, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

This guide assumes you have an Android type device and a laptop. You *should* encrypt your device, get a password manager (stop reusing passwords for goodness sakes!), and use Tor. This guide will run you through putting Tor onto your device, and getting secure communications setup for your friends/family/coworkers/anyone else.

## [Ricochet](https://www.ricochet.im/)

Ricochet is an instant messenger for the desktop that is simple and easy to use. If I have a laptop open, this is my go to messenger with family. Currently, it only supports text, but it gives the best security and usuability. 

![Ricochet Screenshot](ricochetscreen.png)

> Ricochet is a different approach to instant messaging that **doesn't trust anyone** in protecting your privacy.

> * *Eliminate metadata*. Nobody knows who you are, who you talk to, or what you say.
> * *Stay anonymous*. Share what you want, without sharing your identity and location.
> * *Nobody in the middle*. There are no servers to monitor, censor, or hack.
> * *Safe by default*. Security isn't secure until it's automatic and easy to use.

It uses the [Tor network](https://www.torproject.org/) in order to anonymize you. What's the Tor network? Watch the [Tor Project Animation](https://www.youtube.com/watch?v=JWII85UlzKw). A quick explanation is that Tor hides your location from people watching your connection (NSA and Facebook alike) and thus it *can* make you anonymous.

Ricochet and Conversations both utilize the Tor network to keep you safer.

### How to set it up

If you're on GNU/Linux running Debian Stretch or higher, simply <code>sudo apt-get install ricochet-im</code>

All other systems go to the ricochet.im main page and select your operating system [here](https://www.ricochet.im/)

Set it up with someone else and add them as a contact.


## [Conversations](https://conversations.im/)

An amazing messenger for Android. This is the primary messenger my family uses to stay in touch. You'll need [Orbot](https://guardianproject.info/apps/orbot/) which is Tor for Android. I recommend using [F-droid's](https://f-droid.org/) repository to download Orbot and Conversations. F-droid is a 3rd party app store that contains all free software (free as in free beer and free as in freedom).

![Conversations screenshot](https://conversations.im/images/screenshot_encryption_selection.jpg)

Conversations is:

> A free and open source Jabber/XMPP client for Android. Easy to use, reliable, battery friendly. With built-in support for images, group chats and e2e encryption.

> Design principles
* Be as beautiful and easy to use as possible without sacrificing security or privacy
* Rely on existing, well established protocols
* Do not require a Google Account or specifically Google Cloud Messaging (GCM)
* Require as little permissions as possible

> Features
* End-to-end encryption with either OMEMO, OTR or OpenPGP
* Sending and receiving images
* Intuitive UI that follows Android Design guidelines
* Pictures / Avatars for your Contacts
* Syncs with desktop client
* Conferences (with support for bookmarks)
* Address book integration
* Multiple Accounts / unified inbox
* Very low impact on battery life

Conversations has OMEMO, a fork of the Signal protocol

> OMEMO gives you all the advantages you would expect from a modern-day encryption protocol like Future and Forward Secrecy and deniability while allowing you to keep the benefits of message synchronization and offline delivery. OMEMO not only gives you a better encryption features than OpenPGP and OTR but is also much easier to setup. OMEMO is the encryption you can actually use in your daily life. Turn it on once and forget you ever did.

*And*, it supports the Tor network.

### How to set it up

1. Install F-droid
2. Add the Guardian Projects repository to F-droid and refresh
3. Install Orbot
4. Install Conversations
5. Open conversations and tap "create account"
6. Pick a username
7. on the add account screen, go to the upper right menu, click settings
8. In the settings menu, go all the way down to expert settings, and select "connect via tor", 
9. Go back and finish the registration process

## [Signal](https://whispersystems.org/)

Signal is an app that sends secure messages to others who also have the app and can replace your default SMS app. It also supports secure phone calling.

![Signal Screenshot](https://whispersystems.org/assets/header/signal-header-3928749d381ba96d54fc66a0673114c2.jpg)

> Privacy is possible, Signal makes it easy.

> Using Signal, you can communicate instantly while avoiding SMS fees, create groups so that you can chat in real time with all your friends at once, and share media or attachments all with complete privacy. The server never has access to any of your communication and never stores any of your data.

> * Say Anything. Signal uses an advanced end to end encryption protocol that provides privacy for every message every time.
* Open Source. Signal is Free and Open Source, enabling anyone to verify its security by auditing the code. Signal is the only private messenger that uses open source peer-reviewed cryptographic protocols to keep your messages safe.
* Be Yourself - Signal uses your existing phone number and address book. There are no separate logins, usernames, passwords, or PINs to manage or lose.
* Group Chat. Signal allows you to create encrypted groups so you can have private conversations with all your friends at once. Not only are the messages encrypted, but the Signal server never has access to any group metadata such as the membership list, group title, or group icon.
* Fast. The Signal protocol is designed to operate in the most constrained environment possible. Using Signal, messages are instantly delivered to friends.
* Speak Freely - Make crystal-clear phone calls to people who live across town, or across the ocean, with no long-distance charges.

### How to set it up

1. Go to the Google Play Store and install Signal
2. Register with a phone number
3. Sync with your current contacts
4. Set it as your default SMS app
5. Lock down the app with a passcode

## [Ring](https://ring.cx/)

A video chat messenger that has desktop and mobile support. Use this in place of skype. It's peer-to-peer and encrypted by default.

![ring screenshot](https://ring.cx/sites/ring.cx/files/styles/desktop_big/public/screens/sfl_ring_captureecrandesktop-en-elcapitan_0.jpg?itok=8hsFx5Su)

> Ring is a free software for communication that allows its users to make audio or video calls, in pairs or groups, and to send messages, safely and freely, in confidence.

### How to set it up

If you're on GNU/Linux running Debian Stretch or higher, simply <code>sudo apt-get install ring</code>

All other systems, go [here](https://ring.cx/en/download) to download Ring for your system.

You can use Ring on your Android to video chat privately.


## [Syncthing](https://syncthing.net/)

Syncs files between devices. Use it to share files with family and to backup files from your phone to your desktop.

![Syncthing screenshot](https://syncthing.net/images/screenshot-720.jpg)

> Syncthing replaces proprietary sync and cloud services with something open, trustworthy and decentralized. Your data is your data alone and you deserve to choose where it is stored, if it is shared with some third party and how it's transmitted over the Internet.

### How to set it up

If you're on GNU/Linux running Debian Stretch or higher, simply <code>sudo apt-get install syncthing</code>

All other systems, go [here](https://syncthing.net/) to download Syncthing for your system.

You can setup Syncthing on your Android to easily sync the photos you take to any other system you have Syncthing installed on.

## Next Steps

Although you have secure ways to communicate, you also need to secure your endpoints. 

> "Encryption works. Properly implemented strong crypto systems are one of the few things that you can rely on. Unfortunately, endpoint security is so terrifically weak that NSA can frequently find ways around it." --Edward Snowden

Even if you're not worried about the NSA, endpoint security is the weakest link. You need to encrypt your device, switch to a privacy respecting email, use a password manager, turn on 2-factor-authentication, use the tor browser, and ensure Firefox is set up to preserve your privacy.

# Device encryption

You should encrypt your device.

<!--### Change your email provider-->

<!--### Password manager-->

<!--### Turn on 2FA-->

<!--### Tor Browser-->

<!--### Useful Browser Exentions for Firefox-->

<!--### Don't trust other peoples devices-->

<!--you can keep a copy of Tails on a USB connected to your keys if you want-->

## Caveats

This setup is conditional upon being moderately secure. If your life is at risk *please* use something like Tails. Note that smartphones are tracking devices. If you need higher security and don't want a vist to somewhere to be on a permanent record, **leave your phone on and at home**. NSA et al. look for interesting patterns, so its best to leave your phone on and somewhere where you would normally reside.

Furthermore, the security patching for Android is a mess. If you want a mobile OS that has better security support, use CopperheadOS. CopperheadOS currently has no support for Google Play Store, so you won't be able to use Signal. You could use Silence.im, or Conversations.im instead. It also only supports the Nexus series. 

> A hardened open-source operating system based on Android with PaX, OpenBSD malloc and many other privacy/security features.

> "Copperhead is probably the most exciting thing happening in the world of Android security today." --Chris Soghoian, principal technologist with the Speech, Privacy, and Technology Project at the American Civil Liberties Union



---

<p xmlns:dct="http://purl.org/dc/terms/">
  <a rel="license"
     href="http://creativecommons.org/publicdomain/zero/1.0/">
    <img src="http://i.creativecommons.org/p/zero/1.0/88x31.png" style="border-style: none;" alt="CC0" />
  </a>
  <br />
  To the extent possible under law,
  <span rel="dct:publisher" resource="[_:publisher]">the person who associated CC0</span>
  with this work has waived all copyright and related or neighboring
  rights to this work.
</p>
