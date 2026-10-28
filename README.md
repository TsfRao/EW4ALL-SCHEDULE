# EW4All Conference Schedule (prototype)

Mobile-friendly schedule for the UN/Pakistan International Conference on Leveraging Space Technology for EW4All, Climate Actions and Disaster Risk Assessment (27-31 Oct 2026, Sheesh Mahal Hall, Serena Hotel, Islamabad).

Unofficial prototype built from the Programme Book. Verify details with the organisers.

## Features
- Day tabs, search by name, topic, organisation or session
- "Now / Next" banner (Pakistan time)
- Save sessions to "My schedule" (kept in the browser) with clash warnings
- Add to Google Calendar per session (Asia/Karachi)

## Run locally
Open `index.html` in a browser. There is no build step and no dependency.

## Deploy on GitHub Pages
1. Push these files to a new repository (branch `main`).
2. Repository **Settings > Pages > Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`.
3. After about a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

## Edit the schedule
All data is the `D` text block inside `index.html`, one line per item:

```
day|start|end|type|session code|title|speaker(s)|organisation|note
```

- `day`: 27 to 31 (October 2026). `start`/`end`: 24-hour time without colon, for example `930` or `1400`.
- `type`: `C` ceremony, `K` keynote, `P` panel, `T` talk, `V` visit.
- `session code`: a key from the `S` object (for example `T10`) that holds the session name and moderator.
- `note`: optional; shown with a warning mark.
- Do not use the `|` character inside a field. Keep saved-session IDs stable by only appending new lines at the end of the block.

## Known items to confirm with the organisers
- NDMA visit time on Friday 30 Oct (printed 1400-1600; shown after Technical Session 10 as 1540-1740, provisional).
- Technical Session 1: the 1600-1615 and 1610-1630 slots overlap as printed.
- Ahmed Kamal appears with different titles; two similar talks (Wed 1200 and Thu 0930).

## Planned
Validation script, reminders (ntfy or Telegram), offline mode (PWA), speaker profile links with consent, venue map.
