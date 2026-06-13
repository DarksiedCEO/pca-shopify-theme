# PCA™ Shopify Theme — Obsidian Hydration Fountain

Luxury landing section for the PCA Obsidian Hydration Fountain.
Matte black / antique gold / luxury editorial. Dawn-compatible.

---

## Files

| File | Purpose |
|------|---------|
| `sections/pca-obsidian-landing.liquid` | Full landing section — hero, education, lifestyle, founder, guarantee, FAQ, email capture |
| `templates/page.obsidian-fountain.json` | Page template that renders the landing section |

---

## Setup in Shopify

### 1. Upload the theme

**Option A — via Shopify Admin:**
1. Zip the entire theme directory: `zip -r pca-theme.zip .`
2. Go to **Online Store → Themes → Add theme → Upload ZIP file**
3. Upload `pca-theme.zip`

**Option B — via Shopify CLI:**
```bash
shopify theme push
```

### 2. Create the landing page

1. Go to **Online Store → Pages → Add page**
2. Set the title: `Obsidian Hydration Fountain`
3. Under **Theme template**, select `obsidian-fountain`
4. Save

### 3. Connect the product

1. Go to **Online Store → Themes → Customize**
2. Navigate to the Obsidian Fountain page
3. Click the **PCA Obsidian Landing** section in the left sidebar
4. Under **Connected product**, search for and select your Obsidian Hydration Fountain product
5. Save

### 4. Add images

All images are set in the theme customizer under the section settings:

| Setting | Recommended size | Content |
|---------|-----------------|---------|
| Hero image | 1800 × 1200px | Sphynx cat + fountain, luxury environment |
| Education image | 1400 × 900px | Cat drinking from moving water |
| Lifestyle image 1 (large) | 1200 × 1600px | Luxury kitchen or living room |
| Lifestyle image 2 | 800 × 1066px | Modern interior detail |
| Lifestyle image 3 | 800 × 1066px | Sphynx cat in environment |
| Card 01 — Moving Water | 800 × 600px | Water flow detail |
| Card 02 — Modern Interiors | 800 × 600px | Interior lifestyle |
| Card 03 — Stainless Steel | 800 × 600px | Product detail / tray close-up |
| Founder portrait | 160 × 160px | Square or circular crop |

### 5. Add Google Fonts

Add these two lines to your `theme.liquid` `<head>` section **before `</head>`**:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;1,300&family=DM+Sans:wght@400;500;700;800&display=swap" rel="stylesheet">
```

Without this, the section falls back to Georgia / system-ui. It will still look good, but the luxury editorial feel requires Cormorant Garamond.

### 6. Set your contact email

In the section settings under **Guarantee → Contact email**, add your support email address. It renders as a `mailto:` link in the Direct Contact block.

---

## Trust rules (do not modify)

- No fake reviews
- No fake veterinary endorsements
- No fake hydration statistics
- No invented medical claims
- Keep copy luxury editorial — never generic dropship language

---

## V-roadmap

| Version | Status |
|---------|--------|
| V1 | Section architecture + schema |
| V2 | Education, lifestyle, founder, guarantee, email capture |
| V3 | Production hardening — sold-out, a11y, Dawn compatibility |
| V4 | Asset library — hero images, lifestyle images, product detail |
| V5 | Klaviyo integration — welcome flow, abandoned cart |
