# Mission Control — WNF Operating Atlas

Living operating atlas for Wenatchee Natural Foods (Market + Café), INVERT Inc, and Tao Capital. Single-file HTML, fully interactive, mobile/tablet/desktop responsive, edit-in-browser with localStorage persistence and HTML/JSON export.

Live at: **https://joshualparrish.github.io/wnf-atlas/**

---

## What's in this folder

- **`index.html`** — the atlas itself. This is what GitHub Pages serves. All data lives inside the file in `<script>` data blocks (`ENTITIES`, `PEOPLE`, `STANDARDS`, `TRIAGE`, `WEEK`, `FLOWS`, `BREAK_GLASS`).
- **`atlas-data.json`** — extracted snapshot of all data blocks. Backup / point-in-time restore / raw data for feeding other tools. **Must be regenerated whenever index.html data changes** — use Export → Download JSON from the live atlas, or it silently rots.

---

## Tier system (current)

El Jefe → Commander → Senior Operator → Ops Assistant → Squad Lead → Rogue Ranger → Signal Carrier → Rookies & Recruits. Plus External Partners and AI / Future Seats. Each person card carries an entity chip (WNF Market, WNF Café, INVERT, Tao Capital).

---

## Continuous editing workflow

The atlas has an **edit mode** built in — no manual HTML/JSON editing needed.

1. Open the live URL → click **Edit** (pencil) in the header.
2. Every card gets edit (✎) and delete (×) controls; every section gets **+ Add**.
3. Changes auto-save to that browser's `localStorage`. The header shows an **EDITED** badge when your local copy differs from the published file.

### Publishing edits back to GitHub

1. **Export → Download HTML** — downloads `operating_atlas_v2.html` with your edits baked in.
2. **Export → Download JSON** — take this backup at the same time.
3. On the repo page, drag the downloaded HTML onto the file list, rename/confirm overwrite of `index.html`, drag the JSON over `atlas-data.json`, commit. Pages redeploys in ~30 seconds.

### Restoring from a JSON backup

Export → Import JSON → pick the backup → confirm. Then Download HTML if you want to push that state to GitHub.

### When devices diverge

Each browser holds its own localStorage copy. One device at a time for live editing, or Export JSON from the edited device and Import on the other before continuing. **Export → Reset to file defaults** wipes local edits and reverts to whatever GitHub serves.

---

## Contacts vault

Phone numbers/emails are AES-GCM encrypted inside the file (`CONTACTS_BLOB`), unlocked with a shared key (ask Joshua, Sam, or Tyler). The key is cached per-tab in sessionStorage only. Unlocked contact info is **display-only**: it is stripped from localStorage saves, Export JSON, and Export HTML, so decrypted numbers can never leak into the public repo. To change vault contents or re-key, the blob must be re-encrypted and committed (done via Claude session).

---

## Privacy

The public file has no personal cells or personal emails — contact fields read "ask a manager." Safe for public/staff/future hires. Full contact details live only inside the encrypted vault and in the manager-only doc.

---

## Cross-device access

Any browser → the live URL. On iPhone/iPad: Share → Add to Home Screen for app-like access. Works offline once loaded (Google Fonts fall back cleanly).
