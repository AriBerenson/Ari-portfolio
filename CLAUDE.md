# Ari Berenson portfolio site

Static HTML portfolio for Ari Berenson (product and UI/UX designer). Hosted on GitHub Pages from the `main` branch. No build step, no framework: edit the HTML files directly.

**Read `../Ari-Source-Materials/HANDOFF.md` first.** It has the history, decisions, which numbers are backed by which source, and what is still open. (If that folder is not next to this one, ask where it is.)

## Folders
- This folder (`ari-portfolio`): the website and the git repo. Edit only here.
- `../Ari-Source-Materials`: source material (CVS KPI screenshots, case study assets, résumé, question and answer docs). Not part of the website. Never copy it into this repo.

## Pages
- `index.html`: homepage with 8 cards: 01 CVS Health Super App, 02 Agently, 03 Picin, 04 Inmoji, 05 New Balance VAZEE, 06 MyNB, 07 Brand Identity, 08 Sitting In The Circle.
- CVS case study: `cvs-health-super-app.html` (main), then `cvs-health-search.html` and `cvs-health-navigation.html` (deep dives). Page chain: main, search, navigation, Agently.
- Other case studies: `agently.html`, `picin.html`, `inmoji.html`, `mynb.html`, `newbalance-vazee.html`.
- `brand-identity.html`: one page holding Tiger Lily Granola, By Doctors, and WEOM (Ari's own brand projects).
- `sitting-in-the-circle.html` (illustration), `about.html`, `resume.pdf`.
- There is no contact page or form (deliberately removed). The menu ends with a LinkedIn icon.

## Shared files
- `responsive.css`: phone and tablet layout, label colors, footer, CVS info-row grid, LinkedIn icon. Each page also has its own `<style>` block.
- `lightbox.js` / `lightbox.css`: click-to-zoom on every image (except the logo).
- `images/`: site images. CVS images are in `images/cvs/`.

## Design conventions
- Colors: background `#F0F1ED`, text `#1B2430`, accent orange `#DD5E1E`. Orange is for labels (`Lead:`, `RESULT:`, section labels) and highlights; everything else is dark.
- Fonts: Fraunces (headings), Space Grotesk (body), JetBrains Mono (labels, captions). The heading font may change later; do not change it unless asked.
- Case studies share one pattern: back link, label tag, title, info row (role, timeline, team, skills), hero image, then sections with orange mono section labels, stat cards, learnings cards, and a footer chain linking to the next page.
- Orange "[Ari: ...]" notes (`class="ph-tag"`) mark placeholders only Ari can fill. Remove the note once the question is answered; leave the rest.
- Homepage color key: Product / UX (orange), Brand & Campaign (gold), Brand Identity (blue), Illustration / Personal (teal).

## Rules for claims
- Only state what a source supports. If a number or claim does not match a source, say so instead of rounding up. The HANDOFF.md claims table lists where each CVS number comes from.
- Show the exact wording of any change to a claim or number before applying it.

## Checking changes
- Preview: run `python3 -m http.server 8765 --bind 127.0.0.1` from this folder and open http://127.0.0.1:8765, then stop the server. Do not leave preview files in the repo.
- Check desktop (about 1280px wide) and phone (375px). Measure rather than eyeballing: card widths and heights, left edges, line wraps, and no sideways scrolling.
- Do not commit or push unless asked. The owner commits and pushes with GitHub Desktop.
