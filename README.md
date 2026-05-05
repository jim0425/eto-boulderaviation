# Boulder iQ Website — MVP

> **Status:** v1 draft, 2026-05-04
> Single-file static HTML landing page. No build step, no backend, no dependencies.

## What's here

- `index.html` — the entire site (HTML, CSS, JS embedded). One file.

## How to view it

Double-click `index.html` to open in your default browser. Works fully offline. The interactive calculator is live JavaScript — try changing the cycles/year, revenue/cycle, or gross margin inputs and the bar chart updates immediately.

## Site structure (in scroll order)

1. **Hero** — "Don't let EtO compliance eat your profit."
2. **Qualifier checklist** — gates the visitor: small <1 tpy facilities with 3M / Solventum / Anderson combination chambers
3. **Origin story** — necessity is the mother of invention; we built this because we needed it
4. **Interactive calculator** — visitor enters their cycles/year, revenue/cycle, gross margin → sees compliance cost as % of gross profit for each vendor option
5. **Three solution paths** — Indoor / Indoor + Parametric (recommended) / Indoor + Stack CEMS
6. **Vendor comparison table** — Picarro vs CleanAir vs Boulder iQ across three customer scenarios
7. **What's included** — hardware/commissioning column + compliance/support column
8. **Why Boulder iQ wins** — six differentiator cards
9. **FAQ** — eight common questions with click-to-expand answers
10. **CTA** — schedule a 30-minute facility assessment (mailto link with pre-populated form)

## How to deploy

Easiest options, ranked by speed:

1. **Netlify Drop** — netlify.com/drop, drag the folder onto the page, instant URL
2. **Cloudflare Pages** — pages.cloudflare.com, connect a Git repo or direct upload
3. **GitHub Pages** — push to a public repo, enable Pages in settings
4. **AWS S3 + CloudFront** — slightly more setup but ~$0.50/month
5. **Squarespace / Wix** — paste HTML into a custom code block

For a real launch you'll want:
- Custom domain (e.g., boulderiq.com)
- Lead-capture form replacing the mailto: link (Formspree, Netlify Forms, or your own backend)
- Analytics (Plausible, Fathom, or Google Analytics)
- A logo/favicon (the site currently uses text logo only)

## What's intentionally NOT in v1

- No images (faster load, less to maintain at this stage)
- No actual backend (mailto: link gets you started without infrastructure)
- No CMS (everything is hardcoded HTML — easy for now, add a CMS only when content velocity demands it)
- No Tailwind/build chain (single file, no toolchain to break)

## Math anchors used in the page

All numbers come from `[[../Boulder-iQ-EtO-Pricing/Picarro_vs_BoulderIQ_V4_FullStack.xlsx]]`:

- Picarro Purchase 5-yr: $662,344
- Picarro Lease 5-yr: $583,343
- CleanAir aQ alone (R2) 5-yr: $394,500
- CleanAir aQ + CEMS combined (R2) 5-yr: $1,112,200
- Boulder iQ Indoor 5-yr: $300,000
- Boulder iQ Indoor + Parametric 5-yr: $495,000
- Boulder iQ Indoor + Stack CEMS 5-yr: $660,000

Default calculator inputs reflect Boulder iQ's own facility (500 lbs/yr, 137 g/cycle, $900/cycle, 40% margin = 1,655 cycles, $595,800 gross profit).

## Suggested edits before launch

- Replace contact email if you want a different routing (jim.kasic@boulderiq.com is hardcoded in the CTA mailto)
- Add a real logo (currently text-only)
- Verify the FIFRA / NESHAP language with regulatory counsel
- Decide whether to publish before or after May 1, 2026 (NESHAP comment deadline)
- Test the calculator on mobile (it should be responsive but worth verifying on actual devices)

## Source

Project context lives in `[[../Boulder-iQ-EtO-Pricing/README.md]]`.
