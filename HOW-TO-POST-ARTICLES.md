# How to Post New Blog Articles

**No CMS needed. No developer needed. Takes you 5 minutes per article.**

---

## What You Have

A template file: **`article-template.html`** — this is your starting point for every new article.

---

## 5-Minute Article Posting Workflow

### Step 1 — Copy the Template

1. Go into your Netlify site's GitHub repo (or the files folder on your computer)
2. Find `article-template.html`
3. Copy it
4. Rename the copy using this format: **`article-slug-with-dashes.html`**

Examples:
- `how-to-sell-inherited-house-atlanta.html`
- `seller-financing-explained-tulsa.html`
- `probate-sale-guide-florida.html`
- `subject-to-real-estate-seattle.html`

Keep the file in your repo's root or in a `/blog/` subfolder — either works.

### Step 2 — Edit 3 Lines in the `<head>` Section

Open the file in any text editor (VS Code, Notepad, Sublime, or even Google Docs). Find these 3 lines near the top:

```html
<title>ARTICLE TITLE HERE | Cash House Buyers 4 You</title>
<meta name="description" content="ARTICLE META DESCRIPTION HERE — 150-160 characters..." />
<meta property="og:image" content="https://cashhousebuyers4you.com/assets/og-image.png" />
```

Replace with:
- **Title:** The actual article title. Include your primary keyword. Keep under 60 characters.
- **Meta description:** Summary in 150–160 characters. Tell readers what they'll learn. Include the primary keyword once.
- **OG image:** Leave alone unless you have a custom image for this article.

### Step 3 — Edit the Article Body

Scroll down to the comment that says `<!-- ========== EDIT BELOW FOR EVERY NEW ARTICLE ========== -->`

Everything between that comment and `<!-- ========== END OF EDITABLE SECTION ========== -->` is where you write. Fill in:

- **Category tag** (top of article) — Atlanta, Tulsa, Florida, or Seattle
- **Published date** — today's date
- **Read time** — estimate (1 min per 200 words)
- **Article title** — same as the `<title>` tag
- **Subhead** — one sentence summary
- **Body content** — use the template structure: intro → H2 section → H3 subsections → list → blockquote → inline CTA → more H2 sections → conclusion → CTA

### Step 4 — Upload

Two ways:

**Option A — If you're using GitHub + Netlify (the proper way):**
1. Drag the file into your GitHub repo
2. Click "Commit changes"
3. Netlify auto-deploys within 60 seconds
4. Article is live at: `cashhousebuyers4you.com/your-article-slug`

**Option B — If you just want to upload manually:**
1. Go to Netlify.app → log in
2. Open your site → Deploys tab
3. Drag the article file into the deploy drop zone
4. Done.

### Step 5 — Update the Sitemap

**Important for SEO:** Add your new article URL to `sitemap.xml`:

```xml
<url>
  <loc>https://cashhousebuyers4you.com/your-article-slug</loc>
  <lastmod>2026-04-23</lastmod>
  <changefreq>monthly</changefreq>
  <priority>0.6</priority>
</url>
```

Paste that block inside the `<urlset>` tag (before `</urlset>`). Change the URL and date.

### Step 6 — (Optional but Good SEO) Tell Google

1. Go to Google Search Console
2. "URL Inspection" → paste your new article URL
3. Click "Request Indexing"
4. Google crawls it within a day

---

## Content Tips for Better Rankings

1. **Write 1,500–2,500 words.** Google rewards depth. Short articles don't rank.
2. **Use specific numbers.** "We closed 9 days after contract" beats "fast closing."
3. **Include real deal examples.** Names optional, situations real. This is what separates your articles from AI-generated junk.
4. **Add images.** Use the `<img>` tag. Host images in an `/assets/` folder.
5. **Internal link.** Link to your Options to Sell page, How It Works page, FAQ, market pages at least 2–3 times per article.
6. **Include a local angle.** Mention specific neighborhoods, counties, state-specific laws. Google loves local relevance.
7. **Add one inline CTA** mid-article. Not more than one — it's annoying.

---

## Article Ideas to Publish (Priority Order)

### Atlanta (Flagship)
1. "How to Sell a House Fast in Atlanta: Cash Offer vs. Realtor"
2. "Selling an Inherited House in Atlanta: The Complete 2026 Guide"
3. "Cash Home Buyers in Atlanta: How to Spot Legit vs. Scam"
4. "Subject-To Real Estate in Atlanta: What It Is, When to Use It"

### Tulsa
1. "Sell My House Fast Tulsa, OK — 2026 Guide"
2. "Probate House Sale Tulsa, OK: How the Process Works"
3. "Seller Financing in Tulsa: Should You Consider It?"

### Florida (Hernando/Pasco)
1. "Selling an Inherited Home in Hernando County, FL: 2026 Guide"
2. "Sell My House Fast Spring Hill, FL — Cash &amp; Creative Options"
3. "Florida Homestead Exemption &amp; Cash Sales: What Sellers Need to Know"

### Seattle
1. "Sell Your House Fast in Seattle: Why Seller Financing Might Net You More"
2. "Capital Gains Tax on a Seattle Home Sale: 4 Ways to Minimize It"
3. "Cash Home Buyers in Seattle: A Local Seller's Guide"

---

## Want Me (Claude) to Write These For You?

In any future Cowork session, just say: *"Write me the article 'How to Sell a House Fast in Atlanta'"* and I'll produce a full 2,000-word SEO-optimized article ready to paste into the template.

Same for any topic. 15 minutes per article with me.
