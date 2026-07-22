# GCSE Classics Set Texts — one website

Interactive study tools for the OCR 2027–28 set-text prescriptions
(Eastbourne College Classics). Everything runs in the browser; no data is
collected or sent anywhere, so the pages are safe to embed in Teams.

## What's in the box

```
gcse-classics/
├── index.html            ← landing page (Latin | Greek)
├── gellius-pliny/
│   └── index.html        ← Gellius & Pliny — 8-tab app (Latin prose)
├── pyramus-thisbe/
│   └── index.html        ← Pyramus & Thisbe — 5-tool app (Latin verse)
├── herodotus/
│   └── index.html        ← Tales from Herodotus — 8-tab app (Greek prose)
└── odyssey-10/
    └── index.html        ← Odyssey 10 (Circe) — 5-tool app (Greek verse)
```

The landing page links to each text by folder, so the whole thing works as a
single site the moment it is hosted.

## Deploying it (Netlify — the easy way)

1. Go to https://app.netlify.com/drop
2. Drag the whole `gcse-classics` folder onto the page.
3. Netlify gives you a URL (e.g. `your-name.netlify.app`). That URL is the
   landing page; each text lives at `.../gellius-pliny/`, `.../herodotus/`, etc.
4. In Teams, add a **Website** tab pointing at whichever URL you want — the
   landing page for the full set, or a single text's folder for one class.

Any static host works the same way (GitHub Pages, school web space, etc.):
just upload the folder and keep the structure intact.

## Updating one text on its own (the whole point)

Each text is a single self-contained `index.html` inside its own folder, so the
four apps never touch each other. To update just one text:

1. Build/export that text's new app as a single HTML file.
2. Rename it to `index.html`.
3. Drop it into that text's folder, replacing the old `index.html`.
4. Re-upload (drag the folder to Netlify again, or push the one changed file).

Nothing else changes — the landing page and the other three texts are untouched.

## Adding a fifth text later

1. Create a new folder, e.g. `catullus/`, and put its `index.html` inside.
2. Add one more card to `index.html` (copy an existing `<a class="card">`
   block, change the `href` to `catullus/`, and edit the title/blurb).

## Current tool sets

| Text                | Tabs | Tools |
|---------------------|------|-------|
| Gellius & Pliny     | 8    | Read · Translation · Word order · Translation test · Flashcards · Gap the text · Style · My progress (+ Classroom view) |
| Tales from Herodotus| 8    | Read · Translation · Word order · Translation test · Flashcards · Gap the text · Style · My progress (+ Classroom view) |
| Pyramus & Thisbe    | 5    | Read · Translation · Translation test · Flashcards · Gap the text |
| Odyssey 10 (Circe)  | 5    | Read · Translation · Translation test · Flashcards · Gap the text |

Pyramus & Thisbe and Odyssey 10 can be upgraded to the full 8-tab shell (adding
Word order, Style and My progress) as a later job, one text at a time, without
disturbing the others.
