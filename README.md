# Golf Swing & Shot Tracer web

Standalone static landing and legal pages for the Android app
`com.cukkacreatives.golf.shot.swing.trace`. All public content is in English.
No build step, npm dependencies, backend, or secrets are required.

## Files

- `index.html`: app landing page and Google Play link.
- `privacy-policy.html`: privacy, permissions, external services, and data deletion (`#data-deletion`).
- `terms-of-use.html`: terms and accuracy limitations.
- `styles.css`: shared responsive components, colors, typography, and shape tokens.
- `logo.svg`: web vector of the existing Android adaptive launcher artwork.
- `hero.png`: existing app home artwork.
- `app-ads.txt`: publisher record copied from the SkinScanner web project.
- `.nojekyll`: serves these files directly through GitHub Pages.

## Publish to a separate public GitHub repository

Copy the **contents** of this folder, including `.nojekyll`, to the root of
the public website repository. In repository Settings → Pages, use the
publishing branch and its root folder. Keep the relative file structure.
See [GitHub Pages setup](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

For a project site, public paths are:

- `https://durdenk.github.io/golf-shot-tracer-web/`
- `https://durdenk.github.io/golf-shot-tracer-web/privacy-policy.html`
- `https://durdenk.github.io/golf-shot-tracer-web/privacy-policy.html#data-deletion`
- `https://durdenk.github.io/golf-shot-tracer-web/terms-of-use.html`

Public website repository: https://github.com/durdenk/golf-shot-tracer-web

Private Android repository: https://github.com/durdenk/golf-shot-tracer

`GolfExternalLinks.kt` defines the same destinations for both Settings and Premium.

For advertising verification, make sure `app-ads.txt` is reachable at the
root path of the developer website hostname (for example,
`https://<owner>.github.io/app-ads.txt` or `https://<custom-domain>/app-ads.txt`).
A project repository's subpath alone is not a hostname-root deployment.
See [AdMob app-ads.txt setup](https://support.google.com/admob/answer/9363762?hl=en).

## Project details

- App name and package match `assets/features/store-listing/04-10-2026/app-listing.txt`.
- The palette follows the Android app's `ui/theme/Color.kt`.
- Contact: `cukkacreatives@gmail.com`, reused from the reference project's privacy contact.
- `app-ads.txt` reuses publisher `pub-6793071222149082` from the reference project; use it only if Golf uses the same AdMob publisher account.
- The Play link uses the app's package ID; availability has not been confirmed.
- The policies describe the current source: on-device videos, local data, Google Maps/location, Open Topo Data coordinates, Android backup, Google Play subscriptions (purchase/restore/acknowledgement), and Firebase Analytics usage events. Advertising ID collection and ad personalization signals are disabled. No advertising SDK is integrated.
- The live privacy and terms URLs returned HTTP 200 on October 5, 2026. The live privacy copy still describes the earlier version without Firebase Analytics. Publish the updated local legal files to the public repository before distributing this release; this code change does not publish the website.

## Local preview

From this folder, run:

```powershell
python -m http.server 8765 --bind 127.0.0.1
```

Then visit `http://127.0.0.1:8765/`. You can also open `index.html`
directly in a browser. Check the landing and legal pages at desktop and mobile widths.
