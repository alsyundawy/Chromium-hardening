
### How do I capture traffic and see what is really going on

Chrome / Chromium itself has several mechanism to capture all traffic.


**Keep in mind that:**
* Chrome will use your "system proxy settings". (Default)


#### Options we have are:

* `chrome://net-export/` and `chrome://net-internals/#events` (show what Chrome is actually using)
* Via [PAC file](https://bugs.chromium.org/p/chromium/issues/detail?id=839566&q=pac&colspec=ID%20Pri%20M%20Stars%20ReleaseBlock%20Component%20Status%20Owner%20Summary%20OS%20Modified) e.g. `"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --proxy-pac-url="http://my-custom-pac/wpad.dat"` needs [#network-service](chrome://flags/#network-service) since Chrome 72+
* Third party Chrome extension
* Per-profile user settings or Chrome Policy


### Overriding system proxy settings

Old flags you could use are:

```
--no-proxy-server
--proxy-auto-detect
--proxy-bypass-list=XXX
--proxy-pac-url=XXX
--proxy-server=XXX
```

See [here](https://www.chromium.org/developers/design-documents/network-stack/debugging-net-proxy) for more information, keep in mind that since Chrome 72 you need additional [workarounds](https://bugs.chromium.org/p/chromium/issues/detail?id=839566&q=pac&colspec=ID%20Pri%20M%20Stars%20ReleaseBlock%20Component%20Status%20Owner%20Summary%20OS%20Modified) to re-enable the ability to load PAC files from a URL.


### Inspecting Queries

Using `chrome://net-export/` is pretty ugly because there is no interface. I suggest you use Wireshark.


Filters you can use: `dns.qry.name matches "^Google"` (captches all DNS queries with "Google" in it, _you get the idea_). The captured URL's are typically base64 encoded, this means you have to use "tshark" a "CLI version of Wireshark" (_technical incorrect but whatever_).


### Exporting the filtered findings

We can use e.g. `tshark -r whatever_youcaptured.pcapng | awk -F' A ' '{print $2}' | sort -u`. To remove the mentioned encoding we can for example use `$ for b64 in $(tshark -r whatever_youcaptured.pcapng | awk -F' A ' '{print $2}' | sort -u | awk -F'.' '{print $4}' | sort -u);do echo $b64 && echo $b64 | base64 -d 2>/dev/null;echo;done`

The example output will then look like:

```
aH40cHM6L554543hdGUzzz5z656h6Bpcy5jb20v
https://update.googleapis.com/
aH40cHM6L554543hd43434443436hhhbgdeb23v
https://ssl.gstatic.com/
....
```