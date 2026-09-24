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

**`index.html` is a placeholder.** A landing page with a video tour replaces it after TestFlight.
`privacy.html`, `terms.html` and `support.html` must keep their names and stay at the root:
App Store Connect links to them (privacy policy URL, support URL; the marketing URL is the root).
Shared styling is in `style.css`; a new landing page can use its own without touching theirs.
