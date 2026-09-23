---
layout: post
title: 'Experimenting with Image Embeddings Search'
subtitle:
author: Evan Williamson
publish-date: July 24, 2026
tags: [tech, cb-add-on]
short_description: 'Testing client-side embedding models that can be used for search in a CB-CSV project.'
---

At DHSI 2026, Theresa Engelbrecht was working on a prototype for the [Printer's Marks and Chops Archive](https://tmengelb.github.io/cb-pmcarchive/) (or visit the current [PMCarchive site](https://printersmarks.org/)). 
In a follow up meeting with Theresa and her collaborator Andrew Saluti, they asked an innocent question--could CollectionBuilder have a reverse image search feature?

My initial thought was: no, absolutely impossible! 
But, A LOT has changed recently with AI models and ways you can run complex code in the browser, which sent me off on a side quest...

To experiment with the idea of adding image-based search to a static web (CollectionBuilder) project, I set up [embeddings-search-explore](https://evanwill.github.io/embedding-search-explore/embeddings.html).
It uses client-side, local embedding model to provide vector search from image or text.
The idea is to create a compact numerical representation of the collection images, then let visitors find visually similar items by uploading an image or describing what they are looking for--and in this context simply to explore how AI-powered search can work in a collection without relying on a traditional backend or external services.

Embeddings are compact numeric vectors that quantify the "shape" or "meaning" of an item in a way a computer can compare efficiently. 
For images, an embedding summarizes features such as color, texture, structure, and composition. 
Visually similar images end up closer together in that vector space.

To create the search feature, first the collection items are processed with an embeddings model to generate a vector-based index.
When a user visits the embeddings search page, they load the index and the same model in their browser.
The model then processes their search image or text, and returns similar items from the index based on the embeddings.
None of the collection's normal text metadata is involved in the process.

To use client-side and self-contained in a browser without any 3rd party services, the model needs to run in javascript and be small enough to reasonably load on the web.
This prototype implementation uses [Transformers.js](https://huggingface.co/docs/transformers.js) and [CLIP ViT-B/32](https://huggingface.co/Xenova/clip-vit-base-patch32) (about 85 MB, which is kind of pushing reasonable size limit...).
[CLIP (Contrastive Language-Image Pre-Training)](https://github.com/openai/CLIP) is a neural network that can process both images and text into the same vector space.
The pre-processing is automated using a Rake task, which uses Nodejs for the processing (to mirror the JS available in the browser).
The exact same packages are used both in the pre-processing and browser-based search to ensure consistent results. 

The results are varied--sometimes really useful and interesting, sometimes totally mysterious.
There is interesting possibilities for similarity search and discovery beyond metadata keywords, especially when the collection lacks consistent labels or when users want to find related imagery rather than exact matches.
Users are able to search beyond traditional metadata, exploring by resemblance, mood, or visual similarity.
You could set up this basic search of image content without any descriptive metadata at all--enabling basic discovery to undescribed images without needing to officially assign potentially inaccurate metadata.

I plan on packaging this implementation as a [cb-add-on](https://collectionbuilder.github.io/add-ons.html) so others can try it out.
There is a lot more to explore!
