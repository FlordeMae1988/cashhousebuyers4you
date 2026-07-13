# Cash House Buyers 4 You — Implementation Handoff

This repository contains the production-ready static website implementation for **Cash House Buyers 4 You**.

The original scope was taken from `FREELANCER-HANDOFF.md` and focused on implementation tasks inside the codebase (excluding deployment account actions and DNS cutover steps).

## Project Structure

- `index.html` - Main homepage
- `homepage-mockup.html` - Legacy homepage alias (kept for compatibility)
- Core pages:
  - `how-it-works.html`
  - `options-to-sell.html`
  - `about.html`
  - `contact.html`
  - `faq.html`
  - `seniors.html`
  - `for-investors.html`
  - `careers.html`
  - `atlanta.html`
  - `tulsa.html`
  - `florida.html`
  - `seattle.html`
  - `privacy.html`
  - `terms.html`
- SEO files:
  - `sitemap.xml`
  - `robots.txt`
- Tracking/events:
  - `analytics.js`
- Operations notes:
  - `NON-DEPLOY-CHECKLIST.md`

## What Was Implemented

## 1) Homepage and Routing Compatibility

- Renamed/established homepage at `index.html`.
- Kept `homepage-mockup.html` as a compatibility alias.
- Updated internal links to work in local static-server environments (no rewrite engine).
- Added compatibility route files for local testing:
  - `atlanta`
  - `tulsa`
  - `florida`
  - `seattle`

## 2) Forms Wired for Netlify

All required forms now use Netlify-compatible markup:

- `method="POST"`
- `data-netlify="true"`
- `name="<form-name>"`
- hidden `form-name`
- `netlify-honeypot="bot-field"` with hidden `bot-field`

Implemented forms include:

- Seller lead form (homepage): `seller-lead-homepage`
- Contact form: `contact-inquiry`
- Seniors form: `senior-inquiry-jas` (added)
- Investor forms:
  - `investor-signup` (investor page)
  - `investor-signup-homepage` (homepage module)
- Career form: `career-application`

## 3) Form Routing Metadata

Hidden fields were added to support clean Zapier branching:

- Seller leads: `route_to=seller-leads`
- Seniors: `route_to=jas`
- Investor: `route_to=buyer-list`
- Careers: `route_to=hr-inbox`
- Contact routing strategy: `routing_strategy=route-by-reason-dropdown`

## 4) Tracking via Google Tag Manager

- GTM container `GTM-MPPZSR8V` is included in all HTML pages: the container script in `<head>`, and a `<noscript>` iframe fallback immediately after `<body>`.
- The legacy gtag snippet was removed — its GA4 property sat in an account the business no longer controls.
- GA4 configuration and event tags (`form_submit`, `phone_click`, `cta_click`) are now managed from the GTM dashboard, so tracking changes no longer require code edits.
- `analytics.js` remains in the repo but no longer loads GA4; GTM handles it.

## 5) Asset Fixes

- Added missing image path for Jas:
  - `assets/jas.jpg`
- Updated references now resolve in:
  - `index.html`
  - `about.html`
  - `seniors.html`

## Local Development

Run a local static server from the project root:

```bash
cd "/Users/a2021/Downloads/Sami-Handoff"
python3 -m http.server 8000
```

Open:

- `http://localhost:8000/`
- `http://localhost:8000/atlanta`
- `http://localhost:8000/tulsa`
- `http://localhost:8000/florida`
- `http://localhost:8000/seattle`

## Remaining Manual Tasks (Account/Platform Side)

These are intentionally not fully automatable from local files only:

- Create/finish Zapier flows (email, SMS/Twilio, Sheets, optional Slack).
- Replace verification placeholders and verify ownership:
  - `google-site-verification`
  - `msvalidate.01`
- Submit `sitemap.xml` in Google Search Console and Bing Webmaster Tools.
- Enable crawl/error email alerts in webmaster dashboards.
- Execute real-device QA (iPhone/Android/tablet) and final acceptance checks.

For details, see `NON-DEPLOY-CHECKLIST.md`.

## Notes

- This project is intentionally static HTML/CSS/JS (no framework migration).
- Deployment instructions (Netlify + DNS cutover) remain outside this README and should be handled in platform accounts.
