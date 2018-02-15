# Comm-setup
How to set up reasonably secure communications with friends and family

This guide assumes you have an Android type device and a laptop.

# Use privacy friendly messengers

## [Ricochet](https://www.ricochet.im/) [Desktop]

Ricochet is an instant messenger for the desktop that is simple and easy to use. If I have a laptop open, this is my go to messenger with family. Currently, it only supports text, but it gives the best security and usuability. 

![Ricochet Screenshot](https://raw.githubusercontent.com/gnujedi/comm-setup/master/ricochetscreen.png)

> Ricochet is a different approach to instant messaging that **doesn't trust anyone** in protecting your privacy.

> * *Eliminate metadata*. Nobody knows who you are, who you talk to, or what you say.
> * *Stay anonymous*. Share what you want, without sharing your identity and location.
> * *Nobody in the middle*. There are no servers to monitor, censor, or hack.
> * *Safe by default*. Security isn't secure until it's automatic and easy to use.

It uses the [Tor network](https://www.torproject.org/) in order to anonymize you. What's the Tor network? Watch the [Tor Project Animation](https://www.youtube.com/watch?v=JWII85UlzKw). A quick explanation is that Tor hides your location from people watching your connection (NSA and Facebook alike) and thus it *can* make you anonymous.

Ricochet and Conversations both utilize the Tor network to keep you safer.

#### How to set it up

If you're on GNU/Linux running Debian Stretch or higher, simply <code>sudo apt-get install ricochet-im</code>

All other systems go to the ricochet.im main page and select your operating system [here](https://www.ricochet.im/)

Set it up with someone else and add them as a contact.


## [Conversations](https://conversations.im/) [Mobile/Desktop(with Gajim)]

An amazing messenger for Android. This is the primary messenger my family uses to stay in touch. I recommend using [F-droid's](https://f-droid.org/) repository to download Conversations. F-droid is a 3rd party app store that contains all free software (free as in free beer and free as in freedom).

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

1. Install [F-droid](https://f-droid.org)
2. Install Conversations
3. Open conversations and tap "create account"
4. Pick a username

If want to use the Tor network, install orbot from F-droid and enable it under advanced settings in the conversations app.



## [Riot](https://riot.im) [Mobile/Desktop/Web]

Easy video, voice, and group collaboration. Sign up on their website, or download the app through F-droid. Be sure to enable e2e after creating a group.

![Riot screenshot](https://lh3.googleusercontent.com/12Tp_H5PssJjR6vB5kCH5Iw-Z4eG8m_ZkSF239HU-5miIkjei57Pym19ObNCmiFCf18=h900-rw)


## [Syncthing](https://syncthing.net/) [Mobile/Desktop]

Syncs files between devices. Use it to share files with family and to backup files from your phone to your desktop.

![Syncthing screenshot](https://syncthing.net/images/screenshot-720.jpg)

> Syncthing replaces proprietary sync and cloud services with something open, trustworthy and decentralized. Your data is your data alone and you deserve to choose where it is stored, if it is shared with some third party and how it's transmitted over the Internet.

### How to set it up

If you're on GNU/Linux running Debian Stretch or higher, simply <code>sudo apt-get install syncthing</code>

All other systems, go [here](https://syncthing.net/) to download Syncthing for your system.

You can setup Syncthing on your Android to easily sync the photos you take to any other system you have Syncthing installed on.

# Next Steps

Although you have secure ways to communicate, you also need to secure your endpoints. 

> "Encryption works. Properly implemented strong crypto systems are one of the few things that you can rely on. Unfortunately, endpoint security is so terrifically weak that NSA can frequently find ways around it." --Edward Snowden

Even if you're not worried about the NSA, endpoint security is *still* the weakest link. You need to encrypt your device, switch to a privacy respecting email, use a password manager, turn on 2-factor-authentication, use the tor browser, and ensure Firefox is set up to preserve your privacy.

## Device encryption

You should encrypt your device. It is simple to do on Android. Go into security settings and select "encrypt device".

![encrypt android](http://www.howtogeek.com/wp-content/uploads/2016/03/324x576xScreenshot_2016-03-29-12-18-12-576x1024.png.pagespeed.gp+jp+jw+pj+js+rj+rp+rw+ri+cp+md.ic.zqMUFynwnC.png)


## Get a password manager (stop reusing passwords for goodness sakes!)

I recommend [password-store](https://www.passwordstore.org/), a cross-platform and simple manager that encrypts your passwords with a PGP key. It can generate passwords for you, or you can insert your own. On Debian GNU/Linux, the prefered operating mode is to use it in terminal. Once you set it up, all you do is call <code>pass</code> and something like the following example appears:

```

zx2c4@laptop ~ $ pass
Password Store
├── Business
│   ├── some-silly-business-site.com
│   └── another-business-site.net
├── Email
│   ├── donenfeld.com
│   └── zx2c4.com
└── France
    ├── bank
    ├── freebox
    └── mobilephone

```

You can organize the password files anyway you like, placing different password files into more nested folders or whatever! There are versions for Linux, Windows, MacOS, Android, iOS, and an assortment of GUI tools. See the [password-store](https://www.passwordstore.org/) page for more information.

Here is password store on Android:

![passwordstoreandroid](https://lh5.ggpht.com/OeDm8iY4qn5XjbhHgMoGjFgjG27Be3VqpEb0ifTwqyYfVMs1iv7IKCXK0OjFfjFBiQ=h900)

## Turn on 2-factor-authentication

Download FreeOTP onto your device from the Fdroid repository, and set it up with your accounts. This protects your accounts by authenticating a second way. 2FA is highly recommended.

![FreeOTP](https://lh4.ggpht.com/mCBlwc-kwUaIQZXJUjLNorwWUhJN37ib_D6iik54cHP3l__YCE65FKSPKioAT-0ljsjn=h900)


## Tor Browser

You should be using the Tor browser as your main browser when you aren't logging into services that know you. For instance if you are reading the news, window shopping, youtube watching, or looking things up, you should fire up your Tor browser. [Download the Tor Browser for your platform](https://www.torproject.org/download/download.html.en).

## Useful Browser Extensions
You should be using Firefox as your main browser for sites where you log in (school, work, github, bank, etc.). You should install the following extensions in order to make your browsing safer:

* [HTTPS-Everywhere](https://www.eff.org/HTTPS-everywhere) to force HTTPS connections whenever possible
* [Privacy Badger](https://www.eff.org/privacybadger) to combat tracking
* [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) to block ads

You should also go into the privacy settings of firefox, find the history section, select "custom settings for history" and select "clear history when firefox closes." You may also want to disable Pocket, location sharing, and the remembering passwords feature.



## Don't trust other peoples devices

You really have no idea what kind of spyware/malware craziness other systems have on them. Don't trust other peoples devices. If you need to use someone else's computer, you can use a live operating system that lives on a USB drive. I recommend that you install [Tails](https://tails.boum.org/) (the amenisic incognito live system) onto a USB drive and keep it on your keychain/with you somehow. You can set it up to securely store your passphrase database, GPG key, email login and some files. This way, if your computer crashes or you need to use someone else's computer, you always have a way to access your email, passphrases, and a few files. Tails is great because it uses Tor by default and contains other security tools. Tails is based off of Debian GNU/Linux.

Enable a guest WiFi account to protect your internal network from guest devices. This keeps your personal devices isolated. It also is an important social aspect to have an openwireless access point as Bruce Schneier points out:

> Whenever I talk or write about my own security setup, the one thing that surprises people -- and attracts the most criticism -- is the fact that I run an open wireless network at home. There's no password. There's no encryption. Anyone with wireless capability who can see my network can use it to access the internet.

> To me, it's basic politeness. Providing internet access to guests is kind of like providing heat and electricity, or a hot cup of tea.

Running an openwireless access point *can* open you to risks if done improperly. Please make sure to run the guest network through a VPN or Tor. This makes it so that whatever guests do on the network, it is done in an anonymized way. You can also bandwith restrict the guest network in order for your private network to have priority.

## Change your email provider

Recommended email providers:

* [Openmailbox](https://www.openmailbox.org/) (free)
* [Posteo](https://posteo.de/en) (~$15/year)
* [Mailbox](https://mailbox.org/) (~$15/year)
* [Protonmail](https://protonmail.com/) (free, upgraded account ~$50/year)


Switching to a new email can be a hassle, but it is worth the effort to get a unique domain name and to protect your privacy. Most often you can get your first name and last name as the email address. This makes your email more professional and memorable. You can use [DAVdroid](https://davdroid.bitfire.at/) to sync your contacts and calendar to your mobile.

# Caveats

This setup is conditional upon being moderately secure. If your life is at risk *please* use something like Tails. Note that smartphones are tracking devices. If you need higher security and don't want a vist to somewhere to be on a permanent record, **leave your phone on and at home**. NSA et al. look for interesting patterns, so its best to leave your phone on and somewhere where you would normally reside.

Furthermore, the security patching for Android is a mess. If you want a mobile OS that has better security support, use CopperheadOS. 

> A hardened open-source operating system based on Android with PaX, OpenBSD malloc and many other privacy/security features.

> "Copperhead is probably the most exciting thing happening in the world of Android security today." --Chris Soghoian, principal technologist with the Speech, Privacy, and Technology Project at the American Civil Liberties Union

CopperheadOS currently has no support (and none planned) for Google Play Store, and only supports the Nexus series. They use the FDroid repository for adding applications.

You really shouldn't be using Microsoft Windows or Apple MacOS. These operating systems do not respect your privacy. Use a GNU/Linux distribution like Debian instead.


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
