### Warning
**You shouldn't use flags to configure Chrome because they're not supported. Instead, configure Chrome for your [enterprise or organization using policies](https://support.google.com/chrome/a/answer/9037717) (chrome://policy).** The original page was [removed](https://www.chromium.org/administrators/policy-list-3/atomic/_groups). 

### Flags (depending which OS/Chrome version)
* Chrome 76: 307
* Chrome 77: 302

### Enabled

Feature | Comment or setting
------------ | -------------
[#automatic-tab-discarding](chrome://flags/#automatic-tab-discarding) | //
[#autoplay-policy](chrome://flags/#autoplay-policy) | Document user activation is required.
[#clipboard-content-setting](chrome://flags/#clipboard-content-setting) | //
[#cookies-without-same-site-must-be-secure](chrome://flags/#cookies-without-same-site-must-be-secure) | **Recommend !** See [here](https://scotthelme.co.uk/csrf-is-really-dead/)
[#disable-javascript-harmony-shipping](chrome://flags/#disable-javascript-harmony-shipping) | (Enabled (Default)
[#disallow-unsafe-http-downloads](chrome://flags/#disallow-unsafe-http-downloads) | **Recommend !**
[#dns-over-https](chrome://flags/#dns-over-https) | **Recommend !**
[#disallow-doc-written-script-loads](chrome://flags/#disallow-doc-written-script-loads) | //
[#drag-to-pin-tabs](chrome://flags/#drag-to-pin-tabs]) | _optional_
[#enable-appcontainer](chrome://flags/#enable-appcontainer) | [**Recommend !**](https://blog.chromium.org/2019/09/experimenting-with-same-provider-dns.html)
[#enable-autofill-credit-card-ablation-experiment](chrome://flags/#enable-autofill-credit-card-ablation-experiment) | //
[#enable-block-tab-unders](chrome://flags/#enable-block-tab-unders) | //
[#enable-brotli](chrome://flags/#enable-brotli) | //
[#enable-framebusting-needs-sameorigin-or-usergesture](chrome://flags/#enable-framebusting-needs-sameorigin-or-usergesture) | //
[#enable-future-v8-vm-features](chrome://flags/#enable-future-v8-vm-features) | //
[#enable-gpu-appcontainer](chrome://flags/#enable-gpu-appcontainer) | **Recommend !**
[#enable-history-entry-requires-user-gesture](chrome://flags/#enable-history-entry-requires-user-gesture) | //
[#enable-history-manipulation-intervention](chrome://flags/#enable-history-manipulation-intervention) | //
[#enable-mark-http-as](chrome://flags/#enable-mark-http-as) | Mark as actively dangerous
[#enable-message-center-new-style-notification](chrome://flags/#enable-message-center-new-style-notification) | //
[#enable-native-notifications](chrome://flags/#enable-native-notifications) | //
[#enable-origin-trials](chrome://flags/#enable-origin-trials) | //
[#enable-parallel-downloading](chrome://flags/#enable-parallel-downloading) | //
[#enable-picture-in-picture](chrome://flags/#enable-picture-in-picture) | //
[#enable-quic](chrome://flags/#enable-quic) | Controversial
[#enable-reader-mode](chrome://flags/#enable-reader-mode) | _optional_
[#enable-webrtc-h264-with-openh264-ffmpeg](chrome://flags/#enable-webrtc-h264-with-openh264-ffmpeg) | //
[#enable-webrtc-hide-local-ips-with-mdns](chrome://flags/#enable-webrtc-hide-local-ips-with-mdns) | //
[#enable-webrtc-new-encode-cpu-load-estimator](chrome://flags/#enable-webrtc-new-encode-cpu-load-estimator) | //
[enforce-tls13-downgrade](chrome://flags/#enforce-tls13-downgrade) | Enabled (Known root only)
[#expensive-background-timer-throttling](chrome://flags/#expensive-background-timer-throttling) | //
[#extension-content-verification](chrome://flags/#extension-content-verification) | Enforce strict
[#gdi-text-printing](chrome://flags/#gdi-text-printing) | //
[#pdf-isolation](chrome://flags/#pdf-isolation) | **Recommend !**
[#smooth-scrolling](chrome://flags/#smooth-scrolling) | //
[#tab-groups](chrome://flags/#tab-groups) | v75+ _optional_
[#tab-hover-cards](chrome://flags/#tab-hover-cards) | _optional_
[#tab-hover-card-images](chrome://flags/#tab-hover-card-images) | _optional_
[#unified-consent](chrome://flags/#unified-consent) | //



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
[#enable-javascript-harmony](chrome://flags/#enable-javascript-harmony) | //


### Android specific

Feature | Comment or setting
------------ | -------------
[#safe-browsing-telemetry-for-apk-downloads](chrome://flags/#safe-browsing-telemetry-for-apk-downloads) | Disabled
[#enable-android-night-mode](chrome://flags/#enable-android-night-mode) | Enabled (optional)
[#enable-android-spellchecker](chrome://flags/#enable-android-spellchecker) | Enabled


### Microsoft Edge (Chromium) [edge://flags]

Feature | Comment or setting
------------ | -------------
[#enable-aura-tooltips-on-windows](edge://flags/#enable-aura-tooltips-on-windows) | [Aura Dark Mode Tooltips](https://mspoweruser.com/microsofts-latest-flag-improves-dark-mode-implementation-on-chromium-based-edge/)
[#edge-cdm-override-service](edge://flags/#edge-cdm-override-service) | Enabled (Default)
[#edge-controls](edge://flags/#edge-controls) | Enabled (Default)
[#edge-cookie-import](edge://flags/#edge-cookie-import) | Disabled
[#edge-experimental-scrolling](edge://flags/#edge-experimental-scrolling) | Disabled
[#edge-follow-os-theme](edge://flags/#edge-follow-os-theme) | Enabled (Default)
[#edge-installation-of-extensions-from-microsoft-store](edge://flags/#edge-installation-of-extensions-from-microsoft-store) | Enabled (Default)
[#edge-playready-drm-win10](edge://flags/#edge-playready-drm-win10) | Enabled (Default)
[#edge-playready-drm-win10](edge://flags/#edge-playready-drm-win10) | Disabled, will break Netflix!
[#edge-reading-view](edge://flags/#edge-reading-view) | Enabled (Default)
[#edge-sign-in-with-aad](edge://flags/#edge-sign-in-with-aad) | Disabled
[#edge-user-agent-spoofing-service](edge://flags/#edge-user-agent-spoofing-service) | Enabled
[#edge-widevine-drm](edge://flags/#edge-widevine-drm) | Disabled, will break Netflix!
[#edge-reading-view-grammar-tools](edge://flags/#edge-reading-view-grammar-tools) | Grammar Tools



### Problematic do not touch!

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
#PasswordExport | ?
#PasswordImport | ?
#disable-hyperlink-auditing | 73
#enable-autofill-credit-card-last-used-date-display | ?
#enable-autofill-credit-card-upload-send-detected-values | ?
#enable-av1-decoder | ?
#enable-desktop-ios-promotions | ?
#enable-fast-unload | ?
#enable-filesystem-in-icognito | ?
#enable-gamepad-extensions | ?
#enable-md-bookmarks | ?
#enable-modern-media-controls | ?
#enable-new-app-menu-icon | ?
#enable-new-preconnect | ?
#enable-new-print-preview | ?
#enable-nup-printing | ?
#enable-password-generation | ?
#enable-policy-tool | ?
#enable-push-api-background-mode | ?
#enable-simple-cache-backend | ?
#enable-single-click-autofill | ?
#enable-site-per-process | v70
#enable-site-settings | ?
#enable-tcp-fast-open | ?
#extensions-toolbar-menu | ?
#important-sites-in-cbd | ?
#new-audio-rendering-mixing-strategy | ?
#ntp-ui-md | v70
#secondary-ui-md | v71
#show-saved-copy | ?
#simplified-fullscreen-ui | ?
#simplified-fullscreen-ui | ?
#sound-content-setting | ?
#stop-in-background | ?
#voice-search-on-local-ntp | ?


### Chrome v68 (only)
* No single background connection, there are builds compiled with and without a specific flag which toggles `chrome://net-internals/#dns`.


### DNS-over-HTTPS
 
Starting with [Chrome 78](https://blog.chromium.org/2019/09/experimenting-with-same-provider-dns.html) the Browser will get an option to control DoH via `chrome://flags/#dns-over-https` (the flag can only be opt-out'ed [but is listed in my list as enabled [[default]]), however the option is experimental and only avbl. for several users/OS, the iOS and Linux implementation is still unfinished, that been said they won't get this right of the batch. 

Supported are the following providers (for now): Cleanbrowsing, Cloudflare, DNS.SB, Google, OpenDNS & Quad9. If a provider isn't in the integrated list then Chrome will automatically use a fallback and switch back to the "normal" mode.

Fo [force Chrome to use DoH](https://bugs.chromium.org/p/chromium/issues/detail?id=799753#c8) add the following shortcut path: 
* `--enable-features="dns-over-https<DoHTrial" --force-fieldtrials="DoHTrial/Group1" --force-fieldtrial-params="DoHTrial.Group1:server/https%3A%2F%2F1.1.1.1%2Fdns-query/method/POST` 

This example will configure Chrome to use Cloudflares DoH server. To test if DoH is working or not, check the [https://1.1.1.1/help](https://1.1.1.1/help) url.  

