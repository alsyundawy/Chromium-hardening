### Warning
**You shouldn't use flags to configure Chrome because they're not supported. Instead, configure Chrome for your [enterprise or organization using policies](https://support.google.com/chrome/a/answer/9037717) (chrome://policy).** The original page was [removed](https://www.chromium.org/administrators/policy-list-3/atomic/_groups).  - Statement is from a Google Marketing Manager (_not my own!_).


### Flags (depending which OS/Chrome version)
* Chrome 78: 282
* Chrome 77: 302
* Chrome 76: 307
* Chrome 75: 311
* Chrome 74: 316


### Security (only) flags (enabled)
* #enable-sync-uss-nigori (only if your use Browser sync!)
* (_optional_) #password-leak-detection (or use HaveIBeenPwned website/extension via KeePass, enabling this option will cause more traffic due to password checks (if some are stored in the database)
* #extension-content-verification
* #disallow-doc-written-script-loads
* #enable-appcontainer
* #enforce-tls13-downgrade (known root only)
* #enable-gpu-appcontainer
* #disallow-unsafe-http-downloads
* #ignore-gpu-denylist (disabled) (outdated)
* #pdf-isolation (will be removed and is only relevant in case you read PDF's via Browser)
* #edge-strict-origin-isolation (replaces app container lockdown)
* #block-unsafe-downloads-over-insecure-connections
* #edge-limit-media-autoplay (will be removed, edge onlxy)
* Microsoft Edge tracking prevention (_optional_ - MS Edge + Defender only [via Chrome 75+ with Ent. GPO policy])
* #enable-webrtc-srtp-aes-gcm (if WebRTC is supported/enabled)
* #treat-unsafe-downloads-as-active-content
* #enable-tls13-early-data (disabled, GET fingerprinting)
* `--enable-quic` & `--quic-version=h3-23` as command line argument to [enable HTTP/3](https://blog.cloudflare.com/http3-the-past-present-and-future/) See here how to run [Chrome with flags](https://www.chromium.org/developers/how-tos/run-chromium-with-flags).


### Privacy (only) flags (enabled)
* #device-discovery-notifications
* #prefetch-privacy-changes
* #enable-sharing-device-registration
* #sharing-use-device-info
* #enable-removing-all-third-party-cookies
* #enterprise-reporting-in-browser (disabled)
* #autofill-prune-suggestions (if autofill was enabled)
* #turn-off-streaming-media-caching
* #improved-cookie-controls
* #enable-webrtc-hide-local-ips-with-mdns
* #dns-over-https
* #disable-hyperlink-auditing (outdated)
* ~~Enable search suggestions on the local NTP (disable) (outdated)~~
* #reduced-referrer-granuarity
* Anonymize local IPs exposed by WebRTC (outdated)
* #search-results-extensions-block-v2 (Opera only)
* #unified-consent
* Top Sites from Site Engagement (disable) (outdated)
* New history entries require a user gesture (outdated)
* #enable-history-manipulation-intervention
* Disable minimum for server-side tile suggestions on NTP (disable) (outdated)
* #enable-webrtc-remote-event-log (_optional_) (if WebRTC is allowed/enabled)
* #pdf-form-save (disabled)
* #cookies-without-same-site-must-be-secure + #same-site-by-default-cookies (both must be enabled, might break websites!)
* #enable-data-reduction-proxy-with-network-service (connect to Google - disabled)
* #happiness-tracking-surveys-for-desktop (disabled)
* #use-sync-sandbox (connect to Google)
* #load-media-router-component-extension (WARNING: Don't touch it (breaks the "Cast" feature _optional_ to avoid Google startup connections/loopback)
* #enable-webvr (prevent possible WebVR API based fingerprinting methods)
* #enable-generic-sensor (disabled, fingerprinting)
* #omnibox-experimental-keyword-mode (disable)
* #omnibox-suggestion-transparency-options
* #omnibox-drive-suggestions (disable)
* #enable-speculative-service-worker-start-on-query-input (disabled + performance/fingerprinting reasons)
* #use-new-accept-language-header (disabled)
* #data-saver-server-previews (disabled)
* #tab-hover-cards (disabled)
* #enable-filesystem-in-incognito
* #passwords-account-storage (disabled) (use KeePass instead and disable all "Gaia account features")


## Performance (only) flags (enabled)
* #animated-avatar-button (disabled)
* #enable-gpu-rasterization
* #enable-lazy-image-loading
* #enable-lazy-frame-loading
* #enable-parallel-downloading
* ~~Enable doodles on the local NTP (disable)~~ (outdated)
* ~~Enable search suggestions on the local NTP (disable)~~ (outdated)
* #enable-layout-ng
* #d3d11-video-decoder


## Advertising (only) flags (enabled)
* ~~App Banners (disabled)~~ (outdated)
* ~~Autoplay policy (document user activation required)~~ (outdated)
* ~~Enable promos on the local NTP (disabled)~~ (outdated)
* ~~User Activation V2 (disabled)~~ (outdated)
* #happiness-tracking-surveys-for-desktop-demo (disabled)


### Enabled

Feature | Comment/setting
------------ | -------------
[#use-angle](chrome://flags/#use-angle) | D3D11on12 **Recommend !*
[#automatic-tab-discarding](chrome://flags/#automatic-tab-discarding) | //
[#autoplay-policy](chrome://flags/#autoplay-policy) | Document user activation is required.
[#clipboard-content-setting](chrome://flags/#clipboard-content-setting) | //
[#cookies-without-same-site-must-be-secure](chrome://flags/#cookies-without-same-site-must-be-secure) | **Recommend !** See [here](https://scotthelme.co.uk/csrf-is-really-dead/)
[#chrome-colors](chrome://flags/#chrome-colors) | //
[#chrome-custom-color-picker](chrome://flags/#chrome-colors-custom-color-picker) | //
[#disable-javascript-harmony-shipping](chrome://flags/#disable-javascript-harmony-shipping) | (Enabled (Default)
[#disallow-unsafe-http-downloads](chrome://flags/#disallow-unsafe-http-downloads) | **Recommend !**
[#dns-over-https](chrome://flags/#dns-over-https) | **Recommend !**
[#disallow-doc-written-script-loads](chrome://flags/#disallow-doc-written-script-loads) | **Recommend !**
[#drag-to-pin-tabs](chrome://flags/#drag-to-pin-tabs]) | _optional_
[#enable-appcontainer](chrome://flags/#enable-appcontainer) | [**Recommend !**](https://blog.chromium.org/2019/09/experimenting-with-same-provider-dns.html)
[#ForcedColors](chrome://flags/#ForcedColors) | _usability_ (_[optional](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Accessibility/HighContrast/explainer.md)!_)
[#enable-autofill-credit-card-ablation-experiment](chrome://flags/#enable-autofill-credit-card-ablation-experiment) | //
[#enable-block-tab-unders](chrome://flags/#enable-block-tab-unders) | //
[#enable-brotli](chrome://flags/#enable-brotli) | //
[#enable-experimental-fling-animation](chrome://flags/#enable-experimental-fling-animation) | //
[#reduced-referrer-granuarity](chrome://flags/#reduced-referrer-granuarity) | **Recommend !**
[#enable-framebusting-needs-sameorigin-or-usergesture](chrome://flags/#enable-framebusting-needs-sameorigin-or-usergesture) | //
[#enable-future-v8-vm-features](chrome://flags/#enable-future-v8-vm-features) | //
[#enable-gpu-appcontainer](chrome://flags/#enable-gpu-appcontainer) | **Recommend !**
[#enable-pixel-canvas-recording](chrome://flags/#enable-pixel-canvas-recording) | **Recommend !**
[#enable-history-entry-requires-user-gesture](chrome://flags/#enable-history-entry-requires-user-gesture) | //
[#enable-history-manipulation-intervention](chrome://flags/#enable-history-manipulation-intervention) | //
[#enable-mark-http-as](chrome://flags/#enable-mark-http-as) | Mark as actively dangerous
[#enable-message-center-new-style-notification](chrome://flags/#enable-message-center-new-style-notification) | //
[#enable-native-notifications](chrome://flags/#enable-native-notifications) | //
[#enable-origin-trials](chrome://flags/#enable-origin-trials) | //
[#enable-parallel-downloading](chrome://flags/#enable-parallel-downloading) | //
[#enable-picture-in-picture](chrome://flags/#enable-picture-in-picture) | //
[#enable-quic](chrome://flags/#enable-quic) | Controversial, I **recommend enabling it**
[#enable-reader-mode](chrome://flags/#enable-reader-mode) | _optional_
[#enable-webrtc-h264-with-openh264-ffmpeg](chrome://flags/#enable-webrtc-h264-with-openh264-ffmpeg) | //
[#enable-webrtc-hide-local-ips-with-mdns](chrome://flags/#enable-webrtc-hide-local-ips-with-mdns) | **Recommend !**
[#enable-webrtc-new-encode-cpu-load-estimator](chrome://flags/#enable-webrtc-new-encode-cpu-load-estimator) | //
[enforce-tls13-downgrade](chrome://flags/#enforce-tls13-downgrade) | Enabled (Known root only) **Recommend !**
[#expensive-background-timer-throttling](chrome://flags/#expensive-background-timer-throttling) | //
[#extension-content-verification](chrome://flags/#extension-content-verification) | Enforce strict (hard fail) - **Recommend !**
[#gdi-text-printing](chrome://flags/#gdi-text-printing) | //
[#isolate-origins](chrome://flags/#isolate-origins) | **Recommend !**, [see here why](https://wicg.github.io/isolation/)
[#ignore-gpu-denylist](chrome://flags/#ignore-gpu-denylist) | **Recommend !** (disabled)
[#ntp-customization-menu-v2](chrome://flags/#ntp-customization-menu-v2) | //
[#pdf-isolation](chrome://flags/#pdf-isolation) | **Recommend !**
[#smooth-scrolling](chrome://flags/#smooth-scrolling) | //
[#tab-groups](chrome://flags/#tab-groups) | v75+ _optional_
[#tab-hover-cards](chrome://flags/#tab-hover-cards) | _optional_
[#tab-hover-card-images](chrome://flags/#tab-hover-card-images) | _optional_
[#unified-consent](chrome://flags/#unified-consent) | //
[#overlay-scrollbars](chrome://flags/#overlay-scrollbars) | **Recommend !**
[#overlay-scrollbars-flash-after-scroll-update](chrome://flags/#overlay-scrollbars-flash-after-scroll-update) | **Recommend !**
[#overlay-scrollbars-flash-when-mouse-enter](chrome://flags/#overlay-scrollbars-flash-when-mouse-enter) | **Recommend !**
[new-tab-button-position](chrome://flags/#new-tab-button-positio) | **Recommend !** (_optional_)


### Disabled

Feature | Comment or setting
------------ | -------------
[#account-consistency](chrome://flags/#account-consistency) | //
[#allow-previews](chrome://flags/#allow-previews) | //
[#allow-sxg-certs-without-extension](chrome://flags/#allow-sxg-certs-without-extension) | //
[#data-saver-server-previews](chrome://flags/#data-saver-server-previews) | //
[#device-discovery-notifications](chrome://flags/#device-discovery-notifications) | //
[#enable-autofill-credit-card-upload](chrome://flags/#enable-autofill-credit-card-upload) | //
[#enable-media-session-service](chrome://flags/#enable-media-session-service) | Volume OSD (optional)
[#enable-native-google-assistant](chrome://flags/#enable-native-google-assistant) | [//](https://www.howtogeek.com/429382/how-to-enable-google-assistant-on-your-chromebook/)
[#enable-client-lo-fi](chrome://flags/#enable-client-lo-fi) | //
[#enable-data-reduction-proxy-with-network-service](chrome://flags/#enable-data-reduction-proxy-with-network-service) | //
[#enable-generic-sensor-extra-classes](chrome://flags/#enable-generic-sensor-extra-classes) | //
[#enable-generic-sensor](chrome://flags/#enable-generic-sensor) | //
[#enable-lookalike-URL-navigation-suggestions](chrome://flags/#enable-lookalike-url-navigation-suggestions) | //
[#enable-noscript-previews](chrome://flags/#enable-noscript-previews) | //
[#enable-optimization-hints](chrome://flags/#enable-optimization-hints) | //
[#fill-on-account-select-http](chrome://flags/#fill-on-account-select-http) | //
[#fill-on-account-select](chrome://flags/#fill-on-account-select) | //
[#hardware-media-key-handling](chrome://flags/#hardware-media-key-handling) | Avoid media stats leakage
[#happiness-tracking-surveys-for-desktop](chrome://flags/#happiness-tracking-surveys-for-desktop) | //
[#network-service](chrome://flags/#network-service) | //
[#new-usb-backend](chrome://flags/#new-usb-backend) | //
[#new-tab-loading-animation](chrome://flags/#new-tab-loading-animation) | ([optional](https://old.reddit.com/r/chrome/comments/ahxx8c/new_tab_loading_animation/))
[#omnibox-ui-hide-steady-state-url-trivial-subdomains](chrome://flags/#omnibox-ui-hide-steady-state-url-trivial-subdomains) | hides www only
[##omnibox-ui-hide-steady-state-url-scheme](chrome://flags/#omnibox-ui-hide-steady-state-url-scheme) | hides https:// only
[#omnibox-ui-hide-steady-state-url-scheme-and-subdomains](chrome://flags/#omnibox-ui-hide-steady-state-url-scheme-and-subdomains) | //
[#omnibox-drive-suggestions](chrome://flags/#omnibox-drive-suggestions) | Workaround for a bug
[#omnibox-rich-entity-suggestion](chrome://flags/#omnibox-rich-entity-suggestion) | Since 74.0.3729.169 enabled
[#pdf-form-save](chrome://flags/#pdf-form-save) | //
[#reduced-referrer-granularity](chrome://flags/#reduced-referrer-granularity) | //
[#safe-search-url-reporting](chrome://flags/#safe-search-url-reporting) | //
[#show-autofill-type-predictions](chrome://flags/#show-autofill-type-predictions) | //
[#show-managed-ui](chrome://flags/#show-managed-ui) | //
[#tab-hover-cards](chrome://flags/#tab-hover-cards) | //
[#enable-javascript-harmony](chrome://flags/#enable-javascript-harmony) | //
[#web-contents-occlusion](chrome://flags/#web-contents-occlusion) | //
[#calculate-native-win-occlusion](chrome://flags/#calculate-native-win-occlusion) | //
[#enable-experimental-productivity-features](chrome://flags/#enable-experimental-productivity-features) | //
[#new-tabstrip-animation](chrome://flags/#new-tabstrip-animation) | //




### Android specific

Feature | Comment or setting
------------ | -------------
[#safe-browsing-telemetry-for-apk-downloads](chrome://flags/#safe-browsing-telemetry-for-apk-downloads) | Disabled
[#enable-android-night-mode](chrome://flags/#enable-android-night-mode) | Enabled (optional)
[#enable-android-spellchecker](chrome://flags/#enable-android-spellchecker) | Enabled
[#enable-site-isolation-for-password-sites](chrome://flags/#enable-site-isolation-for-password-sites) | Enabled (v74+)

### [Microsoft Edge (Chromium)](https://blogs.windows.com/windowsexperience/2019/11/04/introducing-the-new-microsoft-edge-and-bing/) specific [edge://flags]

Most Chromium based flags for Edge are explained over [here](https://github.com/MicrosoftEdge/MSEdgeExplainers). The project basically explains what each flag does (with Info, Screenshots & more).

Feature | Comment or setting
------------ | -------------
[#edge-ForcedColors](edge://flags/#ForcedColors) | Enabled (_usability_)
[#enable-aura-tooltips-on-windows](edge://flags/#enable-aura-tooltips-on-windows) | [Aura Dark Mode Tooltips](https://mspoweruser.com/microsofts-latest-flag-improves-dark-mode-implementation-on-chromium-based-edge/)
[#edge-cdm-override-service](edge://flags/#edge-cdm-override-service) | Enabled (Default)
[#edge-controls](edge://flags/#edge-controls) | Enabled (Default)
[#edge-cookie-import](edge://flags/#edge-cookie-import) | Disabled
[#edge-dns-over-https]((edge://dns-over-https) | **Recommend !**, see here [why](https://en.wikipedia.org/wiki/DNS_over_HTTPS)
[#edge-experimental-scrolling](edge://flags/#edge-experimental-scrolling) | Disabled
[#edge-follow-os-theme](edge://flags/#edge-follow-os-theme) | Enabled (Default)
[#edge-installation-of-extensions-from-microsoft-store](edge://flags/#edge-installation-of-extensions-from-microsoft-store) | Enabled (Default)
[#edge-strict-origin-isolation](edge://edge-strict-origin-isolation) | **Recommend !**
[#edge-playready-drm-win10](edge://flags/#edge-playready-drm-win10) | Disabled, will break Netflix!
[#edge-reading-view](edge://flags/#edge-reading-view) | Enabled (Default)
[#edge-sign-in-with-aad](edge://flags/#edge-sign-in-with-aad) | Disabled
[#edge-user-agent-spoofing-service](edge://flags/#edge-user-agent-spoofing-service) | Enabled
[#edge-widevine-drm](edge://flags/#edge-widevine-drm) | Disabled, will break Netflix!
[#edge-reading-view-grammar-tools](edge://flags/#edge-reading-view-grammar-tools) | Grammar Tools
[#enable-force-dark](edge://flags/#enable-force-dark) | Enforce use of "Dark Mode"
[#global-media-controls](edge://flags/#global-media-controls) | Enable media control buttons
[#edge-enable-shy-ui](edge://flags/#edge-enable-shy-ui) | Fullscreen Dropdown (_matter of taste_)


#### Other Edge "Tweaks"

* In order to **enable the new Extensions Menu**, create a shortcut or edit the existing shortcut `--enable-features=ExtensionsToolbarMenu` The example should then look like this: `msedge.exe --enable-features=ExtensionsToolbarMenu`.



### Some flags are (in general) problematic - do not touch! -

Some flags can cause "critical security holes" in your configuration even if you enable/disable them to prevent exactly this. The flags are been tested against [BrowserAudit](https://browseraudit.com/test), however keep in mind that the test page might not be 100% accurate!

Feature | Reason
------------ | -------------
[#allow-sxg-certs-without-extension](chrome://flags/#allow-sxg-certs-without-extension) | Triggers an critical error (DOM)
[#enable-signed-http-exchange](chrome://flags/#enable-signed-http-exchange) | Triggers an critical error (DOM)
[#focus-mode](chrome://flags/#focus-mode) | Leakage (?) unconfirmed, triggers warnings
[#enable-built-in-module-kv-storage](chrome://flags/#enable-built-in-module-kv-storage) | Leakage (?) unconfirmed, triggers warnings
[#enable-built-in-module-infra](chrome://flags/#enable-built-in-module-infra) | Possible attacks
[#disable-windows10-custom-titlebar](chrome://flags/#disable-windows10-custom-titlebar) | Only if you really need it




### Deprecated

Feature | Deprecated or removed since
------------ | -------------
#enable-appcontainer | v78
#PasswordExport | v77
#PasswordImport | v77
#disable-hyperlink-auditing | v73
#enable-autofill-credit-card-last-used-date-display | v76
#enable-autofill-credit-card-upload-send-detected-values | v75
#enable-av1-decoder | v74
#enable-desktop-ios-promotions | v74
#enable-fast-unload | v74
#enable-filesystem-in-icognito | v74
#enable-gamepad-extensions | v76
#enable-md-bookmarks | v74
#enable-modern-media-controls | v77
#enable-new-app-menu-icon | v74
#enable-new-preconnect | v75
#enable-new-print-preview | v76
#enable-nup-printing | v77
#enable-password-generation | v75
#enable-policy-tool | v76
#enable-push-api-background-mode | v77
#enable-simple-cache-backend | v69
#enable-single-click-autofill | v72
#enable-site-per-process | v70
#enable-site-settings | v77
#enable-tcp-fast-open | v76
#extensions-toolbar-menu | v76
#important-sites-in-cbd | v77
#new-audio-rendering-mixing-strategy | v78
#ntp-ui-md | v70
#secondary-ui-md | v71
#show-saved-copy | v71
#simplified-fullscreen-ui | v70
#simplified-fullscreen-ui | v71
#sound-content-setting | v70
#stop-in-background | v70
#voice-search-on-local-ntp | v70
#allow-running-insecure-content | [v81](https://security.googleblog.com/2019/10/no-more-mixed-messages-about-https_3.html)
##temporary-unexpire-flags-m76 | 80

### DNS-over-HTTPS
 
Starting with [Chrome 78](https://blog.chromium.org/2019/09/experimenting-with-same-provider-dns.html) the Browser will get an option to control DoH via `chrome://flags/#dns-over-https` (the flag can only be opt-out'ed [but is listed in my list as enabled [[default]]), however the option is experimental and only avbl. for several users/OS, the iOS and Linux implementation is still unfinished, that been said they won't get this right of the batch. 

Supported are the following providers (for now): Cleanbrowsing, Cloudflare, DNS.SB, Google, OpenDNS & Quad9. If a provider isn't in the integrated list then Chrome will automatically use a fallback and switch back to the "normal" mode.

Fo [force Chrome to use DoH](https://bugs.chromium.org/p/chromium/issues/detail?id=799753#c8) add the following shortcut path: 
* `--enable-features="dns-over-https<DoHTrial" --force-fieldtrials="DoHTrial/Group1" --force-fieldtrial-params="DoHTrial.Group1:server/https%3A%2F%2F1.1.1.1%2Fdns-query/method/POST` 

This example will configure Chrome to use Cloudflares DoH server. To test if DoH is working or not, check the [https://1.1.1.1/help](https://1.1.1.1/help) url. 


### Fooling the NTP to increase the Browser performance and to gain some (questionable) privacy benefit

There is some traffic caused for NTP lookups, this can be disabled with the following trick:
* Change your default search engine to "Startpage" and remove all other search engines in your lists.
* Enable or disable the following flags `Enable using the Google local NTP`, `Enable doodles on the local NTP` (disable), `Enable search suggestions on the local NTP` (disable), `Top Sites from Site Engagement` (disable), `Disable minimum for server-side tile suggestions on NTP` (disable) & `Enable promos on the local NTP` (disable).
