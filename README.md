<p align="center">
  <a href="https://tunekadal.com/software/adzap/">
    <img src="assets/adzap.svg" alt="AdZap — Choose the sites. Zap the ads. A Chrome extension that blocks ads and trackers only on the websites you pick." width="100%" />
  </a>
</p>

<h1 align="center">AdZap</h1>

<p align="center">
  <b>Choose the sites. Zap the ads.</b><br />
  A Chrome extension that blocks ads and trackers only on the websites you pick.<br />
  Every site you haven't zapped stays exactly as it was.
</p>

<p align="center">
  <a href="https://github.com/ShinojJerald/AdZap/releases/latest"><b>Download AdZap 1.1.0</b></a> &nbsp;·&nbsp;
  <a href="https://tunekadal.com/software/adzap/">Product page</a> &nbsp;·&nbsp;
  <a href="https://github.com/ShinojJerald/AdZap/issues">Report an issue</a>
</p>

<p align="center"><sub>Google Chrome 116 or later · Free · Version 1.1.0 · Not in the Chrome Web Store</sub></p>

This repository holds AdZap's releases and documentation.

## How it works

AdZap starts switched off. Nothing is filtered until you choose a site.

1. **Open a site** whose ads or trackers you want gone.
2. **Zap it.** Click the AdZap bolt in Chrome's toolbar and press **ZAP ADS**. The page reloads with blocking on for that site.
3. **Undo any time.** Press **Unzap this site** in the same menu, or <kbd>Alt</kbd>+<kbd>Z</kbd>, and the site goes back to normal.

Zapping `example.com` also covers its subdomains, such as `news.example.com`. Zapping `news.example.com` covers only that subdomain.

## What it blocks

On a zapped site, Chrome applies AdZap's rule lists with its built-in blocking engine (declarativeNetRequest).

| List | Rules | What it covers |
| --- | ---: | --- |
| Ads | 57,323 | Ad requests, compiled from EasyList |
| Trackers | 56,296 | Tracking and analytics requests, compiled from EasyPrivacy |
| Annoyances | 51 | Common share buttons, live-chat widgets, and push-notification and newsletter pop-up scripts |

AdZap also hides leftover ad slots and banners on zapped pages with element-hiding styles. The toolbar badge counts blocked requests on the current tab, and the menu shows blocked here, all time and the last 7 days.

## Install

AdZap isn't listed in the Chrome Web Store, so it's installed as an unpacked extension.

1. Download `adzap-1.1.0.zip` from the [latest release](https://github.com/ShinojJerald/AdZap/releases/latest).
2. Extract it to a folder you'll keep, such as `Documents\AdZap`. Chrome runs AdZap from that folder, so don't delete or move it.
3. Open `chrome://extensions` in Chrome.
4. Turn on **Developer mode** (top-right corner).
5. Click **Load unpacked** and choose the folder that contains `manifest.json`.
6. Pin AdZap from the puzzle-piece menu so the bolt stays in the toolbar.

### Check your download

In PowerShell, in the folder with the ZIP:

```powershell
Get-FileHash .\adzap-1.1.0.zip
```

On a Mac or Linux: `shasum -a 256 adzap-1.1.0.zip`. The SHA-256 hash should be:

```
381378495486f0488b6ee1465b33fd96049a1216069cbb2778b9c9076631aa56
```

It's also listed in `adzap-1.1.0-SHA256SUMS.txt` on the release.

### Update or remove

- **Update:** replace the files in your AdZap folder with the new version, then press reload on AdZap's card in `chrome://extensions`. AdZap doesn't update itself.
- **Remove:** press **Remove** on AdZap's card in `chrome://extensions`. Chrome deletes AdZap's saved list and counts with it.

## Privacy

- **What it sends:** AdZap's own code makes no network requests. It only loads files that come inside the extension. There's no account, no analytics and no AdZap server.
- **What it keeps, in Chrome on your computer:** the sites you've zapped (with the date you zapped each one); blocked-request counts (an all-time total and one for each of the last 30 days, numbers only); per-tab counts and the site each tab is showing, cleared when Chrome closes; and whether its rule lists turned on correctly.

### Permissions

| Permission | Why AdZap needs it |
| --- | --- |
| `declarativeNetRequest` | Block requests on zapped sites with Chrome's built-in engine |
| `declarativeNetRequestFeedback` | Count exactly which requests its own rules blocked (unpacked installs) |
| `storage` | Keep your list of zapped sites and the block counts |
| `webNavigation` | Apply the hiding styles as zapped pages load |
| `webRequest` | Count blocked requests |
| `scripting` | Insert the hiding styles into zapped pages |
| `tabs` | Show the badge count and reload a page after you zap or unzap it |
| Access to all sites | Work on whichever site you zap. On sites you haven't zapped, an allow rule keeps every request unblocked. |

## Limitations

- **Not every ad.** Filter lists can't catch every ad, and some sites, including YouTube, keep changing how they deliver ads. AdZap can't promise a page with no ads.
- **Sometimes too much.** The general lists can block something a site needs. In testing, a zapped youtube.com had a connectivity check blocked. If a zapped site misbehaves, unzap it.
- **Chat and sign-up widgets.** The annoyance rules block common live-chat, newsletter and notification scripts, so those may not appear on zapped sites.
- **Hidden elements can return.** Pages that keep rebuilding themselves may put back some of the elements AdZap hides.
- **Chrome only, so far.** Built for Google Chrome 116 or later and tested in Chromium. Edge, Brave and Opera haven't been tested; Firefox, Safari and phone browsers aren't supported.
- **Manual updates.** Unpacked extensions don't update automatically.
- **Some pages can't be zapped:** Chrome's own pages, and one-word addresses such as `localhost`.

## Report a problem

[Open an issue](https://github.com/ShinojJerald/AdZap/issues) with your Chrome version, the site and what happened.

## Licences

AdZap's blocking rules are compiled from EasyList and EasyPrivacy by [the EasyList authors](https://easylist.to/), used under GPL-3.0 or CC BY-SA 3.0. See [LICENSES.md](LICENSES.md).

Made by [Shinoj Jerald](https://github.com/ShinojJerald).
