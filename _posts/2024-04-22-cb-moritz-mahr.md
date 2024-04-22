---
layout: post
title: "Q&A with Moritz Mähr, Stadt.Geschichte.Basel and cb-translate"
subtitle: 
author: Julia Stone; Moritz Mähr
publish-date: April 22, 2024
tags: [project spotlight]
short_description: In this post, CB Community Liaison Julia Stone reflects upon her time with the CollectionBuilder team and discusses what she is looking forward to next in her career journey. 
---

{% include feature/image.html objectid="/images/blog/stadt-geschichte.-basel.png" link="https://forschung.stadtgeschichtebasel.ch/" alt="Home page for the Stadt.Geschichte.Basel project" target="blank" %}

As part of our CollectionBuilder Project Spotlight Q&A series, **Moritz Mähr**, Associate Researcher in Digital Humanities at the University of Bern and digital Project Manager of [Stadt.Geschichte.Basel](https://forschung.stadtgeschichtebasel.ch/){:target="_blank" rel="noopener"} at the University of Basel, shares how he has used CollectionBuilder and contributed to the development of the [cb-translate template](https://github.com/CollectionBuilder/cb-translate){:target="_blank" rel="noopener"}.

<hr>

### 1. Please describe the [Stadt.Geschichte.Basel project](https://forschung.stadtgeschichtebasel.ch/){:target="_blank" rel="noopener"} and any other experiences you have with using CollectionBuilder.

Stadt.Geschichte.Basel is a significant historical research project at the University of Basel in Switzerland, funded with over 9 million Swiss Francs from public and private sources, running from 2017 to 2025. 

The project chronicles the extensive history of Basel from its beginnings to the present in ten printed volumes. It explores long-term developments through three research perspectives: interconnectedness and multilocality, humans and non-humans, and continuities and discontinuities. These perspectives help understand Basel's history in local, regional, and global contexts, examining the roles of humans, animals, and objects without strict chronological divisions.

The project draws on a range of sources--historical paintings, archaeological site photographs, maps, and quantitative data from statistical yearbooks, among others. The variety of topics and authors is reflected in the diverse formats provided, from scanned prints and self-made diagrams to bar charts created with standard office software and georeferenced historical city maps.

To make these resources accessible to a wider audience, we use CollectionBuilder, hosting an ever-growing collection of sources at [our website](https://forschung.stadtgeschichtebasel.ch/){:target="_blank" rel="noopener"}. We appreciate CollectionBuilder's simplicity and are developing [our own version on GitHub](https://github.com/Stadt-Geschichte-Basel/forschung.stadtgeschichtebasel.ch){:target="_blank" rel="noopener"}.

### 2. Please discuss your work in helping to develop the [cb-translate template](https://github.com/CollectionBuilder/cb-translate){:target="_blank" rel="noopener"}.

One challenge was the localization of CollectionBuilder, which is primarily designed for English-speaking users. We contacted the CollectionBuilder team and tried to align our goals. 

Evan Williamson and Olivia Wikle pointed out some important pillars of the CollectionBuilder philosophy that we should adhere to when implementing a prototype. After that, my team and I went ahead and implemented translations for Spanish and German, as well as some rudimentary [documentation](https://github.com/CollectionBuilder/cb-translate/blob/main/docs/localization.md){:target="_blank" rel="noopener"}.

### 3. How do you see the cb-translate template evolving? Are there new features you are interested in adding to this template?

Even though we are running it in production, I would still consider cb-translate experimental. It needs some testing and bug hunting. I also hope that other open source hackers will join us in maintaining cb-translate. 

We will try to keep up with the upstream version of [CollectionBuilder-CSV](https://github.com/CollectionBuilder/collectionbuilder-csv){:target="_blank" rel="noopener"} and translate all features as soon as possible. New features should be added to CollectionBuilder-CSV first.

### 4. What types of projects do you think would work well with the cb-translate template? 

Everything that is either not English or multilingual.

### 5. What do you see as the benefits and challenges of using CollectionBuilder templates for building digital projects?

Simplicity and use of legacy technology is the biggest advantage. It is very portable, easy to archive even for long-term purposes, and a good starting point for rapid prototyping. As soon as you stray too far from its original purpose or design philosophy, you run into problems. But this is the case with virtually all collection software (Wax, Omeka, etc.).

### 6. Do you have any future CollectionBuilder and/or cb-translate projects that you are planning to do? If so, please describe them.

We will be holding a CollectionBuilder workshop at the Digital History & Citizen Science Conference in Halle, Germany in September 2024. I hope we can encourage many other projects to use CollectionBuilder.

### 7. Anything else to add? Please feel free to share links to any resources, projects, repositories, etc.

We have implemented a lot of nice features in [our version](https://github.com/Stadt-Geschichte-Basel/forschung.stadtgeschichtebasel.ch){:target="_blank" rel="noopener"}, you should really check it out. Unfortunately we are behind in documenting them. Hopefully we will catch up by the end of 2024.

<p class="box-warning">Want to share one of your CB projects? We welcome you to contribute! Please reach out to <a href="mailto:collectionbuilder.team@gmail.com" target="_blank">collectionbuilder.team@gmail.com</a> to participate in a Q&A.</p>