## MS Edge GPO Settings

You can override the MS Edge settings via GPO, the GPO settings are preferred which means you can enforce them on your system even after you turned on the sync function.

* `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft` (all user)
* `Computer\HKEY_CURRENT_USER\Software\Policies\Microsoft` (current user)
* `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\MicrosoftEdge` (**ignore it!**)


The button to control this is a 32-bit DWORD `ShowHomeButton`. Most of these are 32-bit DWORD entries with numerical options such as 0 or 1, 0 being false/disabled and 1 being true (enabled). Other entries are mostly REG_SZ type and accepting characters.


After changing/enforcing the settings you see `Managed by your organization`. You will notice a little lockbox icon next to any policy enforced settings. On newer builds you will be able to use `edge://management` again, this is where group policy settings will be visible within the browser.


### Force location of profile and/or cache files, cache size, etc (same as on the old Edge)
* UserDataDir
* DiskCacheDir
* DiskCacheSize
* MediaCacheSize
* ExtensionCacheSize


### SmartScreen related
* PreventSmartScreenPromptOverride
* SmartScreenAllowListDomains
* SmartScreenEnabled


### Edge/Sync related
* SyncDisabled
* EnableSyncConsent
* EdgeFeedbackEnabled


## Example GPO

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge]
; Always needs to be set to 1
"ShowHomeButton"=dword:00000001
; Allow to run Edge in Background
"BackgroundModeEnabled"=dword:00000000
; Autofill
"AutofillCreditCardEnabled"=dword:00000000
; Show Bookmark Bar
"BookmarkBarEnabled"=dword:00000001
; Allow other persons (profiles)
"BrowserAddPersonEnabled"=dword:00000000
; Allow Guest mode
"BrowserGuestModeEnabled"=dword:00000000
; Enable/Disable Password Manager
"PasswordManagerEnabled"=dword:00000000
; Each page runs isolated (own process)
"SitePerProcess"=dword:00000001
; Enable/Disable Address Autofill
"AutofillAddressEnabled"=dword:00000000
; Allow third-party blocking
"ThirdPartyBlockingEnabled"=dword:00000001
; Use a specific data folder (in this case a RAMDISK)
"UserDataDir"="Z:\\Profiles\\MSEdgeChromium"
; Enable/Disable SmartScreen
"SmartScreenEnabled"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist]
; Encforce extensions
"1"="ndcileolkflehcjpmjnfbnaibdcgglog;https://extensionwebstorebase.edgesv.net/v1/crx"
"2"="niloccemoadcdkdjlinkgdfekeahmflj;https://clients2.google.com/service/update2/crx"

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls]
; Load specific plugins
"1"="https://helpx.adobe.com/flash-player.html"
"2"="http://get.adobe.com/flashplayer/about/"
"3"="http://speedcheck.rogers.com/"
```