# BarCraft landing page

Static marketing + legal pages (privacy, support) for BarCraft. No build step — plain HTML/CSS.

## Pages
- `index.html` — home: sells private-event bartending first, with an app section
- `hire.html` — private events: services, rate card, FAQ, inquiry form
- `about.html` — bio and work history
- `app.html` — the BarCraft app
- `privacy.html` — privacy policy (store-required URL)
- `terms.html` — Terms of Use / EULA, incl. the zero-tolerance objectionable-content clause
  required for App Store Guideline 1.2 (UGC apps)
- `support.html` — support + account/data deletion (store-required URLs)

## Design
Warm paper, black Fraunces serif and Instrument Sans, with one rust accent. Every color and
font is a token in `:root` at the top of `styles.css`. `js/site.js` handles the
header, mobile menu, scroll reveals and hero parallax. Photos in `assets/events/` were re-encoded
from the originals, which strips GPS.

## Preview locally
Open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit
http://localhost:8000.

## Publish free on GitHub Pages
Push these files to a repo, then in the repo go to **Settings → Pages → Build and deployment**
and set **Source: Deploy from a branch**, picking the branch and the folder that contains these
files (root, or `/docs` if you move them there). Your URLs become:
`https://<user>.github.io/<repo>/privacy.html` and `.../support.html` — use those for the
App Store / Play Store submission. (`.nojekyll` is included so Pages serves the files as-is.)

To swap the contact email later (e.g. to `support@barcraft.social`), search-replace
`adamliscia@gmail.com` in `privacy.html` and `support.html`.
