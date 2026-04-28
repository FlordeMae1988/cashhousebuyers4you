# Cash House Buyers 4 You — Freelancer Handoff Package

## 🎯 Scope (8 Hours or Less)

This is a **pre-built HTML website**. All 15 pages are done, all copy is written, all design is complete. Your job is **implementation only** — deploy, integrate, launch.

**Estimated time: 6–8 hours. Budget: $400–$800 flat fee.**

---

## 📦 What You're Delivered

All files are in this folder. 15 complete HTML pages:

| File | Purpose |
|---|---|
| `homepage-mockup.html` | Homepage (rename to `index.html` on deploy) |
| `how-it-works.html` | How It Works process page |
| `options-to-sell.html` | Creative finance options page (cash, seller financing, subject-to) |
| `about.html` | About Us + team |
| `contact.html` | Contact page with form |
| `faq.html` | Frequently Asked Questions |
| `seniors.html` | For Seniors & Families page |
| `for-investors.html` | Investor list signup page |
| `careers.html` | Careers page with application form |
| `atlanta.html` | Atlanta, GA market page (flagship) |
| `tulsa.html` | Tulsa, OK market page |
| `florida.html` | Hernando/Pasco, FL market page |
| `seattle.html` | Seattle, WA market page |
| `privacy.html` | Privacy Policy |
| `terms.html` | Terms of Service |
| `sitemap.xml` | Sitemap for search engines |
| `robots.txt` | Robots file |

---

## ✅ Your Deliverables (6–8 hours total)

### 1. Deploy to Netlify (1–2 hours)

1. Create free Netlify account
2. Create GitHub repo, push all files
3. Connect Netlify to GitHub repo (auto-deploys on push)
4. Rename `homepage-mockup.html` → `index.html`
5. Create URL-friendly routes — rename market files:
   - `atlanta.html` works at `/atlanta`
   - `tulsa.html` works at `/tulsa`
   - `florida.html` works at `/florida`
   - `seattle.html` works at `/seattle`
   - Configure Netlify `_redirects` file for clean URLs (no `.html` extensions in URLs)
6. Verify all internal links work after deploy

### 2. Wire Up Forms with Netlify Forms + Zapier (1–2 hours)

Every form in the site is a standard HTML form. Add `data-netlify="true"` and a name attribute. Netlify Forms auto-captures submissions (free for first 100/mo).

**Forms to configure:**
- Homepage hero "Get My Offer" form → seller leads
- Contact form → general inquiries + routes to team by dropdown
- Seniors page form (if present) → Jas
- Investor signup form → buyer list
- Career application form → HR inbox

**Zapier automations (paid account needed — client has one):**
- Form submission → email to `info@cashhousebuyers4you.com`
- Form submission → SMS to client via Twilio ($20/mo)
- Form submission → Google Sheet row (optional but recommended)
- Form submission → Slack channel notification (if client uses Slack)
- Missed call on CallRail tracking number → auto-text seller "Sorry I missed you, I'll call back within the hour"

### 3. DNS Cutover at Namecheap (30 min)

- Current domain: **cashhousebuyers4you.com** registered at Namecheap
- Client will provide Namecheap login access
- Update DNS records to point at Netlify:
  - A record: `75.2.60.5` (Netlify's load balancer)
  - CNAME `www` → `<your-netlify-subdomain>.netlify.app`
- SSL cert auto-provisions via Netlify
- Propagation takes 1–24 hours

### 4. Google Analytics 4 + Search Console (1 hour)

- Client provides Google account access
- Install GA4 tracking code on every page (add to `<head>`)
- Set up conversion events: form submissions, phone clicks, tool completions
- Verify Google Search Console ownership
- Submit `sitemap.xml` to Google + Bing Webmaster Tools
- Set up email alerts for crawl errors

### 5. Real-Device QA (1 hour)

- Test on iPhone Safari + Chrome
- Test on Android Chrome + Samsung Browser
- Test tablets (iPad, Samsung tablet)
- Check all forms submit correctly
- Check all phone numbers tap-to-call on mobile
- Verify no broken links

### 6. Post-Launch Fixes (1 hour)

- Address any bugs discovered post-launch
- Fix any design inconsistencies
- Optimize page load times (image compression if needed)

---

## 🛠 Tools to Set Up (Additional — can be done by client's VA, not you)

If client wants you to handle these, add 2–3 hours:

- 4 interactive tools: Solution Matcher Quiz, Net Proceeds Calculator, Equity Calculator, ARV Estimator
- 8 SEO articles (content needed from client or me)
- BBB embed code (client will provide)

These are **optional** — site can launch without them and they can be added post-launch.

---

## ❗ What NOT to Do

- Don't rebuild in WordPress/React/Vue. The static HTML is intentional — faster, cheaper, better SEO.
- Don't change the design/colors without client approval.
- Don't use page builders (Elementor, Divi). Code is clean and should stay that way.
- Don't add tracking pixels the client hasn't requested (Facebook Pixel, TikTok, etc.).

---

## 📞 Communication with Client

- **Client:** Jagger, Managing Partner
- **Email:** jaggermailing@gmail.com
- **Phone:** (866) 883-3769
- Prefers Slack or email. Available during US Eastern Time business hours.
- Questions? Ask directly. Don't assume.

---

## 💰 Payment Structure (suggested)

- 30% deposit on contract signing
- 40% at end of deployment (steps 1–3 complete)
- 30% on final launch (steps 4–6 complete + client QA approval)

Fixed-price recommended: **$500–$600** for someone competent. $800 for premium quality.
