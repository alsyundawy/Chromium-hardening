# Overview

Chrome (Chromium based Browsers) have a lot of anti-fingerprinting tricks integrated which are not visible via flags. The benefit compared using some extensions is that those flags are more reliable because an extension could fail to load, stopped working etc. and then you're exposed/fingerprintable.

Reducing the network traffic overall helps to keep the fingerprint possabilities lower. 

## Working with hidden flags

* `--disable-reading-from-canvas` block Canvas fingerprinting
* `--disable-3d-apis` # blocks WebGL fingerprinting

These mentioned flags are not needed in e.g. ungoogled-Chromium, Brave or Chromium!


## Always launch Google Chrome in "Guest Browsing Mode"

* Add to Chrome.exe `--guest`. ("right-click" - "properties" - "shortcut" - "target" and then simply add --guest)

## Search engine

I suggest Startpage (sorry I'm biased) but personally I have very good experience with Startpage. The default engine is set to Chrome but you can change it with this example

* `https://startpage.com/?kae=t&kp=-2&kav=1&q=%s"`


## Multicast

This is often called as "background spying" but it's an service which allows you to stream your content to other devices. This is also implemented in other Browsers like Mozilla Firefox. In case you monitor the traffic you'll see ssdp and mdns based connections.

* IGMP: 224.0.0.0/24
* 1900 & 5353 are the ports

Multicast can not fully be disabled (not even with the flags), that's simply a part on how the Browser works, however blocking the mentioned ports/protocols helps to get rid of those connections but you will lose the "streaming ability" (not only under Chrome).

## IPv6

IPv6 (by default) will be used as fallback in case IPv4 is not reachable. 

## "Calling home" (1e100.net)

1e100.net is used by Chrome on a regular basis, the domains "rotating". However the original origin of these Google domains are the following domains:

* accounts.google.com
* clients2.google.com
* clients4.google.com
* chrome.google.com
* csp.withgoogle.com
* gvt1.com
* redirector.gvt1.com
* gstatic.com
* update.googleapis.com

Once you blocked them you will see no 1e100.netbased connections anymore, but you will also break several Google functions (login etc.) & domains which you might want to use. There are no "hidden" connections, however there is no flag related solution here, you can block the domains or use alternative Browsers like Chromium/Brave or ungoogled-Chromium if you never use features like Google login.
