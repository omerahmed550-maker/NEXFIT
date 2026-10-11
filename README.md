# NEX FIT

Personal fitness and nutrition tracker. Plain HTML/CSS/JS, no build step, no backend, no accounts.
All data stays on your device (IndexedDB). Works offline once installed.

## Files
- index.html: the whole app (HTML, CSS and JS in one file)
- sw.js: service worker that caches the app so it opens offline
- manifest.webmanifest, icon-180/192/512.png: install metadata and icons

## Put it online (free, about 5 minutes)
The app must be served over HTTPS for the service worker and "Add to Home Screen" to work.
1. Create a free GitHub account and a new public repository (for example `nexfit`).
2. Upload all 7 files from this folder to the repository root.
3. Repository Settings, Pages, Source: "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
4. After a minute your app is at `https://YOUR-NAME.github.io/nexfit/`.
(Netlify Drop or Cloudflare Pages also work: drag the folder in.)
Your workout and food data is never uploaded; hosting only serves the app files.

## Install on iPhone and enable offline
1. Open your HTTPS address in **Safari** (not an in-app browser).
2. Wait for it to load fully while online, then reload once so the offline cache finishes.
3. Tap Share, then **Add to Home Screen**, then Add.
4. Open NEX FIT from the new home screen icon. Settings, About should say "Ready" under Offline.
5. Test it: turn on Airplane Mode, open the app, log something.
Always open it from the home screen icon. Data saved in Safari and in the home-screen app is stored separately on iOS, so pick one and stay with it (use the home-screen app, and restore a backup there if you tested in Safari first).

## Keep and restore your data
- Settings, Export backup: downloads `nexfit-backup-DATE.json`. Choose to include photos or not.
- If the download does nothing, use Copy to clipboard and paste the text into Notes.
- Settings, Restore backup: pick the file or paste the text. It is validated first, nothing changes if it is invalid, and you confirm before it overwrites.
- Export weekly and keep the file in iCloud Drive or email it to yourself. iOS can clear web storage for sites you have not opened in a long while, and deleting the app icon deletes its data.

## Limits
- No built-in food database (it would need a network and licence). Create foods from package labels; they are saved and searchable.
- Rest-timer sound and vibration only work while the app is open on screen. iOS does not allow a closed web app to ring.
- Installed-app notifications need iOS 16.4+ and are not used by default.
- Estimated 1RM uses the Epley formula and is a rough guide.
