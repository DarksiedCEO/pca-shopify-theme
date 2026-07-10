# PCA™ Shopify Theme — Pussycat Alley

Luxury Shopify theme for Pussycat Alley (PCA), a Sphynx-first cat brand.
Obsidian black / soft ivory / antique gold / luxury editorial. Dawn-compatible.

**Current active launch: The Rare Ones Wardrobe** (apparel + Rare Skin Bath Bonnet™ add-on).
The original Obsidian Hydration Fountain landing page is retained but no longer the homepage —
see `sections/pca-obsidian-landing.liquid` below. Full strategy/copy source of truth:
[`docs/launch-blueprint.md`](docs/launch-blueprint.md).

---

## Files

| File | Purpose |
|------|---------|
| `sections/pca-wardrobe-landing.liquid` | **Homepage.** Full Rare Ones Wardrobe landing — announcement bar, video hero, trust strip, collection grid, Buy 2/Buy 3 offer, Bath Bonnet add-on, education, style guide, size guide, brand trust, guarantee, FAQ, final CTA |
| `templates/index.json` | Renders `pca-wardrobe-landing` as the homepage |
| `assets/pca-wardrobe-hero-video.mp4` | Bundled launch hero video (AI-generated placeholder — see Creative Notes below) |
| `assets/pca-wardrobe-hero-poster.jpg` | Poster frame / fallback image for the hero video |
| `assets/pca-wardrobe-scholar-still.jpg`, `assets/pca-wardrobe-turtleneck-still.jpg` | Bundled AI-generated campaign stills, available as image fallbacks in the section |
| `sections/pca-obsidian-landing.liquid` | Legacy landing section for the PCA Obsidian Hydration Fountain — not currently rendered on any template |
| `templates/page.obsidian-fountain.json` | Legacy page template for the fountain landing section |

---

## Before this goes live — required real values

The wardrobe landing section deliberately renders **no invented facts**. In the theme customizer,
under the **Guarantee & Policy** settings group, these fields are blank by default and must be filled
in with true values before launch (the section shows an honest generic fallback until they are):

- Processing time
- Transit time
- Return window (days)
- Support email

Also confirm final pricing for the Alley Scholar Collection™ and Rare One Winter Vest™ styles —
the collection grid ships with `$--` placeholders for these two products until real prices are set.

## Creative notes

The bundled hero video and stills are AI-generated (Higgsfield) launch-speed placeholders — see
`docs/launch-blueprint.md` §12a for the full creative-production guardrails. They are original
campaign-mood imagery, not real product photography. Swap them via the section's `image_picker` /
`hero_video_url` settings once real product photography or a real shoot exists. **Product pages**
(once products are connected) should always use real supplier photos, never these campaign assets.

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
