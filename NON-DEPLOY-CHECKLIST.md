# Non-Deployment Completion Checklist

This checklist covers `FREELANCER-HANDOFF.md` items that are not deployment/DNS.

## 1) Forms + Routing (Implemented in code)

- Homepage hero seller form: `seller-lead-homepage` -> `route_to=seller-leads`
- Contact form: `contact-inquiry` with `reason` dropdown + `routing_strategy=route-by-reason-dropdown`
- Seniors form: `senior-inquiry-jas` -> `route_to=jas`
- Investor signup form: `investor-signup` and `investor-signup-homepage` -> `route_to=buyer-list`
- Career application form: `career-application` -> `route_to=hr-inbox`

## 2) Zapier Automations (Manual account setup)

Recommended trigger: Netlify form submission webhook.

Suggested filter logic by form metadata:

- Seller leads: `route_to == seller-leads`
- Jas queue: `route_to == jas`
- Buyer list: `route_to == buyer-list`
- HR inbox: `route_to == hr-inbox`
- Contact general routing: `form-name == contact-inquiry` and branch on `reason`

Suggested actions per branch:

1. Email notification to `info@cashhousebuyers4you.com`
2. SMS notification via Twilio
3. Append row to Google Sheets
4. Optional Slack notification

## 3) GA4 + Search Console/Bing (Partially implemented in code)

Implemented:

- GTAG snippet (`G-8GYNDHV0C5`) added in all HTML pages.
- Conversion events in `analytics.js`:
  - `generate_lead` (form submissions)
  - `phone_click` (tel links)
  - `tool_completion` (custom events)

Still required manually:

- Replace placeholder verification meta tokens:
  - `google-site-verification`
  - `msvalidate.01`
- Verify domain ownership in Google Search Console and Bing Webmaster Tools.
- Submit `https://cashhousebuyers4you.com/sitemap.xml` in both consoles.
- Enable email alerts for crawl/indexing issues.

## 4) Real-device QA (Manual testing)

Minimum pass:

- iPhone: Safari + Chrome
- Android: Chrome + Samsung Internet
- iPad/tablet viewport checks
- Confirm all forms submit in production
- Confirm phone links open dialer
- Confirm no broken links

## 5) Post-launch fixes (Operational)

- Resolve bugs reported by client/users.
- Keep route/link parity between local (`.html`) and production clean URLs.
- Optimize newly added images before future content uploads.
