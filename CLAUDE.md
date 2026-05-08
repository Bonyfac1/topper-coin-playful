# Project rules

- All code, file names, variable names, and comments must be in English.
- All user-facing text (titles, labels, descriptions, UI copy) must be in English.
- No Czech language anywhere in the project.

## Project context

This is a **second design** for Topper Coin (TPC), running in parallel to the
original site at `~/my-first-project/` (deployed to topperharleycoin.com).

- This variant lives at **aces.name** (Forpsi hosting, FTP user `www.aces.name`).
- Visual direction: playful meme coin — sunset orange + sky blue + cream palette,
  glossy 3D cartoon mascot (Topper Harley pilot), Fredoka font, big emojis.
- Backend (history.php, holders.php) is a **copy** of the original site's
  proxies — both projects can evolve their backends independently.
- Live data is identical to the original (Atmos GraphQL + Supra RPC); only the
  visual layer differs.

## Files

- `index.html` — single-page site with all CSS/JS inline.
- `history.php` — proxy for Atmos OHLC history (called from JS).
- `holders.php` — proxy for Suprascan holder count.
- `assets/logo.png` — round logo mark (favicon + nav).
- `assets/mascot.webp` — Topper Harley pilot mascot still (poster + fallback, ~82 KB).
- `assets/mascot.mp4` — animated hero loop with audio (~890 KB, H.264 CRF 28). Plays muted+looped on hero; the audio track stays in the file for off-site sharing (X, Telegram).
- `deploy.sh` — uploads index.html, PHP proxies, and assets via FTP.
- `.ftp-credentials.example` — template; copy to `.ftp-credentials` and fill.
