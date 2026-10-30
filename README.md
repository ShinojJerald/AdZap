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
  <a href="https://chromewebstore.google.com/detail/pjbchfbicicekcgoaakdephmgkfmddga"><b>Add to Chrome</b></a> &nbsp;·&nbsp;
  <a href="https://tunekadal.com/software/adzap/">Product page</a> &nbsp;·&nbsp;
  <a href="https://github.com/ShinojJerald/AdZap/issues">Report an issue</a> &nbsp;·&nbsp;
  <a href="https://buymeacoffee.com/tunekadal">Buy me a coffee</a>
</p>

<p align="center"><sub>Google Chrome 116 or later · Free · Version 1.3.0 · In the Chrome Web Store as "AdZap: Per-Site Ad Blocker"</sub></p>

This repository holds AdZap's documentation and is the place to report issues. Install AdZap from the [Chrome Web Store](https://chromewebstore.google.com/detail/pjbchfbicicekcgoaakdephmgkfmddga).

## How it works

AdZap starts switched off. Nothing is filtered until you choose a site.

1. **Open a site** whose ads or trackers you want gone.
2. **Zap it.** Click the AdZap bolt in Chrome's toolbar and press **ZAP ADS**. The page reloads with blocking on for that site, and the button shows **ZAPPED ✓**.
3. **Undo any time.** Press **Unzap this site** in the same menu, or <kbd>Alt</kbd>+<kbd>Z</kbd>, and the site goes back to normal.

Zapping `example.com` also covers its subdomains, such as `news.example.com`. Zapping `news.example.com` covers only that subdomain.

The bottom of the menu has links to this page on GitHub, **Share** (copy the link, or share it on X, WhatsApp or by email), **Buy me a coffee** and **Report a problem**, and shows the version you have.

## What it blocks

On a zapped site, Chrome applies AdZap's rule lists with its built-in blocking engine (declarativeNetRequest).

| List | Rules | What it covers |
| --- | ---: | --- |
| Ads | 57,323 | Ad requests, compiled from EasyList |
| Trackers | 56,296 | Tracking and analytics requests, compiled from EasyPrivacy |
| Annoyances | 51 | Common share buttons, live-chat widgets, and push-notification and newsletter pop-up scripts |

AdZap also hides leftover ad slots and banners on zapped pages with element-hiding styles. The toolbar badge shows an estimate of the requests blocked on the current tab, and the menu shows blocked here, all time and the last 7 days, marked "est."

## Install

AdZap is in the Chrome Web Store, published by TuneKadal.

1. Open [AdZap in the Chrome Web Store](https://chromewebstore.google.com/detail/pjbchfbicicekcgoaakdephmgkfmddga) in Google Chrome on your computer.
2. Click **Add to Chrome**, then **Add extension** when Chrome asks.
3. Pin AdZap from the puzzle-piece menu so the bolt stays in the toolbar.

### Update or remove

- **Update:** Chrome keeps AdZap up to date automatically.
- **Remove:** right-click the AdZap bolt and choose **Remove from Chrome**, or press **Remove** on its card in `chrome://extensions`. Chrome deletes AdZap's saved list and counts with it.

### Installed it from GitHub before?

The Chrome Web Store version is a separate copy of AdZap, so your zapped sites don't move across. Add it from the store, zap your sites again, then remove the old copy: press **Remove** on its card in `chrome://extensions`.

## Privacy

- **What it sends:** AdZap's own code makes no network requests. It only loads files that come inside the extension. There's no account, no analytics and no AdZap server. The links at the bottom of the menu (GitHub, Share, Buy me a coffee, Report a problem) open only when you click them. **Report a problem** starts an email in your mail app with your AdZap version and the current site filled in, so you can see what you're sending before you send it.
- **What it keeps, in Chrome on your computer:** the sites you've zapped (with the date you zapped each one); blocked-request counts (an all-time total and one for each of the last 30 days, numbers only); per-tab counts and the site each tab is showing, cleared when Chrome closes; and whether its rule lists turned on correctly.

### Permissions

| Permission | Why AdZap needs it |
| --- | --- |
| `declarativeNetRequest` | Block requests on zapped sites with Chrome's built-in engine |
| `storage` | Keep your list of zapped sites and the block counts |
| `webNavigation` | Apply the hiding styles as zapped pages load |
| `webRequest` | Count blocked requests |
| `scripting` | Insert the hiding styles into zapped pages |
| Access to all sites | Work on whichever site you zap. On sites you haven't zapped, an allow rule keeps every request unblocked. |

## Limitations

- **Not every ad.** Filter lists can't catch every ad, and some sites, including YouTube, keep changing how they deliver ads. AdZap can't promise a page with no ads.
- **Sometimes too much.** The general lists can block something a site needs. In testing, a zapped youtube.com had a connectivity check blocked. If a zapped site misbehaves, unzap it.
- **Chat and sign-up widgets.** The annoyance rules block common live-chat, newsletter and notification scripts, so those may not appear on zapped sites.
- **Hidden elements can return.** Pages that keep rebuilding themselves may put back some of the elements AdZap hides.
- **Chrome only, so far.** Built for Google Chrome 116 or later and tested in Chromium. Edge, Brave and Opera haven't been tested; Firefox, Safari and phone browsers aren't supported.
- **Some pages can't be zapped:** Chrome's own pages, and one-word addresses such as `localhost`.

## Report a problem

Press **Report a problem** in AdZap's menu, or email [hello@tunekadal.com](mailto:hello@tunekadal.com). You can also [open an issue](https://github.com/ShinojJerald/AdZap/issues). Include your Chrome version, the site and what happened.

## Support AdZap

AdZap is free. If it's useful to you, you can [buy me a coffee](https://buymeacoffee.com/tunekadal).

## Licences

AdZap's blocking rules are compiled from EasyList and EasyPrivacy by [the EasyList authors](https://easylist.to/), used under GPL-3.0 or CC BY-SA 3.0. See [LICENSES.md](LICENSES.md).

Made by [TuneKadal](https://tunekadal.com/). © 2026 TuneKadal. All rights reserved.
