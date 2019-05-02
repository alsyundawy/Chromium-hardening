* `chrome://about`
* `chrome://accessibility`
* `chrome://appcache-internals`
* `chrome://apps`
* `chrome://blob-internals`
* `chrome://bluetooth-internals`
* `chrome://bookmarks`
* `chrome://cache`
* `chrome://chrome`
* `chrome://chrome-urls`
* `chrome://components`
* `chrome://conflicts`
* `chrome://crashes`
* `chrome://credits`
* `chrome://device-log`
* `chrome://devices`
* `chrome://dino`
* `chrome://discards`
* `chrome://dns`
* `chrome://downloads`
* `chrome://extensions`
* `chrome://flags`
* `chrome://flash`
* `chrome://gcm-internals`
* `chrome://gpu`
* `chrome://help`
* `chrome://histograms`
* `chrome://history`
* `chrome://indexeddb-internals`
* `chrome://inspect`
* `chrome://invalidations`
* `chrome://local-state`
* `chrome://media-engagement`
* `chrome://media-internals`
* `chrome://nacl`
* `chrome://net-export`
* `chrome://net-internals`
* `chrome://network-error`
* `chrome://network-errors`
* `chrome://newtab`
* `chrome://ntp-tiles-internals`
* `chrome://omnibox`
* `chrome://password-manager-internals`
* `chrome://policy`
* `chrome://predictors`
* `chrome://print`
* `chrome://profiler`
* `chrome://quota-internals`
* `chrome://safe-browsing`
* `chrome://serviceworker-internals`
* `chrome://settings`
* `chrome://signin-internals`
* `chrome://site-engagement`
* `chrome://suggestions`
* `chrome://supervised-user-internals`
* `chrome://sync-internals`
* `chrome://system`
* `chrome://taskscheduler-internals`
* `chrome://terms`
* `chrome://thumbnails`
* `chrome://tracing`
* `chrome://translate-internals`
* `chrome://usb-internals`
* `chrome://user-actions`
* `chrome://version`
* `chrome://webrtc-internals`
* `chrome://webrtc-logs`


Removed
* `chrome://view-http-cache` - ([since v66](https://chromium.googlesource.com/chromium/src.git/+/6ebc11f6f6d112e4cca5251d4c0203e18cd79adc))


### chrome://about
Lists all internal URLs maintained by Chrome/Chromium. It shows a overview of all the URLs which are supported by the installed Browser/Version, they can differ depending on which Chrome(ium) version you have installed and if the fork you use supports it or not (some forks disable/remove specific functions/flags/urls).

### chrome://accessibility
Displays information about [accessibility settings](https://support.google.com/chrome/answer/7040464?hl=en), whether it’s enabled or not for all open tabs. This feature let's impaired users access content on the web. Currently, the accessibility settings are turned off globally.

### chrome://appcache-internals
Shows the list of web apps which have [stored application cache](https://www.html5rocks.com/en/tutorials/appcache/beginner/) in Chrome/Chromium. It basically shows how many cache/space the application uses.

### chrome://apps
It lists all the pre-installed web apps including YouTube, Google Docs, etc. If you install a new Chrome app, it will show up here. It shows user installed apps and pre-installed ones (if any exist).

### chrome://blob-internals
Provides information about Binary Large Objects (blobs). Blobs are essentially large object data which are used to store images and videos.

### chrome://bluetooth-internals
It displays whether the PC has Bluetooth functionality and other related information. It also shows Bluetooth devices which are connected to the PC.

### chrome://bookmarks
It's an internal URL to open the Bookmark manager. You can use the URL or open it via three-dor menu, it's the exactly the same function.

### chrome://chrome
Opens the Chrome Settings page where you can customize all kinds of user settings.

### chrome://chrome-urls
Lists all the internal Chrome URLs just like `chrome://about`.

### chrome://components
Lists all {Chrome/Chromium Components which are required to function properly](https://www.thewindowsclub.com/google-chrome-components-page). Widevine availability, Adobe Flash Player support, Chrome Recovery, etc. 

### chrome://conflicts
Captures conflicts between Chrome/Chromium and PC and [maintains a log for further analysis](https://www.howtogeek.com/135300/how-to-troubleshoot-google-chrome-crashes/).

### chrome://crashes
Keeps a log of Chrome/Chromium [crashes](https://chromecrashes.com/) that recently happened. The crash reports are automatically sent to Google so that they can debug the issues.

### chrome://credits
Lists all the organisation and developers who have worked on Google Chrome/Chromium/Forks with their license and homepage link.

### chrome://device-log
Records all the [events that took place on your PC](https://support.google.com/chrome/a/answer/3293821?hl=en) like power, USB, Bluetooth, Network, etc.

### chrome://devices
Lists compatible devices which are connected to your PC.

### chrome://discards
Provides [information about all the open tabs and whether they have been discarded from memory](https://developers.google.com/web/updates/2015/09/tab-discarding).

### chrome://download-internals
Allows you to monitor downloads and the current status of every external third-party content.

### chrome://downloads
Shows Chrome's/Chromium's internal download manager.

### chrome://extensions
Displays all the [Chrome extensions](https://chrome.google.com/webstore) installed on your Google Chrome browser.

### chrome://flags
Lists all the experimental/stable features of Chrome/Chromium.

### chrome://gcm-internals
Provides information about [Google Cloud Messaging](https://developers.chrome.com/extensions/gcm) which is used by third-party developers to send push notifications.

### chrome://gpu
Shows information about various websites if they took advantage of [hardware acceleration](http://www.webupd8.org/2014/01/enable-hardware-acceleration-in-chrome.html).

### chrome://help
Opens the [“About Chrome”](https://support.google.com/chrome/?hl=en#topic=7438008) page where you can check for Chrome updates.

### chrome://histograms
Shows [histograms of various service handlers](https://chromium.googlesource.com/chromium/src.git/+/HEAD/tools/metrics/histograms/README.md) as to how much time it took to render data.

### chrome://history
Provides information about your browsing history from all the devices where you use Chrome/Chromium.

### chrome://indexeddb-internals
Lists all the websites which have created a local database to store various information and blobs. These databases are actually app data and it’s encrypted so that no malware can access it.

### chrome://inspect
See [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/) for more informations. There are different sections like Devices, Extensions, Pages, Apps, etc with an option to inspect each one of them.

### chrome://interstitials
Lists all the response pages of Chrome’s security. The information page is displayed when a user tries to access a harmful website inadvertently.

### chrome://interventions-internals
It displays few internal flags, quality of the network, logs of intervention and blocklist status.

### chrome://invalidations
provides debug [information about various service handlers so that developers can fix the issues](https://cloud.google.com/cdn/docs/cache-invalidation-overview).

### chrome://local-state
Basically adebug page which lists all the local information tied to Google Chrome. The debug information is parsed in a programming language so that developers can [easily go through the code](https://chromium.googlesource.com/chromium/src/+/lkgr/docs/user_data_dir.md).

### chrome://media-engagement
Lists all the websites which have played [media in the background](https://developers.google.com/web/updates/2017/09/autoplay-policy-changes).

### chrome://media-internals
[Lists all the media devices](https://www.chromium.org/audio-video/media-internals) like an audio speaker, webcam, etc available on your PC. 

### chrome://nacl
Displays information about the operating system, Chrome’s version and support for Portable Native Client. The Portable [NaCl lets developers test their apps and website](https://developer.chrome.com/native-client/nacl-and-pnacl).

### chrome://net-export
It lets developers [export log of Chrome’s network activity](https://dev.chromium.org/for-testers/providing-network-details).

### chrome://net-internals
[Various network settings like DNS, Proxy, Sockets and Domain Security Policy](https://www.smartfile.com/blog/using-chromes-net-internals-chromenet-internals/).

### chrome://network-error
Displays the [response page](https://www.chromestatus.com/feature/5391249376804864) of Chrome/Chromium when the URL is not found or invalid.

### chrome://network-errors
Lists all the response pages when [network errors occur while browsing the web](9https://support.google.com/chrome/answer/2898334?hl=en). 

### chrome://newtab
Opens a fresh new tab, similar to CTRL+T shortcut method just with a URL.

### chrome://ntp-tiles-internals
Lists all the top websites which are displayed on the homepage with their URL and favicon address. You can [add or remove top websites with your custom address as well](https://www.androidpolice.com/2017/01/16/psa-chrome-dev-allows-modify-recommended-sites-articles-sort/).

### chrome://omnibox
Debug [Omnibox](https://developer.chrome.com/omnibox) functionality with various tools.

### chrome://password-manager-internals
Allows you to captures and displays logs of the [internal password manager](https://www.theverge.com/2018/9/4/17818714/google-chrome-password-manager-security) in Chrome/Chromium. Password manager has become a standard feature of Chrome so having a log of events can help developers fix the bugs.

### chrome://policy
Displays all the [user and security policies](https://support.google.com/chrome/a/answer/9024365?hl=en) running on Chrome.

### chrome://predictors
[Lists all the probable key strings](http://googlesystem.blogspot.com/2013/11/chromes-predictors-page.html) which can be used to predict websites.

### chrome://print
Opens the default Print setting where you can customize the page layout and other relevant options.

### chrome://process-internals
Lists all the websites and extensions running in Chrome with their frame information. It’s very similar to [Task Manager’s process tab](https://www.lifewire.com/google-chrome-task-manager-4103619). 

### chrome://quota-internals
Displays the storage available on your system and also lists all the websites which have stored local data on your PC. The summary of data usage can be exported as XML language (.xml) file.

### chrome://safe-browsing
Read here for an [detailed explanation](https://safebrowsing.google.com/).

### chrome://serviceworker-internals
[Lists all the websites which have stored javascript on Chrome](https://www.chromium.org/blink/serviceworker/service-worker-faq).

### chrome://settings
You can create a bookmark which lets you easily access the Chrome settings with just a click.

### chrome://signin-internals
Displays [sign-in information of all the accounts signed into Chrome/Chromium](https://www.chromium.org/developers/about-signin-internals). You will be able to see all the essential data points like token ID, authorization flag, timestamp, and cookie information.

### chrome://site-engagement
[Lists all the websites you have had most engagement with](https://www.chromium.org/developers/design-documents/site-engagement).

### chrome://suggestions
Gives you suggestions about Chrome. It basically shows you the suggestion which you got from the address bar among URL suggestions. 

### chrome://supervised-user-internals
Provides information about the user, whether the user is adult, if supervision is required and so on. The [URL is deprecated](https://www.androidpolice.com/2018/07/22/chrome-will-officially-shut-supervised-users-feature-october-2018/). 

### chrome://sync-internals
Provides [several options to customize sync intervals for various service handlers](https://www.chromium.org/developers/sync-diagnostics).

### chrome://system
It displays information about the system, the OS version, keyboard layout, and installed extensions.

### chrome://terms
Displays [Google Chrome’s Terms and Conditions](https://www.google.com/chrome/privacy/eula_text.html).

### chrome://tracing
Let developers test their web pages and apps with various internal Chrome tools. There are several testing options like latency, UI rendering, javascript loading time, etc. If browsing history is enabled, you will be abble to records your browsing history.

### chrome://translate-internals
Provides information about user’s default language, translation preference and supported languages.

### chrome://usb-internals
Displays [compatible USB devices connected to the PC](https://groups.google.com/a/chromium.org/forum/#!topic/chromium-reviews/9uz3U0mB-4Y). You can even add a USB device with the serial number and verify your account.

### chrome://user-actions
Keeps a [log of every user action like switching tabs, opening bookmarks, closing tabs, etc with a timestamp](https://myactivity.google.com/myactivity).

### chrome://version
Provides detailed information about [Chrome’s version](https://en.wikipedia.org/wiki/Google_Chrome_version_history) including build number, user agent, Flash support, rendering engine, etc.

### chrome://webrtc-internals
Allows you to capture audio streams or event data to analyze possible audio related issues. It can help developers who are trying to build apps and websites based on [real-time communication (RTC) technology](https://webrtchacks.com/webrtc-externals/).

### chrome://webrtc-logs
Displays the event logs captured during real-time communication so that developers can e.g. [debug WebRTC events](https://webrtc.org/native-code/logging/).


See all URL parameters and details within the source code:
* https://cs.chromium.org/#chromium/src/chrome/common/url_constants.cc
* http://src.chromium.org/svn/trunk/src/chrome/common/url_constants.cc
