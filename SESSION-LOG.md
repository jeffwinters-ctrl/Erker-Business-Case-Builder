# SESSION LOG — Abstrakt Creative ROI Calculator

**Project:** Erker Business Case Builder
**Repo:** https://github.com/jeffwinters-ctrl/Erker-Business-Case-Builder.git
**Branch:** main
**Deploy target:** Vercel (static site, connect the GitHub repo)
**Last updated:** 2026-03-26

---

## Project Overview

A standalone single-page web app (single `index.html`, no build step) for Abstrakt Marketing Group that lets B2B/B2C sales prospects calculate projected ROI of investing in creative marketing services (video, display ads, social creative, email, CTV, etc.).

**Tech stack:** Plain HTML + CSS + Vanilla JS, Chart.js v4 via CDN. No framework, no backend, no database.

---

## What Was Built

- Full spec implementation from `AI-BUILD-PROMPT.md` (included in zip)
- B2B (6 industries) and B2C (8 industries) selector with vertical-specific multipliers
- 9 creative channels with multi-select and blended multiplier formula
- Investment sliders: monthly budget ($2,500-$100,000) and duration (3-24 months)
- 4 auto-updating metric cards: Total investment, Projected revenue, Blended ROI, Break-even month
- Dynamic explain callout with natural-language summary
- Two chart views: Channel breakdown (HTML bars) and Growth over time (Chart.js line)
- Export modal with copy-to-clipboard for sales email/deck use
- Disclaimer at bottom with source citations

---

## Branding & Design Decisions

- **Dark mode is forced/always-on** (no light mode toggle, `<meta name="color-scheme" content="dark">`)
- Color palette derived from abstraktmg.com:
  - Page bg: `#0b1120` / Card bg: `#111827` / Surface: `#1a2235`
  - Primary accent (green): `#31c48d` — used for selections, labels, tabs, slider thumbs, logo dot
  - Blue: `#3b82f6` — used for investment metric, chart lines
  - Orange: `#f46f0a` — used for CTA/export buttons
  - Amber: `#f59e0b` — used for break-even metric
- Logo: lowercase "abstrakt" with oversized green period (`.logo-dot` class)
- Header has subtle radial green gradient glow
- Footer includes branded wordmark + link to abstraktmg.com

---

## Commit History

| Hash | Message |
|------|---------|
| d82bc49 | Initial commit: Abstrakt Creative ROI Calculator |
| bc699d6 | Dark mode default with Abstrakt brand colors and styling |
| 0f2677a | Force dark mode, fix mobile slider overflow, make logo period visible |

---

## Known Issues Fixed

1. **Dark mode not activating** — was using `prefers-color-scheme` media query (follows OS). Fixed by making dark the only/default scheme and removing light mode overrides.
2. **Mobile slider overflow** — label `min-width: 130px` + value `min-width: 100px` pushed range input off-screen. Fixed with `flex-wrap`, `min-width: 0` on input, and stacked layout at <=600px.
3. **Logo period not visible** — added dedicated `.logo-dot` class with larger font-size (28px header / 22px footer) and green accent color.

---

## File Structure

```
Business Case App for Creative/
├── index.html          ← entire app (single file, self-contained)
├── AI-BUILD-PROMPT.md  ← original spec/prompt (reference only)
├── files.zip           ← original source zip (reference only)
├── README.md           ← deployment notes
├── SESSION-LOG.md      ← this file
└── .gitignore          ← excludes zip and build prompt from repo
```

---

## Where We Left Off

- App is fully functional and deployed to GitHub
- Dark mode branding is complete and matches Abstrakt identity
- Mobile responsiveness has been addressed for sliders
- **No outstanding bugs or incomplete features at this point**

---

## Potential Next Steps (not yet requested)

- Add light mode toggle switch if needed for prospect presentations on projectors
- Animate metric cards on value change
- Add "Schedule a call" CTA linking to abstraktmg.com booking page
- Custom favicon with Abstrakt branding
- PDF export option in addition to plain-text copy
- A/B test different default channel selections
- Add more industries or channels as Abstrakt's offerings expand
