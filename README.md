
# Pabs Picks — Version 1 (Owner Dashboard)

**Theme:** Dark Sportsbook (Electric Blue)  
**Tagline:** No BS. No Fluff. Just Winners.  
**Build:** Static multi-page site for GitHub Pages (private owner dashboard)

---

## What you received
A ZIP with a ready-to-upload folder containing:
- `index.html` — Keycode login page (requires code each visit)
- `dashboard.html` — Today + Yesterday slips (reads from `data/picks.json`)
- `history.html` — Shows past picks & results
- `settings.html` — Info and small configuration details (shows current keycode)
- `styles.css` — Site styling
- `config.js` — Contains the secure keycode (change this file to update key)
- `data/picks.json` — Where the picks live (edit this to update what displays)
- `README.md` — This file

**Default access key:** Px8!B29  (Change in `config.js` before publishing.)

---

## How to use — Step-by-step (Quick start)

### Option A — Quick local preview (no hosting)
1. Unzip the package.  
2. Open `index.html` in your browser. (Double-clicking the file will work for basic preview.)  
3. Enter the default key **Px8!B29** to reach the dashboard. (You chose "require every visit", so you'll need the key each time.)

> Note: Some browsers restrict `fetch()` on local `file://` URLs for JSON. If today's picks do not load when opening `index.html` as a file, use a simple local server (instructions below).

### Option B — Host on GitHub Pages (free)
1. Create a new GitHub repository (private is fine) named e.g. `pabs-picks`.
2. Upload the entire folder contents to the repository root (index.html etc.).
3. In the repository settings → Pages, choose branch `main` and folder `/ (root)` then Save.
4. GitHub Pages will publish at `https://<your-username>.github.io/<repo-name>/` shortly.
5. Open the URL, go to `index.html`, and enter your key to access the dashboard.

### Option C — Edit Picks (manual)
1. Open `data/picks.json` in a text editor.
2. Replace the sample JSON with your updated picks (keep the structure). Save and re-upload to GitHub or refresh the local server to see changes.

### Option D — Edit the Keycode
1. Open `config.js` and change the `KEYCODE` value to your new secure key. Save and redeploy the files to your hosting provider.
2. The settings page shows the currently configured key (read-only on the site) for convenience.

---

## JSON structure for `data/picks.json` (example)
```json
{
  "today":[
    {
      "sport":"NBA",
      "type":"3-leg SGP",
      "legs":["Player A 20+","Player B 10+","Team ML"],
      "odds":"+850",
      "confidence":42,
      "result":null
    }
  ],
  "yesterday":[
    {
      "sport":"NFL",
      "type":"2-leg Parlay",
      "legs":["Team X ML","Player Y TDs 1+"],
      "odds":"+720",
      "confidence":38,
      "result":"W"
    }
  ],
  "past":[
    {
      "date":"2025-11-06",
      "pick":{
         "sport":"NBA","type":"4-leg","legs":["..."],"odds":"+1200","confidence":22,"result":"L"
      }
    }
  ]
}
```

---

## Optional: Serve locally with a simple server (recommended)
If you want to preview the site locally and ensure the picks JSON loads correctly, run a simple HTTP server:

**Python 3** (in the unzipped folder):
```
python3 -m http.server 8000
```
Then open `http://localhost:8000/index.html` in your browser.

---

## Next upgrades I can help with
- Google Sheets → JSON automation so picks update automatically.  
- Add ChatGPT / Pabs Picker AI integration to auto-generate picks.  
- Add a small backend so keycode can be changed via the site.  
- Add user auth & subscription (if you want to go public).

---

If you want, I can now produce the downloadable ZIP with the full site. The files are created in the build and will be zipped next.
