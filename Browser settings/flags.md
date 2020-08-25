### Warning
**You shouldn't use flags to configure Chrome because they're not supported. Instead, configure Chrome for your [enterprise or organization using policies](https://support.google.com/chrome/a/answer/9037717) (chrome://policy).** The original page was [removed](https://www.chromium.org/administrators/policy-list-3/atomic/_groups).  - Statement is from a Google Marketing Manager (_not my own!_).


### How to Backup and Restore Flags?
Use this [script](https://gist.github.com/kkeybbs/d817fad016b401485ab8c4c8fcffe568) to backup and restore your flags settings.


### Flags (depending which OS/Chrome version)
* Chrome 86: 
* Chrome 85: 269
* Chrome 84: 256
* Chrome 83: 254
* Chrome 82: 252
* Chrome 81: 257
* Chrome 80: 263
* Chrome 79: 273
* Chrome 78: 282
* Chrome 77: 302
* Chrome 76: 307
* Chrome 75: 311
* Chrome 74: 316


### Security (only) flags (enabled)
* (_optional_) #password-leak-detection (or use HaveIBeenPwned website/extension via KeePass, enabling this option will cause more traffic due to password checks (if some are stored in the database)
* #block-unsafe-downloads-over-insecure-connections
* #disallow-doc-written-script-loads
* #disallow-unsafe-http-downloads
* #disallow-unsafe-http-downloads
* ~~#enable-appcontainer~~
* strict-origin-isolation
* #enable-sync-uss-nigori (only if your use Browser sync!)
* #enable-tls13-early-data (disabled, GET fingerprinting)
* #reduced-referrer-granularity (only provides domain name as referer)
* #enable-webrtc-srtp-aes-gcm (if WebRTC is supported/enabled)
* #enforce-tls13-downgrade (known root only)
* #extension-content-verification
* #ignore-gpu-denylist (disabled) (_outdated_)
* #native-file-system-api (_disable_)
* #pdf-isolation (will be removed and is only relevant in case you read PDFs via Browser)
* #treat-unsafe-downloads-as-active-content
* `--enable-quic` & `--quic-version=h3-23` as command line argument to [enable HTTP/3](https://blog.cloudflare.com/http3-the-past-present-and-future/) See here how to run [Chrome with flags](https://www.chromium.org/developers/how-tos/run-chromium-with-flags).
* Microsoft Edge tracking prevention (_optional_ - MS Edge + Defender only [via Chrome 75+ with Ent. GPO policy])
* #tls13-hardening-for-local-anchors
* #cross-origin-isolation
* #treat-unsafe-downloads-as-active-content
* #post-quantum-cecpq2


### Privacy (only) flags (enabled)
* #allow-popups-during-page-unload (_disable_)
* #autofill-prune-suggestions (if autofill was enabled)
* #cookies-without-same-site-must-be-secure + #same-site-by-default-cookies (both must be enabled, might break websites!)
* #data-saver-server-previews (disabled)
* #device-discovery-notifications
* #disable-hyperlink-auditing (_outdated_)
* #dns-over-https
* #enable-autofill-upi-vpa
* #enable-data-reduction-proxy-with-network-service (connect to Google - disabled)
* #enable-filesystem-in-incognito
* #enable-generic-sensor (disabled, fingerprinting)
* #enable-history-manipulation-intervention
* #enable-removing-all-third-party-cookies
* #enable-safe-browsing-ap-download-verdicts (_disabled_ better use uBlock with a malware filter list_)
* #enable-sharing-device-registration
* #enable-speculative-service-worker-start-on-query-input (disabled + performance/fingerprinting reasons)
* #enable-webrtc-hide-local-ips-with-mdns
* #enable-webrtc-remote-event-log (_optional_) (if WebRTC is allowed/enabled)
* #enable-webvr (prevent possible WebVR API based fingerprinting methods)
* #enterprise-reporting-in-browser (disabled)
* #happiness-tracking-surveys-for-desktop (_disable_)
* #improved-cookie-controls
* #improved-cookie-controls-for-third-party-cookie-blocking
* #omnibox-drive-suggestions (_disable_)
* #omnibox-experimental-keyword-mode (_disable_)
* #omnibox-suggestion-transparency-options
* #omnibox-zero-suggestions-on-ntp-realbox (_disable_)
* #passwords-account-storage (disabled) (_use KeePass instead and disable all "Gaia account features"_)
* ##use-multilogin-endpoint (_disabled_)
* #pdf-form-save (_disable_)
* #prefetch-privacy-changes
* #reduced-referrer-granuarity
* #search-results-extensions-block-v2 (_Opera only_)
* #sharing-use-device-info
* #tab-hover-cards (disabled)
* #turn-off-streaming-media-caching
* #unified-consent
* #enable-user-data-snapshot (_disable_)
* #media-history (_disable_)
* #use-new-accept-language-header (_disable_)
* #use-sync-sandbox (_connect to Google_)
* Anonymize local IPs exposed by WebRTC (_outdated_)
* Disable minimum for server-side tile suggestions on NTP (_disable_) (_outdated_)
* New history entries require a user gesture (_outdated_)
* Top Sites from Site Engagement (_disable_) (_outdated_)
* #webxr-plane-detection (_disable_)
* enable-text-fragment-anchor (_disable_)
* [#cors-for-content-scripts](https://www.chromium.org/Home/chromium-security/extension-content-script-fetches)
* [#freeze-user-agent](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/-2JIRNMWJ7s/yHe4tQNLCgAJ)
* ~~Enable search suggestions on the local NTP (_disable_) (_outdated_)~~
* ~~#omnibox-ui-hide-steady-state-url-scheme~~
* ~~#omnibox-ui-hide-steady-url-trivial-subdomains~~
* ~~#omnibox-ui-hide-steady-state-url-path-query-and-ref~~
* ~~#simplify-https-indicator~~
* ~~#heavy-ad-privacy-mitigation~~


## Performance (only) flags (enabled)
* #animated-avatar-button (_disable_)
* #cast-media-route-provider (_disable_)
* #d3d11-video-decoder
* #enable-gpu-rasterization
* #enable-layout-ng
* #enable-lazy-frame-loading
* #enable-lazy-image-loading
* #enable-parallel-downloading
* ~~Enable doodles on the local NTP (_disable_)~~ (_outdated_)
* ~~Enable search suggestions on the local NTP (_disable_)~~ (_outdated_)
* #in-product-help-demo-mode-choice (_disable_)
* #load-media-router-component-extension (WARNING: Don't touch it (breaks the "Cast" feature _optional_ to avoid Google startup connections/loopback)
* enable-heavy-ad-intervention


## Advertising (only) flags (enabled)
* #happiness-tracking-surveys-for-desktop-demo (disabled)
* ~~App Banners (disabled)~~ (_outdated_)
* ~~Autoplay policy (document user activation required)~~ (_outdated_)
* ~~Enable promos on the local NTP (disabled)~~ (_outdated_)
* ~~User Activation V2 (disabled)~~ (_outdated_)


### Enabled

The flags are listed via `https://flags/`.

Feature | Comment/setting
------------ | -------------
[#audio-worklet-realtime-thread](https://flags/#audio-worklet-realtime-thread) | **Recommend !**
[#automatic-tab-discarding](https://flags/#automatic-tab-discarding) | //
[#autoplay-policy](https://flags/#autoplay-policy) | Document user activation is required.
[#chrome-colors](https://flags/#chrome-colors) | //
[#chrome-custom-color-picker](https://flags/#chrome-colors-custom-color-picker) | //
[#clipboard-content-setting](https://flags/#clipboard-content-setting) | //
[#cookies-without-same-site-must-be-secure](https://flags/#cookies-without-same-site-must-be-secure) | **Recommend !** See [here](https://scotthelme.co.uk/csrf-is-really-dead/)
[#cross-origin-embedder-policy](https://flags/#cross-origin-embedder-policy) | **Recommend !**
[#disable-javascript-harmony-shipping](https://flags/#disable-javascript-harmony-shipping) | (Enabled [Default])
[#disallow-doc-written-script-loads](https://flags/#disallow-doc-written-script-loads) | **Recommend !**
[#disallow-unsafe-http-downloads](https://flags/#disallow-unsafe-http-downloads) | **Recommend !**
[#dns-over-https](https://flags/#dns-over-https) | **Recommend !**
[#drag-to-pin-tabs](https://flags/#drag-to-pin-tabs]) | _optional_
[#enable-appcontainer](https://flags/#enable-appcontainer) | [**Recommend !**](https://blog.chromium.org/2019/09/experimenting-with-same-provider-dns.html)
[#enable-autofill-credit-card-ablation-experiment](https://flags/#enable-autofill-credit-card-ablation-experiment) | //
[#enable-block-tab-unders](https://flags/#enable-block-tab-unders) | //
[#enable-brotli](https://flags/#enable-brotli) | //
[#enable-experimental-fling-animation](https://flags/#enable-experimental-fling-animation) | //
[#enable-framebusting-needs-sameorigin-or-usergesture](https://flags/#enable-framebusting-needs-sameorigin-or-usergesture) | //
[#enable-future-v8-vm-features](https://flags/#enable-future-v8-vm-features) | //
[#enable-gpu-appcontainer](https://flags/#enable-gpu-appcontainer) | **Recommend !**
[#enable-history-entry-requires-user-gesture](https://flags/#enable-history-entry-requires-user-gesture) | //
[#enable-history-manipulation-intervention](https://flags/#enable-history-manipulation-intervention) | //
[#enable-mark-http-as](https://flags/#enable-mark-http-as) | Mark as actively dangerous
[#enable-message-center-new-style-notification](https://flags/#enable-message-center-new-style-notification) | //
[#enable-native-notifications](https://flags/#enable-native-notifications) | //
[#enable-origin-trials](https://flags/#enable-origin-trials) | //
[#enable-parallel-downloading](https://flags/#enable-parallel-downloading) | //
[#enable-picture-in-picture](https://flags/#enable-picture-in-picture) | //
[#enable-pixel-canvas-recording](https://flags/#enable-pixel-canvas-recording) | **Recommend !**
[#enable-quic](https://flags/#enable-quic) | Controversial, I **recommend enabling it**
[#enable-reader-mode](https://flags/#enable-reader-mode) | _optional_
[#enable-webrtc-h264-with-openh264-ffmpeg](https://flags/#enable-webrtc-h264-with-openh264-ffmpeg) | //
[#enable-webrtc-hide-local-ips-with-mdns](https://flags/#enable-webrtc-hide-local-ips-with-mdns) | **Recommend !**
[#enable-webrtc-new-encode-cpu-load-estimator](https://flags/#enable-webrtc-new-encode-cpu-load-estimator) | //
[#enforce-tls13-downgrade](https://flags/#enforce-tls13-downgrade) | Enabled (Known root only) **Recommend !**
[#expensive-background-timer-throttling](https://flags/#expensive-background-timer-throttling) | //
[#extension-content-verification](https://flags/#extension-content-verification) | Enforce strict (hard fail) - **Recommend !**
[#ForcedColors](https://flags/#ForcedColors) | _usability_ (_[optional](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Accessibility/HighContrast/explainer.md)!_)
[#gdi-text-printing](https://flags/#gdi-text-printing) | //
[#ignore-gpu-denylist](https://flags/#ignore-gpu-denylist) | **Recommend !** (disabled)
[#isolate-origins](https://flags/#isolate-origins) | **Recommend !**, [see here why](https://wicg.github.io/isolation/)
[#new-tab-button-position](https://flags/#new-tab-button-position) | **Recommend !** (_optional_)
[#ntp-customization-menu-v2](https://flags/#ntp-customization-menu-v2) | //
[#overlay-scrollbars-flash-after-scroll-update](https://flags/#overlay-scrollbars-flash-after-scroll-update) | **Recommend !**
[#overlay-scrollbars-flash-when-mouse-enter](https://flags/#overlay-scrollbars-flash-when-mouse-enter) | **Recommend !**
[#overlay-scrollbars](https://flags/#overlay-scrollbars) | **Recommend !**
[#pdf-isolation](https://flags/#pdf-isolation) | **Recommend !**
[#privacy-settings-redesign](https://flags/#privacy-settings-redesign) | **Recommend !**
[#proactive-tab-freeze](https://flags/#proactive-tab-freeze) | **Recommend !** (_optional_)
[#reduced-referrer-granuarity](https://flags/#reduced-referrer-granuarity) | **Recommend !**
[#show-legacy-tls-warnings](https://flags/#show-legacy-tls-warnings) | **Recommend !**
[#smooth-scrolling](https://flags/#smooth-scrolling) | //
[#tab-groups](https://flags/#tab-groups) | v75+ _optional_
[#tab-hover-card-images](https://flags/#tab-hover-card-images) | _optional_
[#tab-hover-cards](https://flags/#tab-hover-cards) | _optional_
[#unified-consent](https://flags/#unified-consent) | //
[#use-angle](https://flags/#use-angle) | D3D11on12 **Recommend !**



### Disabled

Feature | Comment or suggestion
------------ | -------------
[#account-consistency](https://flags/#account-consistency) | //
[#allow-previews](https://flags/#allow-previews) | //
[#allow-sxg-certs-without-extension](https://flags/#allow-sxg-certs-without-extension) | //
[#autofill-always-return-cloud-tokenized-card](https://flags/#autofill-always-return-cloud-tokenized-card) | //
[#back-forward-cache](https://flags/#back-forward-cache) | // (_possible breakage_)
[#calculate-native-win-occlusion](https://flags/#calculate-native-win-occlusion) | //
[#click-to-call-context-menu-selected-text](https://flags/#click-to-call-context-menu-selected-text) | //
[#click-to-call-ui](https://flags/#click-to-call-ui) | //
[#data-saver-server-previews](https://flags/#data-saver-server-previews) | //
[#device-discovery-notifications](https://flags/#device-discovery-notifications) | //
[#enable-ambient-authentication-in-incognito](https://flags/#enable-ambient-authentication-in-incognito) | //
[#enable-autofill-credit-card-upload](https://flags/#enable-autofill-credit-card-upload) | //
[#enable-data-reduction-proxy-with-network-service](https://flags/#enable-data-reduction-proxy-with-network-service) | //
[#enable-de-jelly](https://flags/#enable-de-jelly) | //
[#enable-experimental-productivity-features](https://flags/#enable-experimental-productivity-features) | //
[#enable-generic-sensor-extra-classes](https://flags/#enable-generic-sensor-extra-classes) | //
[#enable-generic-sensor](https://flags/#enable-generic-sensor) | //
[#enable-javascript-harmony](https://flags/#enable-javascript-harmony) | //
[#enable-ftp](https://flags/##enable-ftp) | //
[#enable-lookalike-URL-navigation-suggestions](https://flags/#enable-lookalike-url-navigation-suggestions) | //
[#enable-media-session-service](https://flags/#enable-media-session-service) | Volume OSD (optional)
[#enable-native-google-assistant](https://flags/#enable-native-google-assistant) | [//](https://www.howtogeek.com/429382/how-to-enable-google-assistant-on-your-chromebook/)
[#enable-noscript-previews](https://flags/#enable-noscript-previews) | //
[#enable-optimization-hints](https://flags/#enable-optimization-hints) | //
[#enable-reopen-tab-in-product-help](https://flags/#enable-reopen-tab-in-product-help) | //
[#enable-send-tab-to-self-broadcast](https://flags/#enable-send-tab-to-self-broadcast) | //
[#enable-sync-uss-nigori](https://flags/#enable-sync-uss-nigori) | //
[#enable-winrt-geolocation-implementation](https://flags/#enable-winrt-geolocation-implementation) | //
[#fill-on-account-select-http](https://flags/#fill-on-account-select-http) | //
[#fill-on-account-select](https://flags/#fill-on-account-select) | //
[#global-media-controls](https://flags/#global-media-controls) | //
[#happiness-tracking-surveys-for-desktop](https://flags/#happiness-tracking-surveys-for-desktop) | //
[#hardware-media-key-handling](https://flags/#hardware-media-key-handling) | Avoid media stats leakage
[#network-service](https://flags/#network-service) | //
[#new-tab-loading-animation](https://flags/#new-tab-loading-animation) | ([optional](https://old.reddit.com/r/chrome/comments/ahxx8c/new_tab_loading_animation/))
[#new-tabstrip-animation](https://flags/#new-tabstrip-animation) | //
[#new-usb-backend](https://flags/#new-usb-backend) | //
[#ntp-realbox](https://flags/#ntp-realbox) | //
[#omnibox-disable-instant-extended-limit](https://flags/#omnibox-disable-instant-extended-limit) | //
[#omnibox-drive-suggestions](https://flags/#omnibox-drive-suggestions) | Workaround for a bug
[#omnibox-rich-entity-suggestion](https://flags/#omnibox-rich-entity-suggestion) | Since 74.0.3729.169 enabled
[#omnibox-ui-hide-steady-state-url-scheme-and-subdomains](https://flags/#omnibox-ui-hide-steady-state-url-scheme-and-subdomains) | //
[#omnibox-ui-hide-steady-state-url-scheme](https://flags/#omnibox-ui-hide-steady-state-url-scheme) | hides https:// only
[#omnibox-ui-hide-steady-state-url-trivial-subdomains](https://flags/#omnibox-ui-hide-steady-state-url-trivial-subdomains) | hides www only
[#omnibox-zero-suggestions-on-ntp](https://flags/#omnibox-zero-suggestions-on-ntp) | //
[#omnibox-zero-suggestions-on-serp](https://flags/#omnibox-zero-suggestions-on-serp) | //
[#pdf-form-save](https://flags/#pdf-form-save) | //
[#percent-based-scrolling](https://flags/#percent-based-scrolling) | // (_possible breakage_)
[#reduced-referrer-granularity](https://flags/#reduced-referrer-granularity) | //
[#safe-search-url-reporting](https://flags/#safe-search-url-reporting) | //
[#safety-tips](https://flags/#safety-tips) | //
[#shared-clipboard-receiver](https://flags/#shared-clipboard-receiver) | //
[#show-autofill-type-predictions](https://flags/#show-autofill-type-predictions) | //
[#show-managed-ui](https://flags/#show-managed-ui) | //
[#tab-hover-cards](https://flags/#tab-hover-cards) | //
[#use-new-accept-language-header](https://flags/#ntp-realbox) | //
[#username-first-flow](https://flags/#username-first-flow) | //
[#web-bundles](https://flags/#web-bundles) | //
[#omnibox-ui-reveal-steady-state-url-path-query-and-ref-on-hover](https://flags/#omnibox-ui-reveal-steady-state-url-path-query-and-ref-on-hover) | //
[#omnibox-ui-sometimes-elide-to-registrable-domain](https://flags/#omnibox-ui-sometimes-elide-to-registrable-domain) | //
[#passwords-weakness-check](#passwords-weakness-check) | //


### Android specific

Feature | Comment or setting
------------ | -------------
[#safe-browsing-telemetry-for-apk-downloads](https://flags/#safe-browsing-telemetry-for-apk-downloads) | Disabled
[#enable-android-night-mode](https://flags/#enable-android-night-mode) | Enabled (optional)
[#enable-android-spellchecker](https://flags/#enable-android-spellchecker) | Enabled
[#enable-site-isolation-for-password-sites](https://flags/#enable-site-isolation-for-password-sites) | Enabled (v74+)

### [Microsoft Edge (Chromium)](https://blogs.windows.com/windowsexperience/2019/11/04/introducing-the-new-microsoft-edge-and-bing/) specific [edge://flags](https://docs.microsoft.com/en-us/microsoft-edge/privacy-whitepaper)

Most Chromium based flags for Edge are explained over [here](https://github.com/MicrosoftEdge/MSEdgeExplainers). The project basically explains what each flag does (with Info, screenshots & more).

Feature | Comment or setting
------------ | -------------
[#edge-ForcedColors](edge://flags/#ForcedColors) | Enabled (_usability_)
[#enable-aura-tooltips-on-windows](edge://flags/#enable-aura-tooltips-on-windows) | [Aura Dark Mode Tooltips](https://mspoweruser.com/microsofts-latest-flag-improves-dark-mode-implementation-on-chromium-based-edge/)
[#edge-cdm-override-service](edge://flags/#edge-cdm-override-service) | Enabled (Default)
[#edge-controls](edge://flags/#edge-controls) | Enabled (Default)
[#edge-cookie-import](edge://flags/#edge-cookie-import) | Disabled
[#edge-dns-over-https](edge://dns-over-https) | Disabled due to privacy/ad-blocking reasons!
[#edge-experimental-scrolling](edge://flags/#edge-experimental-scrolling) | Disabled
[#edge-follow-os-theme](edge://flags/#edge-follow-os-theme) | Enabled (Default)
[#edge-installation-of-extensions-from-microsoft-store](edge://flags/#edge-installation-of-extensions-from-microsoft-store) | Enabled (Default)
[#edge-strict-origin-isolation](edge://edge-strict-origin-isolation) | **Recommend !**
[#edge-playready-drm-win10](edge://flags/#edge-playready-drm-win10) | Disabling it will break e.g. Netflix!
[#edge-reading-view](edge://flags/#edge-reading-view) | Enabled (Default)
[#edge-sign-in-with-aad](edge://flags/#edge-sign-in-with-aad) | Disabled
[#edge-user-agent-spoofing-service](edge://flags/#edge-user-agent-spoofing-service) | Enabled
[#edge-widevine-drm](edge://flags/#edge-widevine-drm) | Disabled, will break Netflix!
[#edge-reading-view-grammar-tools](edge://flags/#edge-reading-view-grammar-tools) | Grammar Tools
[#enable-force-dark](edge://flags/#enable-force-dark) | Enforce use of "Dark Mode"
[#global-media-controls](edge://flags/#global-media-controls) | Enable media control buttons
[#edge-enable-shy-ui](edge://flags/#edge-enable-shy-ui) | Fullscreen Dropdown (_matter of taste_)
[#edge-ee-spinner-on-site-card](#edge://flags/#edge-ee-spinner-on-site-card) | **Recommend !**
[#mixed-content-setting](#edge://flags/#mixed-content-setting) | **Recommend !**
[#edge-collections](#edge://flags/#edge-collections) | (_optional_)
[#win-use-native-spellchecker](edge://flags/#win-use-native-spellchecker) | **Recommend !**
[#omnibox-ui-show-suggestion-favicons ](#edge://flags/#omnibox-ui-show-suggestion-favicons ) | (_optional_)
[#edge-autoplay-user-setting-block-option](edge://flags/#edge-autoplay-user-setting-block-option) | **Recommend !**
[#edge-smartscreen-pua](edge://flags/#edge-smartscreen-pua) | **Disable Recommend !**
* Anonymize local IPs exposed by WebRTC | Enabled
* Extension Content Verification | Enforce Strict
* Reduce default 'referer' header granularity | Enabled
* Load Media Router Component Extension | Disabled
* Connect to Cast devices on all IP addresses | Disabled
* Block scripts loaded via document.write | Enabled
* Parallel downloading | Enabled
* Mark non-secure origins as non-secure | Enabled (mark as active dangerous)
* Treat risky downloads over insecure connections as active mixed content | Enabled
* De-elevate browser on launch | Enabled
* Enable IE Integration | Disabled
* Strict-Origin-Isolation | Enabled
* SameSite by default cookie | Enabled
* Cookies without SameSite must be secure | Enabled
* Microsoft Edge tracking prevention | Enabled (default)
* Experimental Tracking Prevention Features | Enabled
* Potentially unwanted app protection | Enabled (default)
* [post-quantum-cecpq2](https://techcommunity.microsoft.com/t5/discussions/new-feature-in-microsoft-edge-tls-post-quantum-confidentiality/m-p/1196977#) | Enabled
* Enable SmartScreen Model Evaluation | Disabled
* Secure DNS lookups | Disabled (use DNSCrypt/VPN)


### Other MS Edge (Chromium) "Tweaks"

* Multiple profiles (ssuming you have multiple) can be enabled via `edge://settings/profiles/multiProfileSettings`.
* In order to **enable the new Extensions Menu**, create a shortcut or edit the existing shortcut `--enable-features=ExtensionsToolbarMenu` The example should then look like this: `msedge.exe --enable-features=ExtensionsToolbarMenu`.
* [Improving Tracking Prevention in Microsoft Edge](https://blogs.windows.com/msedgedev/2019/12/03/improving-tracking-prevention-microsoft-edge-79/#s7m17j2ibI4KAxAz.97)
* `edge://site-engagement` checks how often you visit your websites (how "popular they are), Chrome uses `chrome://site-engagement, see [here](https://www.chromium.org/developers/design-documents/site-engagement) for more information.
* Enable `edge://flags/#edge-allow-store-extension-themes` to allow EDgeium to install Themes from Chrome Web Store.
* #edge-limit-media-autoplay (will be removed, edge only)
* #edge-strict-origin-isolation (replaces app container lockdown)
* ~~legacy-tls-enforced~~ outdated, Edge 74+ disables TLS 1.0 & 1.1 by default
* ~~#edge-de-elevate-on-launch~~ removed
* ~~#edge-smartscreen-evaluate-model~~ removed 
* ~~#passive-mixed-content-warning~~ removed
* ~~#edge-wdag-prelaunch~~ EOL (prelaunch can be controlled via GUI)
* ~~#edge-mf-clear-playback-Windows 10~~ Causes too many problems


### Brave
[#brave-adblock-cosmetic-filtering](chrome://flags/#brave-adblock-cosmetic-filtering) | enabled


### Some flags are (in general) problematic - do not touch! -

Some flags can cause "critical security holes" in your configuration even if you enable/disable them to prevent exactly this. The flags are been tested against [BrowserAudit](https://browseraudit.com/test), however keep in mind that the test page might not be 100% accurate!

Feature | Reason
------------ | -------------
[#allow-sxg-certs-without-extension](https://flags/#allow-sxg-certs-without-extension) | Triggers an critical error (DOM)
[#enable-signed-http-exchange](https://flags/#enable-signed-http-exchange) | Triggers an critical error (DOM)
[#focus-mode](https://flags/#focus-mode) | Leakage (?) unconfirmed, triggers warnings
[#enable-built-in-module-kv-storage](https://flags/#enable-built-in-module-kv-storage) | Leakage (?) unconfirmed, triggers warnings
[#enable-built-in-module-infra](https://flags/#enable-built-in-module-infra) | Possible attacks
[#disable-windows10-custom-titlebar](https://flags/#disable-windows10-custom-titlebar) | Only if you really need it




### Deprecated

Feature | Deprecated or removed since
------------ | -------------
#allow-running-insecure-content | [v81](https://security.googleblog.com/2019/10/no-more-mixed-messages-about-https_3.html)
#disable-hyperlink-auditing | v73
#enable-appcontainer | v78
#enable-autofill-credit-card-last-used-date-display | v76
#enable-autofill-credit-card-upload-send-detected-values | v75
#enable-av1-decoder | v74
#enable-block-tab-unders | 78+
#enable-client-lo-fi | v78+
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
#PasswordExport | v77
#PasswordImport | v77
#secondary-ui-md | v71
#show-saved-copy | v71
#simplified-fullscreen-ui | v70
#simplified-fullscreen-ui | v71
#sound-content-setting | v70
#stop-in-background | v70
#temporary-unexpire-flags-m76 | 80
#voice-search-on-local-ntp | v70
#appcontainer | 81
#gpu-appcontainer | 81


### DNS-over-HTTPS

Starting with [Chrome 78](https://blog.chromium.org/2019/09/experimenting-with-same-provider-dns.html) the Browser will get an option to control DoH via `https://flags/#dns-over-https` (the flag can only be opt-out'ed [but is listed in my list as enabled [[default]]), however the option is experimental and only avbl. for several users/OS, the iOS and Linux implementation is still unfinished, that been said they won't get this right of the batch.

Supported are the following providers (for now): Cleanbrowsing, Cloudflare, DNS.SB, Google, OpenDNS & Quad9. If a provider isn't in the integrated list then Chrome will automatically use a fallback and switch back to the "normal" mode.

Fo [force Chrome to use DoH](https://bugs.chromium.org/p/chromium/issues/detail?id=799753#c8) add the following shortcut path:
* `--enable-features="dns-over-https<DoHTrial" --force-fieldtrials="DoHTrial/Group1" --force-fieldtrial-params="DoHTrial.Group1:server/https%3A%2F%2F1.1.1.1%2Fdns-query/method/POST`

This example will configure Chrome to use Cloudflares DoH server. To test if DoH is working or not, check the [https://1.1.1.1/help](https://1.1.1.1/help) url.


### Fooling the NTP to increase the Browser performance and to gain some (questionable) privacy benefit

There is some traffic caused for NTP lookups, this can be disabled with the following trick:
* Change your default search engine to "Startpage" and remove all other search engines in your lists.
* Enable or disable the following flags `Enable using the Google local NTP`, `Enable doodles on the local NTP` (_disable_), `Enable search suggestions on the local NTP` (_disable_), `Top Sites from Site Engagement` (_disable_), `Disable minimum for server-side tile suggestions on NTP` (_disable_) & `Enable promos on the local NTP` (_disable_).


### Chrome/Chromium Command Line Switches

If you add a command-line argument that is also used in `/flags`, the flag's state will *not be indicated* in `chrome://flags`. You can find them only manually by checking `chrome://version`.

| In chrome://flags | Command | Comment | 
| :--              | :--        |         --: |    
| :x:           | `--disable-beforeunload`        | Disables JavaScript dialog boxes |    
| :x:           | `--disable-encryption`        | Windows only  | 
| :x:           | `--disable-machine-id`        | Windows only  | 
| :x:           | `--disable-search-engine-collection`        | Disable automatic search engine scraping from webpages.  | 
| :white_check_mark:           | `--enable-stacked-tab-strip`        | Controls the tab strip behavior.  | 
| :x:           | `--enable-tab-adjust-layout`        | Needed if `--enable-stacked-tab-strip` was altered. | 
| :white_check_mark:           | `--disable-features=PostQuantumCECPQ2 www.github.com`        | Example to exclude specific and problematic pages froms the `post-quantum-cecpq2` flag | 
| :white_check_mark:           | `--extension-mime-request-handling`        | Change how extension MIME types (CRX and user scripts) are handled. | 
| :x:           | `--fingerprinting-canvas-image-data-noise`        | Bromite only  |
| :x:           | `--fingerprinting-canvas-measuretext-noise`        | Bromite only  |
| :x:           | `--fingerprinting-client-rects-noise`        | Bromite only  |
| :x:           | `--max-connections-per-host`        | Bromite only, added in Chromium. Range between 6 and 15.  |
| :x:           | `--hide-crashed-bubble`        | Hide `"Restore Pages? Chromium didn't shut down correctly."` |
| :x:           | `--pdf-plugin-name`        | Allows to set the internal PDF viewer plugin name. |
| :x:           | `--scroll-tabs`        | Linux only, the flag requires one the values: always, never, incognito-and-guest |
| :x:           | `--show-avatar-button`        | The flag requires one of the values: always, incognito-and-guest. |
| :x:           | `--set-ipv6-probe-false`        | Priotize IPv4 addresses over IPv6 addresses by dropping the IPv6 connectivity test. |

