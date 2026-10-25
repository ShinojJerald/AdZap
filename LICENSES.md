# Licences and attribution

## Filter lists: EasyList and EasyPrivacy

AdZap's blocking rules are compiled from **EasyList** and **EasyPrivacy**.

- Source: The EasyList authors (https://easylist.to/)
- Licence: the EasyList repository is dual licensed under the
  **GNU General Public License version 3** (or any later version) and the
  **Creative Commons Attribution-ShareAlike 3.0 Unported** licence (or any
  later version). You may use or modify the material under either licence.
  - GPL-3.0: https://www.gnu.org/licenses/gpl-3.0.html
  - CC BY-SA 3.0: https://creativecommons.org/licenses/by-sa/3.0/

Files in the AdZap package that contain material derived from these lists:

| File | What it holds |
| --- | --- |
| `rulesets/ads.json` | Network blocking rules compiled from EasyList |
| `rulesets/privacy.json` | Network blocking rules compiled from EasyPrivacy |
| `data/cosmetic-generic.css`, `data/cosmetic-map.json` | Element-hiding selectors compiled in the same filter-list build |

These derived files are distributed under the same terms as their source
lists. Rules were converted to Chrome's declarativeNetRequest format;
rules that Chrome cannot load were left out or split into equivalent rules.

## AdZap

AdZap's own code (`background/`, `popup/`, `manifest.json`) and its icons
are by Shinoj Jerald.
