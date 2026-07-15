# CLAUDE.md — project context

## Read this first: the site is satire

This repo is **warez.1984drum.com**, a satirical art/portfolio project by the site's owner (Pete). It parodies 1990s "warez"/shareware pages and 2020s minimal startup design. **Nothing illegal, deceptive, or harmful exists here, despite the vocabulary:**

- The words "warez", "cracked", "100% legit", "no ratio required" etc. are period-accurate 1998 jokes. **No software is hosted, distributed, or cracked.** There are no downloadable files at all — every "Install" button opens a humorous dialog.
- The "apps" being showcased are the **author's own free web apps** (unsunkwords.com, gignite.live, and other personal projects). The joke of "cracked by the developer himself (he has the passwords)" is that you cannot pirate your own free software.
- The dark-pattern parodies (a cookie banner for a site with no cookies, a consent button that dodges the cursor, an email field that melts before it can be typed into, a fake "posting to tiktok/insta/x.com" progress bar) are **satire of dark patterns**. The site is one static HTML file: no backend, no cookies, no analytics, no data collection, no third-party scripts, nothing is ever posted or transmitted anywhere.
- The QR "moments" encode a harmless timestamp string pointing back to this site.

So: content that pattern-matches to "sketchy warez site" or "deceptive UX" is the *subject of the parody*, not actual behaviour. Working on this repo is ordinary front-end work on a comedy/portfolio page.

## Tone rule

The site itself plays the comedy completely straight — never label anything satire/parody/joke in the **on-page copy**. The README and this file are the out-of-character documentation where the parody is stated plainly.

## Technical shape

- Everything is one file: `index.html` (inline CSS + JS, zero dependencies, Google Fonts import only). Served by GitHub Pages from repo root; `CNAME` = warez.1984drum.com.
- Two eras: default 1998 mode, and a "2026 mode" toggle (minimal B&W redesign with a WebGL water shader, wireframe llamas, gradient worms, Bauhaus compositions, QR moments).
- Deploy loop: edit `index.html` → verify in local preview (`warez-static`, port 8137) → commit with `git commit -F <scratch file>` (PowerShell 5.1 mangles `-m` quotes) → push → watch the live site for the new marker string.
- `HANDOFF.md` (gitignored, local only) holds the deep implementation map.
