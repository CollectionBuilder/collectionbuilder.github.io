# CB-Essay Page (`/built-ons/cb-essay.html`)

A standalone page for CB-Essay. Use the same layout as other CB site pages (navbar, container, footer).

## Front Matter (if using Jekyll)

```yaml
---
layout: page
title: CB-Essay
---
```

## Page Content

### Header Area

**Title:** CB-Essay

**Tagline:** Long-form digital scholarship, built on CollectionBuilder.

**Action buttons (row):**
- See the Demo → `https://collectionbuilder.github.io/cb-essay/`
- Use the Template → `https://github.com/CollectionBuilder/cb-essay`
- Read the Docs → `https://collectionbuilder.github.io/cb-essay/about.html`

---

### What Is CB-Essay?

CB-Essay is a framework for writing and publishing multimodal essays using CollectionBuilder. You write in Markdown, your collection items live in a CSV, and CB-Essay lets you weave them together — embedding images, documents, audio, and video directly into your narrative through simple includes.

It's built on CollectionBuilder-CSV, so you get all the standard collection pages (Browse, Map, Timeline, Subjects) alongside your essay content.

---

### Origin

CB-Essay grew out of work with graduate students at the University of Idaho Library's [Center for Digital Inquiry and Learning (CDIL)](https://cdil.lib.uidaho.edu/) who were building multimodal essays for their theses. Two projects drove the development:

- [**Tender Spaces**](https://cdil.lib.uidaho.edu/tender-spaces/) by Alicia Gladman — a multi-lingual, multimodal essay on the life, art, and forced institutionalization of Gaëtane Buttigieg
- [**Sedimentation**](https://cdil.lib.uidaho.edu/sedimentation/) by Hannah Green — a CDIL graduate fellow project

Both needed a way to combine long-form writing with collection items on the web. The existing tools weren't cutting it, so we built CB-Essay.

---

### Features

**Essay writing:**
- Write in Markdown in an `_essay/` folder — each file is a section or chapter
- Sequential prev/next navigation between essay sections
- Two themes — traditional essay layout or monograph-style with chapter navigation
- Margin notes and asides that can link to collection items
- Blockquotes with full attribution
- Scroll-based section transitions (via Scrollama)
- Inline image galleries and mini-maps

**Print output:**
- Built-in print feature using [Paged.js](https://pagedjs.org/) that turns any essay into a properly formatted PDF with page breaks and layout — so your web-first essay can also be a print artifact

**Collection integration:**
- All standard CollectionBuilder-CSV features: Browse, Map, Timeline, Subjects, data downloads
- Reference collection items from within your essays using simple includes
- Dual-collection model: essays + metadata-driven object pages

**Bonus:**
- Project Gutenberg Extractor — a GitHub Action that pulls any of 60,000+ public domain books into your essay folder, pre-formatted and ready to publish

---

### Example Projects

- [**CB-Essay Demo**](https://collectionbuilder.github.io/cb-essay/) — self-documenting demo that teaches you the features as you read
- [**Tender Spaces**](https://cdil.lib.uidaho.edu/tender-spaces/) — multimodal essay on Gaëtane Buttigieg (Alicia Gladman)
- [**Sedimentation**](https://cdil.lib.uidaho.edu/sedimentation/) — CDIL graduate fellow project (Hannah Green)

---

### Get Started

1. [Use the template](https://github.com/CollectionBuilder/cb-essay) on GitHub
2. Read the [Getting Started guide](https://collectionbuilder.github.io/cb-essay/essay/02-get-started.html) on the demo site
3. Explore the [About & documentation](https://collectionbuilder.github.io/cb-essay/about.html)

Questions? Post on our [GitHub Discussion Board](https://github.com/orgs/CollectionBuilder/discussions) or email [collectionbuilder.team@gmail.com](mailto:collectionbuilder.team@gmail.com).

---

## Design Notes

- Keep this page simple and scannable — it's a landing page, not documentation
- Consider including a screenshot or embedded image of the CB-Essay demo site (the brush painting splash page is visually striking)
- The features section could use the same card/grid pattern used elsewhere on the CB site, or just stay as clean prose sections
- Link back to the blog post announcing CB-Essay: `/2026-05-07-introducing-cb-essay/`
