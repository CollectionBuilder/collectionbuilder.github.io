# Built Ons — Site Implementation Guide

This folder contains content and specs for adding a "Built Ons" section to collectionbuilder.github.io. Hand this whole folder to Claude Code when working in the actual repo.

## Overview of Changes

There are 4 things to build:

1. **Homepage Built Ons section** — A new section on `index.html` that sits below the existing Templates section. Two cards (CB-Essay and OHD), same visual pattern as the template cards but with a different accent color to distinguish Built Ons from Templates.

2. **Templates page update** (`templates.html`) — Add a Built Ons section below the existing three template cards with a brief intro and the same two cards.

3. **CB-Essay page** (`/built-ons/cb-essay.html`) — Standalone page for CB-Essay.

4. **OHD page** (`/built-ons/ohd.html`) — Standalone page for Oral History as Data.

## File List

- `01-homepage-built-ons-section.md` — Content and HTML structure for the new homepage section
- `02-templates-page-update.md` — Content for the Built Ons addition to templates.html
- `03-cb-essay-page.md` — Full content for the CB-Essay standalone page
- `04-ohd-page.md` — Full content for the OHD standalone page
- `05-nav-update.md` — Nav bar changes

## Design Notes

- The CB site uses Bootstrap (visible from the class names: `container-fluid`, `row`, `col-md`, `card`, `btn-primary`, etc.) and a dark navbar with the gold CB logo.
- Template cards use a dark (`bg-dark`) card header with italic white text for the template name, a card body with an italic green description, and blue (`btn-primary`) action buttons.
- For Built Ons, use the same card structure but with a **different header color** — suggest a muted teal/green (`#2a7f62` or Bootstrap's `bg-success`) to visually distinguish Built Ons from Templates while keeping the same layout pattern. Or just use the same `bg-dark` if you want consistency — up to you.
- The homepage templates section heading is in a large italic serif font. Match that style for the Built Ons heading.

## Nav Update

The current nav is: Templates | Documentation | Tutorials | Blog | About | Join Us

Suggestion: Either add "Built Ons" as its own nav item after Templates, or make "Templates" a dropdown with "Templates" and "Built Ons" as sub-items. The dropdown approach keeps the nav clean. See `05-nav-update.md` for both options.
