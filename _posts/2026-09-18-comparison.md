---
layout: post
title: 'Image comparison feature'
subtitle:
author: Evan Williamson
publish-date: Sep 18, 2026
tags: [tech]
short_description: 'Using before-after to add an image comparison feature option to CB-CSV.'
---

Ever want to add an image comparison feature to your CB project? 

Lucky you: the option is NOW available!

We just added an include feature and display template to CB-CSV using [Before-After Image Comparison Slider](https://github.com/markpbaggett/before-after), a lightweight web component library for comparing two images, created by markpbaggett for TAMU Library.
Think an updated, modern, more feature rich [JutxaposeJS](https://juxtapose.knightlab.com/), built using your CB items!

The new include (["_includes/feature/image-comparison.html"](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/main/_includes/feature/image-comparison.html)) adds an interactive comparison of any two images stacked on top of each other with a slider to reveal one or the other (or fade between them using opacity), ready for any page in your site.
Check the "comment" section at the top of the include file for all the options--horizontal, vertical, or opacity, this is fully featured!

The new `image_comparison` display_template option uses our "compound object" metadata convention to set up the comparison as a standard Item page option.
The comparison display options can be customized in the front matter of the [item layout](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/main/_layouts/item/image_comparison.html).
Check out the [demo image comparison item](https://compound-1lqv.onrender.com/items/comp001.html) and the [docs](https://collectionbuilder.github.io/cb-docs/docs/metadata/compound-objects/#image_comparison).
