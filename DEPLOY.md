# Premium Plumbing & Drain — Full Website

Static multi-page site for https://premium-plumbing-production.up.railway.app/
(Client: Premium Plumbing & Drain, Inc. — seo_tool client #24)

## Structure

- `index.html` — homepage (now uses shared `/css/site.css` + global nav)
- `services.html` — services hub
- `services/*.html` — 8 service pages
- `service-areas.html` — areas hub
- `service-areas/*.html` — 6 city pages (Modesto, Turlock, Tracy, Stockton, Merced, Ceres)
- `about.html`, `reviews.html`, `contact.html`, `404.html`
- `css/site.css` — single shared stylesheet (homepage design system + sub-page components)
- `img/`, `logo.png` — assets pulled from the live deployment
- `sitemap.xml`, `robots.txt`
- `_template.html` — internal page template (not linked; safe to deploy or delete)

All internal links are root-relative (`/services/...`), so the site must be served
from the domain root (which Railway does).

## Deploy

Deploy this whole folder to the existing Railway service the same way the landing
page was deployed (Railway dashboard → the premium-plumbing service → redeploy /
upload, or `railway up` from this folder if the CLI is linked).

## Still open ([PH] markers)

Search the HTML for `[PH]`:
- Both forms are front-end only — wire to a real endpoint (Formspree/SendGrid/GHL webhook).
- The 3 review cards are placeholders — swap for real Google reviews.
- Free-estimate policy wording needs confirmation from the client.
- Stock images in `/img` should be replaced with real job photos.
