# Primiero Family Guide (PWA)

A single installable app for the Dolomites trip — works offline once installed, no server needed for the content itself.

## Files
- `index.html` — the app (Home / Attività-Activities / Escursioni-Hikes / Pratico-Practical)
- `manifest.json` — install metadata
- `sw.js` — offline caching
- `icon-192.png`, `icon-512.png` — home screen icons
- `hero.jpg` — the Brunet Resort photo shown on the Home tab

## Host it (GitHub Pages — the method that's worked for you before)
1. Go to github.com, sign in
2. **+** → **New repository** → name it e.g. `primiero-guide`
3. **Add file → Upload files** → drag in all 6 files above → **Commit changes**
4. **Settings → Pages → Source: Deploy from a branch → main → / (root) → Save**
5. Wait ~2 minutes, then your guide is live at `https://[yourusername].github.io/primiero-guide/`

## Install on your phone
Open that URL in Chrome (Android) or Safari (iOS) → **Add to Home Screen** / install banner → it opens full-screen like a real app from then on.

## What's inside
- **IT/EN toggle** — top right of the header, switches every label and card instantly, remembered on your phone
- **Home** — hero photo of Brunet Resort, hotel link, weather link, a menu link (add yours — see below), and the ear/altitude caution pinned at the top
- **Attività** — all the activity ideas, with a checkmark to mark things off as you go (saved on your phone only)
- **Escursioni** — the hikes, same check-off system
- **Pratico** — clinic, pharmacy, emergency number, and a few reminders (offline maps, daypack, the cable car caution again)

## Adding the daily menu link
Open `index.html`, find this line near the top:
```html
<a class="qbtn disabled" id="menu-link" href="#" target="_blank" rel="noopener">
```
Replace `href="#"` with your menu URL and delete `disabled` from the class list. Re-upload the file to GitHub (or send me the link and I'll do it for you).
