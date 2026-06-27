# Lot Yield Calculator

A free, single-page tool that estimates buildable lots on a raw tract after wetlands and infrastructure takedowns. Built for land buyers and developers who need a fast screen, not a plat.

**Live site:** https://landscreening.netlify.app

---

## What it does

Enter four numbers and it returns the yield instantly:

| Input | Meaning |
|-------|---------|
| Gross acreage | Total tract size |
| Wetlands / unbuildable % | Share lost to wetlands, easements, floodway |
| Roads & infrastructure % | Takedown for ROW, detention, open space |
| Average lot size (ac) | Platted lot size on net developable land |

**Outputs:** buildable lots, net developable acres, lots per gross acre, and a land-takedown bar (gross → after wetlands → net developable).

It is a planning-level estimate only — not a substitute for engineered grading, drainage, setbacks, or a real site plan.

---

## How it's built

One self-contained `index.html` file. No build step, no dependencies, no framework. Plain HTML, inline CSS, and vanilla JavaScript. The takedown chart uses a color-blind-safe palette (blue / amber / teal), and every bar carries a text label so it never relies on color alone.

Edit the calculator by opening `index.html` and changing the markup or the `calc()` function near the bottom.

---

## Hosting

Hosted on Netlify, deployed automatically from this repository.

- **Build command:** none (leave empty)
- **Publish directory:** repository root (`/`)

Push a change to this repo and Netlify redeploys within about a minute.

### Email capture

The "Notify me" box uses Netlify Forms, which is detected automatically on deploy. Submissions appear under the **Forms** tab in the Netlify dashboard — no extra setup.

### Share preview

Open Graph and Twitter/X tags in `index.html` point at `https://landscreening.netlify.app`. If the site address ever changes, update the three URLs in the `<head>` (search for `og:image`, `og:url`, `twitter:image`).

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app |
| `favicon.svg` | Vector tab icon |
| `favicon.ico` | Fallback tab icon |
| `favicon-16.png`, `favicon-32.png`, `favicon-48.png` | PNG tab icons |
| `apple-touch-icon.png` | Home-screen icon (mobile) |
| `og-image.png` | 1200×630 social share preview |

---

## Status

Free preview tool. A paid release will add flood zones, wetlands data, and deal economics (raw land cost per lot, land as a share of finished-lot value).

© Drummond Land Co.
