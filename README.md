# Weigh In

Personal weight, waist, protein and gym tracker. Runs as a home screen web app on iPhone. All data stays in the phone's browser storage, nothing is sent anywhere, so this repo only ever holds code.

## Test on the PC

```
cd "D:\Programs\Weight Loss App"
python -m http.server 8000
```

Open http://localhost:8000 in a browser. Data saved here is separate from the phone.

## Put it online (GitHub Pages)

1. Create a new **public** repo on GitHub called `weigh-in` (free Pages needs public, which is fine since there's no data in it).
2. Upload every file in this folder (Add file → Upload files → Commit).
3. Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)` → Save.
4. After a minute it's live at `https://<your-username>.github.io/weigh-in/`.

## Install on the iPhone

1. Open that address in **Safari**.
2. Share → **Add to Home Screen** → Add.
3. Open it from the new icon (not from Safari, they have separate storage).
4. Settings (gear on Today): set height and Wegovy start, paste the Weight Log table into Import, then **Back up now**.

## Updating

1. Change the files and upload them to the repo again.
2. In `sw.js`, bump `VERSION` (`'v1'` → `'v2'`). Without this the phone keeps the old cached copy.
3. On the phone, close the app fully and reopen it, twice if the change doesn't show.

## Don't lose data

- Back up after weigh-ins (the app nudges you). Save the backup to Files or iCloud Drive.
- Deleting the home screen icon deletes the data with it.
- Data belongs to the exact web address. Renaming the repo or moving hosts means an empty app, so back up first and restore after.
