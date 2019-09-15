### Google Chrome Incognito Mode Shortcut(s)

Chrome allows you to directly open new sessions/windows in a private (incognito) mode. See [here](https://support.google.com/chrome/answer/95464) and [here](https://support.google.com/chrome/answer/7440301) for more details.

**Create a Incognito Window that opens Windows in a new private session**

Right-click or tap and hold on your desktop, and then press/click "New", and click or tap on "Shortcut". 

- On x86 systems the shortcut is: `"%ProgramFiles%\Google\Chrome\Application\chrome.exe" -incognito`
- On x64 systems the shortcut is: `"%ProgramFiles(x86)%\Google\Chrome\Application\chrome.exe" -incognito`

**Create a Incognito Window that always opens new Windows in a new private session**

- On x86 systems the shortcut is: `"%ProgramFiles%\Google\Chrome\Application\chrome.exe" -incognito -new-window`
- On x64 systems the shortcut is: `"%ProgramFiles(x86)%\Google\Chrome\Application\chrome.exe" -incognito -new-window`

There are additional parameters you can add, for example the website you like to open e.g. `-incognito https://github.com/CHEF-KOCH/Chromium-hardening` or `-new-window incognito https://github.com/CHEF-KOCH/Chromium-hardening`.


### Adjust all settings and advanced settings under `chrome://settings` manually

* Do not save passwords in your browser (Prefer a free and open-source password manager like e.g. KeePass).
* Disable all options in the "Privacy" section because most of them use an external Google service. Example: Google Safe Browsing about phishing and malware protection (chrome://settings → [Show advanced settings...] → Privacy)
* Block third-party cookies and site data (chrome://settings/content → Cookies)
* Ask first before allowing sites to run Flash (chrome://settings/content → Flash)
* Ask when a site tries to track your physical location (chrome://settings/content → Location)
* Check the flags mentioned in this project, make sure you set them according to the documentation.


#### Optional
* Do not login (GAIA) with a Google account btw who says Mozilla sync is more secure (they use Amazon).


### Search Engine & Search Operators

The integrated search engine in Chrome is "diffcult to handle" which means adding a new search provider is _difficult_ to some users. There are also "secret" commands (operators) which you can add to the search URL to "improve" the results you get. Here is an example on how to change/improve your search results and how to deal with operators. This is of course only an example different search providers might have different operators! I used Google here because that's the default search result provider in Chrome. 

* Go into your Chrome settings and open the "search provider section" or simply type in: `Chrome://settings/searchengines` 
* Add a search engine with a name of your choice. Using a keyword is also possible, you can use whatever you want as keyword. e.g. xy.
* Add the URL: `https://www.google.net/search?as_q=%s&as_epq=&as_oq=&as_eq=&as_nlo=&as_nhi=&lr=&cr=&as_qdr=y` (this is only an example)
* You see that there are a lot parameters added "&as_param=" etc. This can be tweaked, the easiest way is to go to `https://www.google.com/advanced_search` and copy the URL which does what you want. I do not list [all parameters](https://ahrefs.com/blog/google-advanced-search-operators/) here because they are maybe still in [beta](https://searchengineland.com/search-google-by-date-with-new-before-and-after-search-commands-315184). 
