# Comm-setup
How to set up reasonably secure communications with friends and family

These are my recommendations. Use what works for you.

<hr>



## Signal

> [Signal](https://signal.org/) is an encrypted instant messaging and voice calling application for Android and iOS. It uses the Internet to send one-to-one and group messages, which can include images and video messages, and make one-to-one voice calls. Signal uses standard cellular mobile numbers as identifiers and end-to-end encryption to secure all communications to other Signal users.

Easiest to get people set up on and is on all the major platforms. Video and audio calling. Perfect for group chat with friends and/or family. I would recommend this first---it's super easy to use and on Android it can be the default SMS app. The amount of metadata they can give away is [*very* little](https://signal.org/bigbrother).

<hr>

## Conversations

> [Conversations](https://conversations.im) is a Jabber/XMPP client for Android 4.0+ smartphones that has been optimized to provide a unique mobile experience.

Go to XMPP messenger. Provides a way to connect to people in a more traditional IM way. It uses the OMEMO protocol to encrypt messages (based on the Signal protocol) and has lots of cool features.

<hr>

## Riot

[Riot](https://riot.im) is a matrix client that allows collaboration across a wide variety of other apps and services (ie Slack). Video and audio chat/conference is supported.


An anecdote [from another Reddit user](https://www.reddit.com/r/privacytoolsIO/comments/6k447r/anyone_uses_riotim/djji0fc/) that I like:

>> Is it a good alternative to Signal or Wire?

> It's more of a Discord alternative

>>Does it work well?

> Yes , in my experience it's very stable


<hr>

## Ricochet

> [Ricochet](https://ricochet.im) uses the Tor network to reach your contacts without relying on messaging servers. It creates a hidden service, which is used to rendezvous with your contacts without revealing your location or IP address.

Desktop text chatting. 

<hr>


## Syncthing

> [Syncthing](https://syncthing.net) replaces proprietary sync and cloud services with something open, trustworthy and decentralized. 

To keep projects in sync, libraries of files that can change up-to-date, or just as a Dropbox replacement.

<hr>

## Onionshare

> [OnionShare](https://onionshare.org) is an open source tool that lets you securely and anonymously share a file of any size.

Sharing files with people when Syncthing would be overkill or annoying to setup.

<hr>

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

Download andOTP onto your device from the Fdroid repository, and set it up with your accounts. This protects your accounts by authenticating a second way. 2FA is highly recommended.

## Tor Browser

You should be using the Tor browser as your main browser when you aren't logging into services that know you. For instance if you are reading the news, window shopping, youtube watching, or looking things up, you should fire up your Tor browser. [Download the Tor Browser for your platform](https://www.torproject.org/download/download.html.en).

## Useful Browser Extensions
You should be using Firefox as your main browser for sites where you log in (school, work, github, bank, etc.). You should install the following extensions in order to make your browsing safer:

- Privacy Badger for blocking general tracking
- Ublock Origin for blocking ads
- Cookie AutoDelete for managing cookies
- HTTPS Everywhere for forcing TLS connections
- Decentraleyes

You should also go into the privacy settings of firefox, find the history section, select "custom settings for history" and select "clear history when firefox closes." You may also want to disable Pocket, location sharing, and the remembering passwords feature.



## Don't trust other peoples devices

You really have no idea what kind of spyware/malware craziness other systems have on them. Don't trust other peoples devices. If you need to use someone else's computer, you can use a live operating system that lives on a USB drive. I recommend that you install [Tails](https://tails.boum.org/) (the amenisic incognito live system) onto a USB drive and keep it on your keychain/with you somehow. You can set it up to securely store your passphrase database, GPG key, email login and some files. This way, if your computer crashes or you need to use someone else's computer, you always have a way to access your email, passphrases, and a few files. Tails is great because it uses Tor by default and contains other security tools. Tails is based off of Debian GNU/Linux.

Enable a guest WiFi account to protect your internal network from guest devices. This keeps your personal devices isolated. It also is an important social aspect to have an openwireless access point as Bruce Schneier points out:

> Whenever I talk or write about my own security setup, the one thing that surprises people -- and attracts the most criticism -- is the fact that I run an open wireless network at home. There's no password. There's no encryption. Anyone with wireless capability who can see my network can use it to access the internet.

> To me, it's basic politeness. Providing internet access to guests is kind of like providing heat and electricity, or a hot cup of tea.

Running an openwireless access point *can* open you to risks if done improperly. Please make sure to run the guest network through a VPN or Tor. This makes it so that whatever guests do on the network, it is done in an anonymized way. You can also bandwith restrict the guest network in order for your private network to have priority.

## Change your email provider

Recommended email providers:

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
