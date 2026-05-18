---
layout: post
title: "Introducing CB-Essay and CollectionBuilder Built Ons"
subtitle: 
author: Devin Becker
publish-date: May 18, 2026
tags: [cb-add-on, announcement, cb-essay, imls]
short_description: "CB-Essay is a new CollectionBuilder Built On for writing long-form digital scholarship. We're also introducing Built Ons — frameworks that extend CollectionBuilder into new kinds of projects."
tldr: "CB-Essay is a new CollectionBuilder Built On for writing long-form digital scholarship. We're also introducing Built Ons — frameworks that extend CollectionBuilder into new kinds of projects."
---

We're excited to announce [CB-Essay](https://collectionbuilder.github.io/cb-essay/), a new framework for writing and publishing long-form digital scholarship using CollectionBuilder. We're also using this release to introduce a concept we're calling **CollectionBuilder Built Ons**.

## What Are Built Ons?

CollectionBuilder has templates — CSV, Sheets, GH — for building digital collections. Built Ons are different; they are specialized frameworks **built on top of** CollectionBuilder-CSV. (We are nothing if not literal with our naming conventions.) Built Ons use the same metadata-driven, static web approach but apply it to a different kinds of project.

We're launching two today: [CB-Essay](https://collectionbuilder.github.io/cb-essay/) for long-form digital scholarship and [Oral History as Data (OHD)](https://oralhistoryasdata.github.io/) for publishing and visualizing coded oral history interviews. A third, Digital Dramaturgy, is in development.

## CB-Essay

CB-Essay lets you write multimodal essays in Markdown and integrate items from a CollectionBuilder collection directly into your narrative — images, documents, audio, video, all referenced through simple includes. You get margin notes that link to primary sources, scroll-based section transitions, color and font theming options, well-designed print outputs, full text search, and all the standard CollectionBuilder pages (Browse, Map, Timeline, Subjects) alongside your essay.

CB-Essay grew out of work we did with three graduate students at [CDIL](https://cdil.lib.uidaho.edu/) who were building multimodal essay projects for their theses — Alicia Gladman's [Tender Spaces](https://cdil.lib.uidaho.edu/tender-spaces/), a multi-lingual essay on the life and art of Gaëtane Buttigieg, Hannah Green's [Sedimentation](https://cdil.lib.uidaho.edu/sedimentation/), an interweaved series of essays on sediment and Glen Canyon, and Isabel Marlens' [Fire Lines](https://cdil.lib.uidaho.edu/fire-lines/), an archive-driven exploration of the Legacy of 1910's Great Fire in the Northwest. These projects needed a way to combine long-form writing with collection items on the web, and the CB-Essay allowed for an ease of composition and customization for the authors and developers of the site.

A few things worth highlighting:

- You write in Markdown in an `_essay/` folder — each file is a section or chapter. Your collection metadata lives in a CSV, same as any CB project.
- There are sevearl themes to choose from that change the color and font-family of your site.
- We've added a print feature using [Paged.js](https://pagedjs.org/) that turns any essay into a nicely formatted PDF, complete with proper page breaks and layout. So your web-first essay can also exist as a print artifact when you need it to.
- There's a Project Gutenberg extractor — a GitHub Action that pulls any of 60,000+ public domain books into your essay folder, pre-formatted. This can be used for annotated editions or teaching, or just to test out the project.

Check out the [CB-Essay demo site](https://collectionbuilder.github.io/cb-essay/) — it's self-documenting, so each essay section shows off the features while teaching you how to use them. When you're ready to start, [use the template](https://github.com/CollectionBuilder/cb-essay).

## OHD is now a Built On as Well

[Oral History as Data](https://oralhistoryasdata.github.io/) has been around since 2018 and has powered long-running projects like [Voices of Gay Rodeo](https://www.voicesofgayrodeo.com/) and the [CTRL+Shift](https://ctrl-shift.org/). It transforms coded oral history transcripts into interactive, color-coded thematic visualizations — we wrote about it and other oral history projects in a [previous post](https://collectionbuilder.github.io/2024-01-29-oral-history-projects/).

OHD is now officially a Built On. It's got a [new promo site](https://oralhistoryasdata.github.io/), updated [docs](https://oralhistoryasdata.github.io/docs/), and we're aligning its infrastructure with CollectionBuilder-CSV so updates flow downstream automatically. Get started with the [OHD template](https://github.com/oralhistoryasdata/template) or explore the [demo](https://oralhistoryasdata.github.io/template/).

## IMLS Grant Reinstated

So we should have announced this a long time ago, but like many others, our IMLS grant has been reinstated. We've been using the renewed funds to backward fund projects like our student and digital librarian cohorts, and going forward, we'll be putting funds toward travel and development of new features. If you've got a big idea for a CollectionBuilder feature you'd like to see built, reach out — we may have opportunities to fund development work.

## What's Next

We're adding a Built Ons section to the CollectionBuilder website and connecting both CB-Essay and OHD to receive automatic updates from CollectionBuilder-CSV via GitHub Actions. Digital Dramaturgy will be announced separately when it's ready.

If you've built something on CollectionBuilder that takes it in a new direction, we'd love to hear about it. Post on our [GitHub Discussion Board](https://github.com/orgs/CollectionBuilder/discussions) or email [collectionbuilder.team@gmail.com](mailto:collectionbuilder.team@gmail.com).

-Devin
