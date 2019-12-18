Blocker Toolkit to disable automatic delivery of Microsoft Edge
--------------

Microsoft will distribute Microsoft Edge (Chromium-based) through Automatic Updates for Windows 10 RS4 (1803) and newer.

* https://docs.microsoft.com/en-us/deployedge/microsoft-edge-blocker-toolkit



MacOS
--------------

All builds for MacOS:
* https://www.microsoftedgeinsider.com/en-us/download/?platform=macos

Stable:
* http://go.microsoft.com/fwlink/?LinkID=2093438


Windows
--------------

Starting with 77.0.234.0 how to enable Windows OS Spellchecker `edge://flags/#win-use-native-spellchecker`.


ALl download links:
* microsoftedgeinsider.com/download/win10
* microsoftedgeinsider.com/download/platform=win8dot1
* microsoftedgeinsider.com/download/platform=win8
* microsoftedgeinsider.com/download/platform=win7


Dev Offline Installer
* https://www.microsoftedgeinsider.com/en-us/enterprise
* [MicrosoftEdgeDevEnterpriseX64.msi](https://go.microsoft.com/fwlink/?LinkID=2093291)
* [MicrosoftEdgeDevEnterpriseX86.msi](https://go.microsoft.com/fwlink/?LinkID=2093436)


Roadmap:
* The official roadmap can be found over [here](https://blogs.windows.com/msedgedev/2019/07/16/microsoft-edge-enterprise-evaluation-roadmap/#oe2PuqSTS3mYvoGV.97).

Stable:
* https://go.microsoft.com/fwlink/?linkid=2069324&Channel=Stable (_replace Stable&language=de in the URL with US/GB or to whatever your native language is_)

Stable (x64.msi)
* http://go.microsoft.com/fwlink/?LinkID=2093437

Stable (x86.msi)
* http://go.microsoft.com/fwlink/?LinkID=2093505



ARM
--------------

Canary (needs to be started with `–msedge-sxs`
* `https://mega.nz/#!M1BDzI5K!n8o0Noy_wi8etauRATKMPKT-qC5Ls_KheMr6c8dYDqQ` Source & Credit: [via Twitter](https://twitter.com/ADeltaXForce/status/1136654348983967744)


### Information about the URL scheme

The SHA1 hash and the URL rotates, depending on the version you like to download (yes, MS keeps older versions). The above links are basically only examples.


Sandbox (users)
--------------
Under `C:\Users\WDAGUtilityAccount\AppData\Local\MicrosoftEdge` there is the `Applicationmsedge.exe`.




User Agent switcher (still works but might gets removed)
--------------

```batch
// Facebook
"domain":"facebook.com",
               "applied_policy":"ChromeUA"
```

```batch
// Netflix, HBO etc (for DRM)
"domain":"netflix.com",
               "applied_policy":"EdgeUA"
```

More info about the User-Agent switcher is avbl. [here](https://www.bleepingcomputer.com/news/microsoft/the-new-microsoft-edge-sometimes-impersonates-other-browsers/).


Change default display language
--------------
Close Microsoft Edge (Chromium) and ensure no background task is running! Download the desired language pack from [here](https://chromium.googlesource.com/chromium/reference_builds/chrome_win/+/f4b7e74a777e85405b284a55ce6e3d798bca7159/locales), it is a `.pak` file.


* Canary: `C:\Users\<your-user/pc-name>\AppData\Local\Microsoft\Edge SxS\Application\76.0.152.0\Locales`
* Dev:    `C:\Program Files (x86)\Microsoft\Edge Dev\Application\75.0.139.4\Locales`
* Beta:   `C:\Program Files (x86)\Microsoft\Edge Beta\Application\75.0.139.7\Locales`



Create a new folder and place every other language into it EXCEPT the one you like to switch to so e.g `\Locales\New Folder\` & `\Locales\ru.pak` is then your folder structure. Restart Edge after you're done.


**Warning**
* After you changed the language you might get DPI problems (e.g. the menu is to wide). That's a _known problem_ and depending which DPI you set for your fonts.


### Official Landing pages

* https://32767.ga/edge/
* https://www.microsoftedgeinsider.com/en-us/download
* https://chromium.googlesource.com/chromium/reference_builds/chrome_win/+/f4b7e74a777e85405b284a55ce6e3d798bca7159/locales (language packs)
* https://twitter.com/MSEdgeDev
* https://www.microsoftedgeinsider.com/en-us/download/

### Security Baseline (DRAFT) for Edgeium
* https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991 (_Microsoft Edge v78.zip_)
* https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/1066051 (_Microsoft Edge v79.zip, see [blog post](https://blogs.windows.com/msedgedev/2019/12/18/security-baseline-draft-edge-79/)_)


### Policy Templates
* http://go.microsoft.com/fwlink/?LinkID=2099616 (.cab)
* http://go.microsoft.com/fwlink/?LinkID=2099617 (_MicrosoftEdgeIntunePolicyTemplate.cab_)
* ~~https://techcommunity.microsoft.com/gxcuf89792/attachments/gxcuf89792/EdgeInsiderDiscussions/5164/1/Microsoft%20Edge%20(Insider)%20AdministrativeTemplate.zip (.zip)~~ (_removed by MS and replaced with .cab)


### Blog
* https://techcommunity.microsoft.com/t5/Discussions/Early-preview-of-Microsoft-Edge-group-policies/m-p/693929
* [Blog listing what is new for Canary channel](https://techcommunity.microsoft.com/t5/Discussions/Canary-channel-update-to-80-0-319-0-is-live/m-p/968799)
* [Blog listing what is new for Dev channel](https://techcommunity.microsoft.com/t5/Discussions/Dev-channel-update-to-80-0-334-2-is-live/m-p/1018372)
* [New Tab Page Walkthrough](https://techcommunity.microsoft.com/t5/Articles/New-Tab-Page-Walkthrough/m-p/480053#M550)


### Change log
The Edge Insider Team continues to add new info to this page:
* https://www.microsoftedgeinsider.com/en-us/whats-new
* https://www.microsoftedgeinsider.com/en-us/welcome/update?channel=stable&version=76.0.182.6
