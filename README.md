# travelstats-site

The website for **Travel: Stats tracker**, a travel logbook for iPhone. Four static pages, no build
step, no dependencies:

| | |
|---|---|
| `index.html` | the landing page: the app, the App Store link and a video tour |
| `privacy.html` | the privacy policy — **required by App Store Connect** |
| `support.html` | the support page — **required by App Store Connect** |
| `terms.html` | the terms of use |

Served by GitHub Pages from `main`, at the root. Editing a file and pushing publishes it.

The look is the app's default *Night* palette (`#121211`, amber `#F2B233`) in Geist, self-hosted
from `fonts/` (SIL Open Font License, `fonts/Geist-OFL.txt`) so the page makes no third-party
requests. A light variant follows the reader's system setting.

**The privacy page describes what the app does**, checked against its code and
`PrivacyInfo.xcprivacy`: the app changes first, and this page in the same release.

**The video tour** (`demo/landing-tour.mp4`, `demo/poster.jpg`, `demo/share.jpg`) is filmed and
published from the app repo, never edited here: `docs/demo/landing-tour.json` there holds the five
sections, their launch arguments and their words, and

```sh
TravelStats/Tools/demo/record-demo.sh                 # in ~/Development/travelstats
python3 TravelStats/Tools/demo/publish-demo.py        # copies the film and stills here
```

rewrites the `#demo-timeline` block and the `<noscript>` list in `index.html`, which the panels
and ticks beside the phone are read from. Then commit and push here. It shows the user's real data
(the TEST ONLY johannes seed), at his request.

`privacy.html`, `terms.html` and `support.html` must keep their names and stay at the root:
App Store Connect links to them (privacy policy URL, support URL; the marketing URL is the root).
Shared styling is in `style.css`; `index.html` carries its own sheet, so it never touches theirs.
