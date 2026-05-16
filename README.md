# WNF Operating Atlas

Living operating atlas for Wenatchee Natural Foods (Market + Café), INVERT Inc, and Tao Capital. Single-file HTML, fully interactive, mobile/tablet/desktop responsive, edit-in-browser with localStorage persistence and HTML/JSON export.

**This repo is set up to publish via GitHub Pages.** Once Pages is enabled, the atlas lives at `https://<your-username>.github.io/<repo-name>/`.

---

## What's in this folder

- **`index.html`** — the atlas itself. This is what GitHub Pages serves. All data is inside the file in `<script>` data blocks (`ENTITIES`, `PEOPLE`, `STANDARDS`, `TRIAGE`, `WEEK`, `FLOWS`, `BREAK_GLASS`).
- **`atlas-data.json`** — extracted snapshot of all data blocks. Useful for backup, import into other tools, or feeding a new chat that needs the raw data.

---

## First-time setup (60 seconds)

1. Create a free GitHub account at github.com if you don't have one.
2. Create a new repo. Name it something like `wnf-atlas`. Keep it **public** (Pages is free on public repos; private Pages requires GitHub Pro at $4/mo). The atlas is sanitized of personal data, so public-but-obscure is fine.
3. Click **"uploading an existing file"** on the new repo page → drag both `index.html` and `atlas-data.json` (and this README) → commit.
4. Repo → **Settings → Pages** → under "Source" pick **Deploy from a branch** → branch **main**, folder **/ (root)** → Save.
5. Wait ~60 seconds. Pages reports the live URL at the top of the Pages settings page. That's your atlas.

---

## Continuous editing workflow

The atlas has an **edit mode** built in — you don't need to touch HTML or JSON manually.

### Quick edits (from any device)

1. Open your GitHub Pages URL.
2. Click the **Edit** (pencil) button in the header → body gets edit mode.
3. Every card now has an **edit (pencil)** and **delete (×)** in the corner. Every section has an **"+ Add"** button.
4. Click edit → drawer opens with form fields → make changes → **Save**. Changes auto-save to your browser's `localStorage`. The header shows an **EDITED** badge so you know your local copy differs from the published version.

### Publishing your edits back to GitHub

1. Click the **Export** button in the header → **Download HTML**. The atlas downloads a fresh `operating_atlas_v2.html` with all your edits baked into the data blocks.
2. Go to your GitHub repo → click `index.html` → click the pencil (edit) icon → delete the existing content → paste the new file's contents → "Commit changes."

   *(Faster path: drag the downloaded HTML onto the repo's file list → confirm overwrite → commit.)*

3. GitHub Pages redeploys in ~30 seconds. Refresh the page anywhere and your edits are live.

### Backup before each redeploy

Click **Export → Download JSON** before redeploying. Save the JSON file somewhere safe (Drive, Dropbox, iCloud). That's your point-in-time snapshot.

### Restoring from a JSON backup

Open the atlas → **Export → Import JSON** → pick the backup file → confirm. All data is replaced. Then **Export → Download HTML** if you want to push that state back to GitHub.

---

## Cross-device access notes

- **Mac, PC:** any browser → your Pages URL.
- **iPhone, iPad:** Safari or Chrome → your Pages URL. Add to Home Screen for app-like access (tap Share → Add to Home Screen).
- **Offline:** Once the page is loaded, it works without internet (except for the Google Fonts, which fall back to system fonts cleanly). Saving the file to Files.app on iOS or to Documents on macOS gives you an offline copy.

---

## When edits get out of sync

Each browser (and each device) holds its own `localStorage` copy. If you edit on your phone and your desktop separately, they'll diverge. The cleanest discipline:

- One device at a time for live editing, OR
- Export JSON from the device you edited on, Import JSON on the other device before continuing.

If you ever want to wipe local edits and revert to whatever's in `index.html` on GitHub: open atlas → **Export → Reset to file defaults** → confirm. That clears localStorage and reloads.

---

## What was stripped from the atlas (privacy notes)

This version has no personal cell phones, no personal emails, no "saved in Joshua's phone as X" notes. Anywhere contact info used to live, the field reads "Ask a manager for contact info." Safe to share with public, existing staff, or future hires.

For full contact details (staff cells, vendor rep cells, etc.), keep a **separate, manager-only** doc — recommended location: a Notion page restricted to Tier-1 manager access.

---

## File on Joshua's Mac

The local working source lives at:
`/Users/joshuaparrish/Documents/Claude/Projects/WNF/operating_atlas_v2.html`

A pre-sanitized backup (KEEP PRIVATE) lives at:
`/Users/joshuaparrish/Documents/Claude/Projects/WNF/operating_atlas_v2.BACKUP_with_personal_data.html`
