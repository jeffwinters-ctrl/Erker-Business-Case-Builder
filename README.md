# Abstrakt Marketing Group — Creative ROI Calculator

A standalone single-page web application that allows B2B and B2C sales prospects to calculate the projected ROI of investing in creative marketing services.

## Features

- B2B and B2C industry selector with vertical-specific modifiers
- 9 creative channels (Video, Display, Social, Email, CTV, etc.) with multi-select
- Adjustable monthly budget ($2,500–$100,000) and campaign duration (3–24 months)
- Real-time metric cards: Total investment, Projected revenue, Blended ROI, Break-even month
- Channel breakdown bar chart and growth-over-time line chart (Chart.js)
- Export summary for email/slide deck use
- Dark mode support
- Fully responsive

## Tech Stack

- Plain HTML + CSS + Vanilla JavaScript (no build step)
- Chart.js v4 via CDN
- No backend, no database, no auth — fully static

## Deployment

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → "New Project" → import the GitHub repo
3. Vercel auto-detects static HTML — click Deploy
4. Live URL in ~30 seconds

Or simply open `index.html` directly in a browser.
