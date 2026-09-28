# RBI Daily

A small study tracker I built for RBI Grade B prep. It's one HTML file, no build step and no server, so it runs fine on GitHub Pages.

You get a daily vote with a streak, a focus timer that logs your minutes, checklists for Phase 1, Phase 2 and the interview, a library for PDFs and notes, and a progress page with mock scores.

## Files

- `index.html` is the whole app
- `sw.js` caches it so it opens offline
- `manifest.webmanifest` and the three png files are for the Home Screen icon

## Putting it online

1. Make a repo and upload all six files to the root.
2. Settings > Pages > deploy from the `main` branch, `/ (root)`.
3. Open the Pages link in Safari, tap Share, then Add to Home Screen.

## Updating

Upload the new `index.html` over the old one. The page is fetched from the network first, so the change shows up the next time you open it. If the phone still shows the old look, close the app fully and reopen it once or twice.

## Where your data lives

Progress, streaks and scores are in the browser's localStorage. Files from the Library are in IndexedDB. Both stay on the device, and clearing Safari's website data deletes both.

Progress > Copy data gives you a backup of the first kind. It doesn't include library files, so keep your originals somewhere else.

## Not included

No push notifications. Those need a server or a native app.
