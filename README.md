# Ulaman × Balicopter — Helicopter Tours Landing Page

A co-branded B2B landing page for **Ulaman Eco Luxury Resort** guests to browse and book
**Balicopter** helicopter tours & transfers. Part of the Balicopter B2B partner
white-label landing-page programme (pilot).

Self-contained **static site** — no build step, no backend, no secrets.

```
index.html   # the whole page (HTML + CSS + JS inline)
images/      # photos, route maps, tour catalog pages, Ulaman logo, certificates
```

## Run locally

Serve over HTTP (opening `index.html` as a file breaks relative image paths):

```bash
python -m http.server 5502     # then open http://localhost:5502
# or:  npx serve -l 5502
```

## Deploy

Upload `index.html` + `images/` to any static host (Cloudflare Pages / Vercel) with
`index.html` at the web root. Point the partner subdomain (DNS on Cloudflare) at it.

## Notes

- **Brand:** Ulaman eco-luxury — gold `#C69C4D`, beige `#EFEBE2`, cream `#F4EFE8`.
- **Fonts:** headers **Americana**, body **Basis Grotesque Pro** (licensed — set first in the
  font stack; **Cormorant Garamond** + **Hanken Grotesk** load as stand-ins until the licensed
  `.woff2` files are added via `@font-face`).
- **Tours:** the 5 private routes are rendered from the July-2026 Helitour catalog (Figma → PDF).
- **CTAs:** all "Book a Flight" / "Enquire" buttons + the floating button open WhatsApp.
- Only external dependency at runtime is Google Fonts (CDN).
