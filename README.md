# travelstats-site

The website for **Travel: Stats tracker**, a travel logbook for iPhone. Four static pages, no build
step, no dependencies:

| | |
|---|---|
| `index.html` | what the app is, in one line |
| `privacy.html` | the privacy policy — **required by App Store Connect** |
| `support.html` | the support page — **required by App Store Connect** |
| `terms.html` | the terms of use |

Served by GitHub Pages from `main`, at the root. Editing a file and pushing publishes it.

The look is the app's default *Night* palette (`#121211`, amber `#F2B233`) in Geist, self-hosted
from `fonts/` (SIL Open Font License, `fonts/Geist-OFL.txt`) so the page makes no third-party
requests. A light variant follows the reader's system setting.

**The privacy page describes what the app does**, checked against its code and
`PrivacyInfo.xcprivacy`: the app changes first, and this page in the same release.
