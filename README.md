### "Hardens" Chrome & Chromium based Browser and their settings in the name of privacy/security  

The goal of this project is to provide information (and _maybe_ an extension/policy) to setup Chromium/Chromium to get the best out-of-the-box application security & privacy.

[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/fold_left.svg?style=social&label=Follow%20%40CHEF-KOCH)](https://twitter.com/CKsTechNews)
[![Say Thanks!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://saythanks.io/to/CHEF-KOCH)
[![Discord](https://discordapp.com/api/guilds/418256415874875402/widget.png)](https://discord.me/CHEF-KOCH)

### Chromium vs. Mozilla Firefox Quantum (**still needs to be updated!**)


## Differences between Chrome & Chromium

Chromium was not made by Google, it's a web browser 'developed' (based on parts of the original source code from Chrome) by volunteers and released under FLOSS. There exist bunch of alternative forks of it with additional features in it.

Most core developers are Google employees, you can easily see this in their bug reports (eMail/name) etc, that they work for the Chromium project as 'volunteers' and release the source code but in reality they work for the mother Google, that said not all of them.

A fork means that Google takes the original source code of Chromium and they adding some bits of code and tools (like for example Flash Player (now removed), RLZ etc) Google Chrome itself is either open-source nor proprietary, it's freeware under [Google Chrome's Terms of Service](https://www.google.com/intl/en/chrome/browser/privacy/eula_text.html). Googles Privacy policy can be reviewed [here](https://policies.google.com/privacy?hl=en).


## Performance (Overall)

| Feature        | Chrome           | Firefox Quantum  | Description |
| ------------- |:-------------:| :-------------:| -------:|
| Startup Memory | Chromium consumes overall more memory than Firefox, but starts up faster - Chromes kernel requires more resources
| Multi-core system integration   | Chrome ones is older and more reliable because it's longer tested  |  Firefox isolation feature is (by default) limited | Both perform equal, depending on the used API |
| JavaScript performance | //  |  // | Equal? (depending) |
| _Synthetic Octane benchmark_ | 45169 Points | 43246 Points |
| ARES-6 Browser Benchmark | ~ 21 sec | ~ 50 sec | [Test link](https://browserbench.org/ARES-6/about.html) |
| WebXPRT Test | ~ 275 | ~ 300 | Several API tests |
| Basemark | ~ 1420 | ~ 810 Points | Lots of different tests (encryption etc) |


### Independent performance tests
* [A Quick Look At The Firefox 66.0 vs. Chrome 73.0 Performance Benchmarks (phoronix.com)](https://www.phoronix.com/scan.php?page=news_item&px=Firefox-66-Chrome-73-Benchmarks)
* [Firefox vs. Chrome Browser Performance On Intel Ice Lake + Power/Memory Usage Tests (phoronix.com)](https://www.phoronix.com/scan.php?page=article&item=firefox-chrome-icelake&num=7)


## Privacy & Security Scandals

Firefox
========

* [Firefox browser trusts DarkMatter CA certificate to cause security industry controversy](https://bugzilla.mozilla.org/show_bug.cgi?id=1427262) (see [here](https://www.reuters.com/investigates/special-report/usa-spying-raven/) how it could be abused) _However, this one is questionable and controversial because there is no audit or sign that this was abused_
* [Firefox Users Cry Foul Over 'Mr. Robot' Ad Installed As Research Program](http://fortune.com/2017/12/17/firefox-mr-robot-looking-glass/) [2017]
* [Firefox Shield Studies](https://wiki.mozilla.org/Firefox/Shield/Shield_Studies) - these studies are separate from the normal telemetry
* [Cliqz](https://gist.github.com/solso/423a1104a9e3c1e3b8d7c9ca14e885e5) acquired by Mozilla
* [Firefox tracks users with Google Analytics in the add-on settings](https://github.com/mozilla/addons-frontend/issues/2785) [2017]
* Most concerns can be destroyed using about:config.
* Firefox has forks in order to (by default) opt-out (without any need of altering about:config). E.g. Waterfox.
* [Mozilla responds to Booking.com Snippet Concerns; “It was not a paid placement or advertisement. We are continually looking for more ways to say thanks for using Firefox."](https://old.reddit.com/r/privacytoolsIO/comments/abfgj5/mozilla_responds_to_bookingcom_snippet_concerns/)


Isn't it funny that [Firefox Wikipedia page](https://gist.github.com/solso/423a1104a9e3c1e3b8d7c9ca14e885e5) has not any section related to Mr. Robot and safebrowsing privacy concerns while Chrome has this mentioned?! Remember Firefox (by default) has also in fact more studies and telemetry integrated in his browser! They even call telemetry in the article as [security](https://en.wikipedia.org/wiki/Firefox#Security) feature. Is this objective written - _I very much doubt it._


Chrome
========

* ZERO no additional studies or additional telemetry. The stuff which is send back is exactly the same like Mozilla does. Safebrowsing, Malware (Phishing filter updates etc).
* Google sells (officially) only ads.
* Most concerns can be destroyed using about:flags.
* Chrome has forks (Chromium) in order to (by default) opt-out (without any need of altering about:flags). E.g. Cent Browser.


## Features
* Chromium generally supports the latest HTML features sooner
* Firefox generally supports the latest Javascript features sooner
* Both have mobile versions
* Both manage bookmarks
* Both have a useful dashboard startpage
* Firefox is more extensible
* There are countless themes and extensions, and there's an advanced Customize mode to change the placement of anything on the screen.
* Firefox has an advanced user profile system that's easy to backup
* Both support syncing browser data and preferences between multiple installations, including on mobile
* Firefox allows non-tabbed mode, Chromium does not
* Firefox allows traditional style menus, Chromium does not
* Chrome was the first browser which by default introduced adblocking without any extension ([Android Chrome version got it first](https://www.ghacks.net/2017/07/31/google-launches-adblocker-in-chrome-dev-and-canary-for-android/))

## Extension coverage
* Some extensions like e.g. Ghostery lacks features compared to the Mozilla version
* Chromium has a Downloadbar and limited support for Greasemonkey, Tapermonkey Userscripts by default
* The Firefox extension API is far more powerful than Chromium's; every part of the browser can be customized
* Mozilla adopted WebExtension API which technically can run Chrome/Firefox extensions but it's messy (atm)
* Both extension/theme/plugin stores getting daily scans to avoid malware
* WebKit/WebExtension seems the today's default

## Data privacy with default settings
* Firefox uses Yahoo as its default search engine in North America, and other search engines in other regions
* Chromium uses 'Google' as its default search engine
* Firefox Sync can be hosted on your own server, and uses a zero-knowledge architecture. Chrome Sync only syncs to Google servers but's encrypted.
* Both support private sessions where there is no history saved (private/incognito modes)
* Chromium natively supports WebRTC, just like Edge and Firefox do as well. WebRTC basically can return your IP info if queried, but your browser's usual HTTP headers return IP info and a wealth of other metadata anyway. The potential privacy concern is WebRTC providing IP info if located behind e.g. a VPN or anonymous proxy, so if either apply, block the WebRTC query (among other things) with an extension. If neither apply, then it is pretty much no point of talking about security (no matter which browser).

## Data privacy after user configuration
* Both Firefox and Chromium extensions may send private/usage data to somewhere (with prior warning)
* You can change the default search engines of both to services like DuckDuckGo
* Users can easily disable features of Chromium that remotely use Google-services
* You can selectively enable Chromium's extensions for private sessions
* You can use NoScript in Firefox and µMatrix (formerly HTTP Switchboard) in Firefox and Chromium to greatly enhance your privacy
* Both support the HTTPS Everywhere extension from the Electronic Frontier Foundation
* Both can be configured to use TOR, but the TOR project recommends configuring Firefox or using the Firefox-based Tor browser
* Firefox allows extensive control over which elements of the browser run and transmit data. These can be changed in the about:config page
* Newer versions of Chromium require you download extensions from the Chrome web store or manually install from a local file
* None browser is perfect this is due -> we still using outdated protocols and usability


## Preferences file

See this [documentation](https://chromium.googlesource.com/chromium/src/+/master/docs/user_data_dir.md) for more details regarding to the default profiles.

Windows: C:\Users\<username>\AppData\Local\Google\Chrome\User Data\
MacOS X: ~/Library/Application Support/Google/Chrome/
Linux: ~/.config/google-chrome/


## Media Engagement Index (MEI) (Chrome 66+)

The MEI is determined by a ratio of visits to significant media playback events per origin, determined by these four factors:

* Consumption of the media (audio/video) must be greater than 7 seconds.
* Audio must be present and unmuted.
* Tab with video is active.
* Size of the video (in px) must be greater than 200×140.


## Chrome's integrated Ads-blocker

[Google](https://blog.chromium.org/2018/02/how-chromes-ad-filtering-works.html) is evaluating sites based on the [Better Ads standards](https://www.betterads.org/standards) and then rating them as a pass, warning, or failing. Site owners can access these evaluations using an API, and sites can be re-reviewed after bad ads have been addressed.


## Privacy Concerns

I'll explain in short the privacy concerns and if it's true or already outdated or already fixed.

<p align="center">
<img src="https://raw.githubusercontent.com/CHEF-KOCH/Chromium-hardening/master/Wikipedia/Privacy%20concerns.png">
</p>

The official Wikipedia privacy concerns (User tracking concerns) is outdated.

<p align="center">
<img src="https://raw.githubusercontent.com/CHEF-KOCH/Chromium-hardening/master/Wikipedia/Botnet.png">
</p>


| Privacy concern        | Explanation           |
| ------------- |:-------------:|
Chrome sends details about its users and their activities to Google through both optional and non-optional user tracking mechanisms. | Google already explained this right from the beginning since 2008 with a [Blog post](https://blog.chromium.org/2008/10/google-chrome-chromium-and-google.html). The privacy settings can also be manually controlled as explained over [here](https://support.google.com/chrome/answer/114836?visit_id=0-636611054822963698-3982001039&rd=1). This is in the meantime an common technique in all current Browser starting from Firefox over Opera and even Edge has some kind of safebrowsing mechanism, safebrowsing itself doesn't contain any personal information which can expose you or your browser habits. The only critical thing someone can find here is that these data are stored locally into your Browser Data folder. |
Every URL you even begin to type in the address bar is sent to Google, in whole or in fragments, for auto-completion purposes. | It's called Omnisearch and can be disabled since many years in Chrome via about:flags. [Google explained how you disable it](https://productforums.google.com/forum/#!topic/chrome/PLaFaRnd1Hw). The Google URL Search prediction (or link prefetching) can be disabled, after that and clearing the Browser Cache it will only show results based on your **Offline** Browser History.  |
Connects to Google every 30 minutes to download a list of malicious URLs, so the fact that you even have Chrome open is transmitted to Google. |  This is a protection mechanism in order to protect you from malware. You can disable it in the options since many years. |
Asks you to login to your Google account, so your browsing tabs, history, etc. is stored on Google servers. | Login is optional since forever and always will be. Every Browser nowadays have a login function. |
Connects to websites in the background before you are even finished typing them in, without your explicit instruction. | This is a prefetch option to predict stuff to load content more quickly. This doesn't expose you and is not relevant to any privacy aspect. If you don't like it disable it via about:flags. |
Contains an RLZ identifier, an encoded string sent together with all queries to Google. | RLZ source code was released exactly one week after it got integrated. RLZ will never be send when you install Chrome from official sources. It's however true that on Android it's more problematically but you can use a Chromium based Browser (fork) which doesn't include the RLZ source code. |
[clientID](http://blogoscoped.com/archive/2008-09-09-n68.html) | The clientID (unique one) was removed already since Aug. 2009 due privacy concerns but no one ever add any proof that this exposes you or fingerprint/track you. |
Page not found | This is not even a tracking method, it's a 404 which are displayed in order to inform the user that the URL/Domain is not reachable. You however can change this behavior with a cached version since Chrome 55. |
Google Update | This is also not a privacy concern, every Browser has an integrated update mechanism. Using the latest versions which contains security bug fixes is important and the opposite of an privacy concern. Since Android P Google even started to force OEMs to push more frequently security updates for normal users which should help to get less vulnerable. |
Other features like Do not Track & Co. | Can all be controlled (disabled/enabled) within settings. |


Privacy related issue tickets can be found [here](https://bugs.chromium.org/p/chromium/issues/list?q=component:Privacy).


**About Ungoogled-Chromium**


[Ungoogled-Chromium](https://github.com/Eloston/ungoogled-chromium) project has major weaknesses too so before you recommend this browser as _alternative_ think about the following:


```bash
Update as of September 2016:
I, Eloston, am in a period of time where I do not have as much time as I had before to work on this project...


~~~

Update 9/29:

Our favorite infosec expert (whom we’ve cited before on a few matters) SwiftOnSecurity, let us know today that Ungoogled Chromium is a student project and doesn’t have the ability to update itself (and likely hasn’t been updated.) In that regard, we can’t recommend it...

```

In other words it has [no auto-updater mechanism integrated](https://lifehacker.com/ungoogled-chromium-strips-away-the-privacy-invading-fea-1787139870), this is for advance users no problem they can use some tools/scripts or manually download and install it but the normal user will never do this. However, in the meantime some things has changed, it more often gets updates now which is a good sign but this is no guarantee for code quality which applies to every Browser or Fork. The release page by itself mostly only provides the source code until the project manager decide to release a new version which is then always behind other forks because it needs to be reviewed over a long(er) time period.


Using scripts and updater tools can be dangerous when they suddenly starting to download official Google builds, as shown [here](https://github.com/Eloston/ungoogled-chromium/issues/415) which the user is only aware of after everything happened. and Windows Users now need such an updater/downloader in order to get the binaries, read [here](https://github.com/henrypp/chrlauncher/issues/33#issuecomment-279736691) basically this means you must trust someone else because most users will blindly install it and not compile it themselves. I see this as very critical.


### Google's "spying code"

The following integrations are "controversial"

* [Anchor ping attribute](https://mytechdecisions.com/compliance/chrome-safari-and-opera-to-force-hyperlink-auditing/) - often called "Hyperlink auditing" or Hyperlink ping
* Features wich sends data back to google, such as [safe browsing](https://safebrowsing.google.com/) & spell check
* URL tracker ([chromium_src/chrome/browser/google/chrome_google_url_tracker_client_browsertest.cc](https://chromium.googlesource.com/chromium/src/+/66.0.3359.158/chrome/browser/google/chrome_google_url_tracker_client.h))
* [Background sync](https://developers.google.com/web/updates/2015/12/background-sync)
* [Battery API](https://www.chromestatus.com/feature/4537134732017664), [WebUSB API](https://developers.google.com/web/updates/2016/03/access-usb-devices-on-the-web), [WebBluetooth API](https://developers.google.com/web/updates/2015/07/interact-with-ble-devices-on-the-web)
* [Cloud Messaging](https://developers.google.com/cloud-messaging/chrome/client), [Firebase](http://firebase.googleblog.com/2013/03/power-your-chrome-extension-with.html), [Push Client](https://developers.google.com/web/ilt/pwa/introduction-to-push-notifications)
* [DNS prefetching](https://dev.chromium.org/developers/design-documents/dns-prefetching)
* [Domain reliability service](https://groups.google.com/a/chromium.org/forum/#!topic/chromium-dev/bIbPyQvXtpo)
* [Google GAIA Login](https://www.nytimes.com/2010/04/20/technology/20google.html)
* [Metrics reporting](https://www.stigviewer.com/stig/google_chrome_current_windows/2014-07-08/finding/V-44771)
* [Network Time Tracker](https://chrome.google.com/webstore/detail/webtime-tracker/ppaojnbmmaigjmlpjaldnkgnklhicppk)
* [RAPPORT](https://developers.google.com/web/tools/chrome-user-experience-report/)
* [Remote debugging](https://blog.chromium.org/2011/05/remote-debugging-with-chrome-developer.html)
* [Report Uploader](https://www.chromium.org/developers/crash-reports)
* [WebRTC log uploading service](https://webrtc.org/native-code/logging/) - `chrome://webrtc-logs`


**Conclusion**

Chrome is not more or less tracking anyone then all other Browsers on the market. Other Browsers in fact trying to imitate Chrome and his features such as [Chromecast](https://en.wikipedia.org/wiki/Chromecast) detection which is often misleading called as _background spying_ because it sends every X minutes requests in order to check if the service is available or not among other features such as [Captive portal](https://en.wikipedia.org/wiki/Captive_portal) checks.

Browser Forks mostly only removing integrated functions which is _maybe the best way_ to prevent from a privacy perspective additional damage. An global opt-out for certain integrated features is definitely the better method, you can read about how you do this (with examples) [here](https://github.com/CHEF-KOCH/Chromium-hardening/blob/master/Configure%20Google%20Chrome%20via%20Group%20Policies.md).



**Statement 2019**


I write this as neutral as possible based on the research I did over the couple years.

Okay now, in 2019 I checked the Wikipedia link again and compared it with the Firefox Wikipedia article. It is (still) beyond me why the Firefox article never got a "criticism" section like almost all other listed browsers on Wikipedia. Mozilla made several serious mistakes (same like Opera, Chrome, etc.) and all of the incidents are nothing but past. They got on both sides fixed - Mozilla responded and Google did the same. In fact Mozilla had more security & privacy incidents over the couple years (see research) which are not even mentioned on Wikipedia (Mr. Robot etc.). In my point of view Wikipedia has the responsible for an "objective" article and apparently there are huge interest to suppress Google (or to push Mozilla) with _facts_ which are years old (and outdated) or even wrong. I already debunked all myths above and now I'm going to mentioned the so called "spying" code, which is in fact documented since day one. Are they controversial? Sure, no doubt about it.


Assuming Google abuses these APIs is nothing but wrong since there is zero evidence. The only real evidence you can find is the [location story](https://www.theguardian.com/technology/2018/aug/14/how-to-turn-off-google-location-tracking) which also affected iOS, the problem here is that no one finally could say if it was a bug or on purpose. The [Google Play Services](https://www.apkmirror.com/apk/google-inc/google-play-services/) file is huge, commplex and controls several security and privacy related API's. The service also updates itself in the background and it's difficult to say if the location tracking was maybe only an incident or a result of an outdated APK file, the topic is complex and there are both sides (not only one).


The API's are designed ([and documented](https://developer.chrome.com/api_index)) in order to help developers & webmasters to improve/track their extensions/websites, nothing more and nothing less, the rest of the rumours are in 99% without any real evidence.



__Misunderstanding on purpose?__


Some people constantly "WANT Chrome to spy", there are developers which need/want those [mentioned API's](https://developer.chrome.com/apps/api_index) (see __Google's "spying code"__) and on one hand it makes sense to integrate them while other people might arguing that they don't need them or raising _their own_ privacy concerns. Keep in mind that the Browser itself contains not only the "Browser part" it also includes other projects to e.g. render PDF's & more. The question in my opinion isn’t whether someone is collecting data, it’s whether someone is able to, which means if you distrust corp. X you have to automatically distrust corp. Y too.




__Does Chrome spy?__


[NO](https://www.google.com/chrome/privacy/), from a developer perspective the Browser does not spy. As said above, the integrated APIs _could be abused_ but other Browser also including them (for example the [Battery API is also included in FF](https://developer.mozilla.org/en-US/docs/Web/API/Battery_Status_API) to name only one example which could be used against you to track you) and you might be able to disable them via settings/options or flags, sadly not all can be disabled or only with "huge" effort. This is more a general question what "the web" should allow and what not. However, there is no evidence of a "keylogger" or other stuff which people usually excusing Google.


In the last 6 years whenever I read something in the news about "Chrome spying" I saw zero, right zero (!) evidence for such claims. [I see clickbait articles](https://www.vice.com/en_us/article/wj7x9w/google-chrome-scans-files-on-your-windows-computer-chrome-cleanup-tool) (Chrome has more market shares than Firefox -> higher interests) with strange arguments, like that Chrome would collect all your files, this is incorrect, there was in this case an advance option to enable/disable it. So what, Firefox does the same to improve their products. There are many other examples like this. I think we can agree that every such controversial toggle should be opt-in my default and not opt-out but this is most likely not going to happen.



**Can security be archived without tracking?**

**I say no**, in fact I log everything whats going on on my PC, Router and my devices otherwise how could I ever know if I'm compromised or not? I guess that's why Google created the [dashboard](https://myaccount.google.com/intro/dashboard?hl=en) to review your options. Apparently, some people never heard of it or never reviewed their options, as a result we get a lot "why google tracked me" topics. It's a feature because your login is used for many websites and Google products. Or how else do you guarantee that no one broke into your account if you can't see when you where logged in the last time with which device?



__Does Google has an interest in collecting data?__

[YES](https://safety.google/privacy/data/), of course and that's what people complaining about, it's controversial. The real problem here is that people which want opt-in/opt-outs do not get everything what they want and this is maybe the biggest point you can find when it comes to the privacy discussion. This is basically the reason why forks exists, to address exactly this. The question we should ask is if a Browser should be allowed to collect any data (debug, tracking etc.) because we can assume that everything can be abused - this is the real question and not only affects Chrome. Browser development and [bug bounty](https://www.google.com/about/appsecurity/chrome-rewards/) programs are also not really cheap. and most people have no interest to search for holes in your program when there is no reward, because you basically "waste" your lifetime in order to improve the product. Open Source is not really an argument because open source is in general not meant to be a "money making machine", of course there might bbe some whiteheads but that's not the norm. Speaking of how they get money, mostly [ads](https://www.quora.com/How-does-using-a-web-browser-help-the-developers-of-the-browser-financially), [donations](https://www.investopedia.com/articles/investing/041315/how-mozilla-firefox-and-google-chrome-make-money.asp) or [search engine deals](https://www.computerworld.com/article/3240008/mozillas-record-2016-revenue-funded-its-firefox-quantum-browser.html). You see, you can't destroy the web and remove ads or search engines, at some point they all need mooney to survive, this is okay and not really an argumentation point.



__Real problems__

* Transparency
* Trust - it is not a renewable resource which affects all, Firefox, Opera, Google & others.
* [Cookies](https://blog.chromium.org/2019/05/improving-privacy-and-security-on-web.html) and its pervasive advertising network and partnerships
* Login? No one in the world, not Google or Mozilla forces you to login into the Browser to sync your stuff. You still can backup everything offline in every browser.
* Private modes are pointless, not Firefox nor Chrome providing a "maximum secure" Browser out of the box because this would destroy the web and break many many websites.
* Are ads etc bad? What about the people which actually need the clicks/ads to survive? Blogger etc.
* Google, Firefox made mistakes - _it's simply a learning process_, you never did any mistakes right?! The market is hard and you can't satisfy each an everyone.
* Every blogger or website can decide to use Google Analytics (Mozilla bzw uses Googletagmanager) or not. No one is forcing you to do that. [Brave uses rewards](https://brave.com/brave-rewards/) which is a cool and "fresh" idea.
* Misunderstanding from non-technical persons. Just because there is a background connection doesn't automatically mean something is "spying". There are legitimate things like [Chrome Cast support](https://support.google.com/chromecast/chromecast?hl=en) which are implemented in order to make your life easier. The criticism point here can only be that there should be an option to disable it.
* Ignorance, stupidity & laziness - That's why most of the mentioned stuff exist, people expect to get everything as easy as possible without thinking about the consequences. The browser is much more than a Browser, it's a PDF reader, media player and much more.
* Control, maybe the biggest point when it comes to Google & privacy. They are in a good position to [dictate the web](https://en.wikipedia.org/wiki/Criticism_of_Google) (_if you check the page Chrome is not mentioned with any word_) and this is dangerous.



__My personal note__

I think both browsers terrible failed, Firefox and Chrome. Both are trying to gain user trust by implementing more and more "privacy gimmicks" and the changes are slowly going "mainstream". However, I constantly ask myself why we need configuration tweaks, extensions X in order to gain the privacy which all of these Browser promising us. That said here is what ever Browser should integrate, adopt or change (_in my opinion_).

- Listen to your own community, this is maybe the biggest and most important point, the community always knows best because they are the ones which at the end using your product.
- If you're unsure, don't hesitate and ask. It's no shame to ask your community if you lost your way or if you want input on a good idea.
- Get rid of idiotic modes like incognito, or private modes. This is a terrible idea, if you promise a secure and private browser then you don't need it and implement it by default for everyone straight from the beginning.
- Several forks already started to implement ad-blocking, HTTPSE & other "gimmicks". Which are helpful when it comes to giving the user control (privacy) back. The correct way should be to get such developers on board and adopt these into the browser, so that everyone can get the same benefits.
- Find a balance! Ads are okay unless they are malware or annoying. I think most people would not enable ad-blockers for page x if they know the ads they seeing are not annoying, possible dangerous or can compromise your security somehow. There are pages which placing their ads so that they are not bothering you while you read or click on the website.
- Think about alternatives and out-of-the-box. Do you really need Google tracking on your website?! How about a donation system or merchandise. No ads, no ad-blocker or script-blocker needed! It's that easy!
- Be open! Don't integrate telemetry in daily builds! You have a dev/beta/canary/RC version? So why not implement it there?! Most people simply don't want and like telemetry on their daily browsing habits because it makes them feel like they are the product.
- Provide Installers/Options for "power-users". Every browser installer I've seen so far are stuck in the 90's. There is no setup which gives you the ability to use pre-made configurations/profiles or to remove/install feature X.
- None of the Browser was able to implement an simple extension to integrate Tor functionality. Maybe a hint...
- Privacy "blah", just do it! Don't promise. DO IT!
- Check the priorities and get a identity, don't change like a flag in the wind.
- Adopting features from other Browser is okay, but don't overdue it not every change Browser X does has to be copied, especially not if it#s bugged (__autoplay__ ... __hm__).


## Chrome Vs. MS Edge (Chromium)

MS did a good job with Edge, however the new Edge (Chromium based) seems even better compared to the original Chrome Browser. It adds a lot of "requested" features into it and some functions are quite unique. Privacy wise it's a step forward compared to Chrome. 

* MS Edge has, overall the better privacy & performance 
* MS Edge provides built in tracking protection like in Firefox has
* DRM (4K Netflix) works (compared to Firefox and Chrome) really good
* The advanced safe download protection (Windows Defender) function is unique compared to other Browsers (Google mentioned such a function will be introduced only for Enterprise users).
* MS Edge does not "care" about Google's Manifest which means ad-blocking will always be possible
* The sync between mobile option is not bad, compared to other solution, this one offers ad-blocking support (on Android).


## Acknowledgments and References
* [Baselines of Web Browsers](https://thesimplecomputer.info/baselines-web-browsers)
* [Browser Sec Whitepaper](https://github.com/cure53/browser-sec-whitepaper)
* [Cent Browser](https://www.centbrowser.com/)
* [Chrome Browser for enterprise](https://enterprise.google.com/chrome/chrome-browser/)
* [Chrome Profiles](https://support.google.com/chrome/answer/2364824)
* [Chrome Security FAQ](https://chromium.googlesource.com/chromium/src/+/lkcr/docs/security/faq.md)
* [Chrome Vs. Chromium](http://www.linuxinsider.com/story/79510.html)
* [Chrome removed the enable_webrtc=false flag (which means no more No-WebRTC builds)](https://chromium.googlesource.com/chromium/src/+/d98b020fe1f0cb85de21de5313261a66ad9c9fe4)
* [Chromium Updater Script by mkorthof](https://github.com/mkorthof/chrupd)
* [Chromium WPAD detection](https://sunweavers.net/blog/node/37)
* [Compile Chrome on Windows](https://github.com/henrypp/chromium)
* [Custom DNS names in Chromium](http://michaelkc.tumblr.com/post/98129633274/working-with-custom-dns-names-in-chromium)
* [DNS caches can be used as cross-domain persistent cookies](https://bugs.chromium.org/p/chromium/issues/detail?id=546733)
* [How Chromium works](https://medium.com/@aboodman/in-march-2011-i-drafted-an-article-explaining-how-the-team-responsible-for-google-chrome-ships-c479ba623a1b#.is7blrj34)
* [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/en-us/download/) + ([Source Code](https://github.com/MicrosoftEdge/MSEdge))
* [NoScript whitelist](https://github.com/CHEF-KOCH/NoScript-Whitelist)
* [Official Chromium Security tracker](https://bugs.chromium.org/p/chromium/issues/list?q=Type%3DBug-Security)
* [Official Google Chrome Group Policy Templates & Guidance](https://www.chromium.org/administrators/policy-templates)
* [Official System Hardening Guide](https://sites.google.com/a/chromium.org/dev/chromium-os/chromiumos-design-docs/system-hardening)
* [Opt-out/opt-in selective on every Google Service](https://takeout.google.com)
* [POTARC](https://github.com/CHEF-KOCH/Online-Privacy-Test-Resource-List)
* [Privacy disrespected (by default)](https://bugs.chromium.org/p/chromium/issues/detail?id=795526)
* [The Private Life of Chromium Browsers](https://thesimplecomputer.info/the-private-life-of-chromium-browsers)
* [The story of why Chrome and Firefox will soon block sites with certain SSL certificates](https://www.templarbit.com/blog/2018/09/07/the-story-of-why-chrome-and-firefox-will-soon-block-sites-with-certain-ssl-certificates/)
* [Transitioning from SPDY to HTTP/2](https://blog.chromium.org/2016/02/transitioning-from-spdy-to-http2.html)
* [Why isn't passive browser fingerprinting (including passive cookies) in Chrome's threat model?](https://dev.chromium.org/Home/chromium-security/security-faq#TOC-Why-isn-t-passive-browser-fingerprinting-including-passive-cookies-in-Chrome-s-threat-model-) *[ref](https://dev.chromium.org/Home/chromium-security/client-identification-mechanisms)
* [https://bugs.chromium.org/p/chromium/issues/detail?id=795526](https://bugs.chromium.org/p/chromium/issues/detail?id=661792)
* ~~[BetterFirefox](https://github.com/CHEF-KOCH/BetterFirefox)~~


## External scripts, extension scanners or tools
* [PowerShell script to get the latest build of Chromium directly from the Chromium Project](https://github.com/RealDrGordonFreeman/Chromigen)
* [CRXcavator](https://crxcavator.io/) - Submit a Chrome Extension ID in order to inspect it


## Papers
* [Web Developer's Guide to Prerendering in Chrome](https://web.archive.org/web/20120309113126/http://code.google.com/chrome/whitepapers/prerender.html)
* [Google Chrome Privacy Whitepaper](https://www.google.com/chrome/privacy/whitepaper.html) **updated frequently by me & other people**


## Controversial Topics
* [Google promises Chrome changes after privacy complaints](https://www.cnet.com/news/google-promises-chrome-changes-after-privacy-complaints/)
* [Former Mozilla exec: Google has sabotaged Firefox for years](https://www.zdnet.com/article/former-mozilla-exec-google-has-sabotaged-firefox-for-years/)
* [How DRM has permitted Google to have an "open source" browser that is still under its exclusive control](https://boingboing.net/2019/05/29/hoarding-software-freedom.html)
* [Chrome to limit full ad blocking extensions to enterprise users](https://9to5google.com/2019/05/29/chrome-ad-blocking-enterprise-manifest-v3/)


## Microsoft Edge (Chromium)
* [Edge Privacy Concept](https://blogs.windows.com/msedgedev/2019/05/06/edge-chromium-build-2019-pwa-ie-mode-devtools/#H8GDbV0SOi7Am1AB.97)


## How to compile Chromium with Codes
* [GN build configuration](https://www.chromium.org/developers/gn-build-configuration) 
* [Chromium build with proprietary codecs by jedi4ever](https://gist.github.com/jedi4ever/d095656ae0f0eca4a83ebb2b331da367) 
