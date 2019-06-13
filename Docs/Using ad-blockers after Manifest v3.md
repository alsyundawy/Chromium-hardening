### What happened?
Chrome decided to deprecate the blocking capabilities of the webRequest API in [Manifest V3](https://groups.google.com/a/chromium.org/forum/m/#!msg/chromium-extensions/veJy9uAwS00/9iKaX5giAQAJ), not the entire webRequest AP! This manifest does not only break ad-blockers, it also affects other extensions [such as Tampermonkey](https://9to5google.com/2019/01/29/chrome-manifest-v3-tampermonkey/).

The official Manifest can be found [here](https://docs.google.com/document/d/1nPu6Wy4LWR66EFLeYInl3NzzhHzc-qnk4w4PX-0XMw8/edit#heading=h.xgjl2srtytjt).

### Which Chrome(ium) based Browser are not affected?
Brave promised to [revert the new webRequest API changes](https://www.reddit.com/r/uBlockOrigin/comments/buijcf/google_relents_slightly_on_blocking_adblockers/epg198z/). See also [here](https://old.reddit.com/r/brave_browser/comments/buhq20/chrome_to_limit_full_ad_blocking_extensions_to/epdmuk5/). Vivaldi also [promised to take action](https://vivaldi.com/blog/chromium-ad-blocker).

### Using ad-block(er) does not require an "Enterprise Chrome version"
There are several wrong news spread around the internet that ad-blocking needs a "special Enterprise" version, this is totally wrong. 

### About the Enterprise version
The "Enterprise" version is basically spoken just a normal Chrome version packaged as an .MSI for easy deployment using some kind of software distribution tool. The tool itself is closed source.

What people need is a Windows version which (officially) deploy some type of [Group Policy](https://support.google.com/chrome/a/answer/7650032?hl=en&ref_topic=7649835) to enable this. Typically that's a Windows 10 Pro/Enterprise version which comes with (gpedit.msc) the Group Policy Editor.

[Windows 10 Home users can install gpedit manually](https://www.itechtics.com/enable-gpedit-windows-10-home/). There are also [unofficial tools](https://www.ryadel.com/en/group-policy-editor-windows-10-home-gpedit-msc-policyplus-gpsearch/) to enable it.

### "Unlocking" Ad-Blocking after Manifest V3

* [Download the Chrome "Enterprise version" (the .msi) file](https://github.com/CHEF-KOCH/Chromium-hardening/blob/master/Docs/Chrome%20download%20URLs.md).
* Download the Policy and [preferences templates](https://support.google.com/chrome/a/answer/7650032?hl=en&ref_topic=7649835) (_it's not yet updated)_.
* [Import the .admx template](https://www.windowstricks.in/2016/06/import-admx-files-windows-10.html). _I assume MacOS/Linux users getting a separate template_ (**speculation**). I will upload them [here](https://github.com/CHEF-KOCH/Chromium-hardening/tree/master/Chrome%20Policy).
* That's pretty much it.


## Resources
- [Google creates ad blocker Chrome extension for performance testing (9to5google.com)](https://9to5google.com/2019/06/13/google-creates-chrome-ad-blocker-extension/)
- [Improving Security and Privacy for Extensions Users (security.googleblog.com)](https://security.googleblog.com/2019/06/improving-security-and-privacy-for.html) 
