# Card Comparison — Install on Android

This folder is a ready-to-host web app (PWA). Host it once (free, ~5 minutes),
then install it on your phone from Chrome. After that it behaves like a normal
app: home screen icon, fullscreen, works offline, and your saved library stays
on your phone.

## Step 1 — Put it online with GitHub Pages (free)

1. Go to https://github.com and sign up (or log in).
2. Click the "+" (top right) -> "New repository".
   - Name it anything, e.g. `card-compare`
   - Set it to **Public**
   - Click "Create repository".
3. On the new repo page, click "uploading an existing file".
4. Drag ALL the files from this folder in (index.html, manifest.webmanifest,
   sw.js, and the four .png icons). Click "Commit changes".
5. Go to the repo's **Settings** tab -> **Pages** (left sidebar).
   - Under "Branch", pick `main`, folder `/ (root)`, click **Save**.
6. Wait a minute, then refresh that Pages screen — it shows your app's link,
   something like: `https://YOURNAME.github.io/card-compare/`

## Step 2 — Install it on your phone

1. Open that link in **Chrome on your Android phone**.
2. Tap the three-dot menu (top right) -> **"Add to Home screen"**
   (on newer Chrome it may say **"Install app"**).
3. Confirm. The Card Comparison icon appears on your home screen.

Done. Launch it from the icon — it opens fullscreen like a real app and works
without internet.

## Notes

- Your saved comparisons live in the app's own storage on your phone. They do
  NOT carry over automatically from the standalone HTML file you were using —
  open the old file once, use Library -> Export, then Import inside the
  installed app to move them across.
- To update the app later: upload a new index.html to the repo, and bump the
  CACHE_VERSION string at the top of sw.js (e.g. to 'cardcompare-v2') so
  phones fetch the new version.
- The share feature works even better installed, because the app runs on a
  proper https address.
- The same link installs on iPhone too: open it in Safari -> Share ->
  "Add to Home Screen".
