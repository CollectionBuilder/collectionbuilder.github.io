---
layout: docs
title: Metadata
permalink: /docs/metadata.html
section: metadata
step: 3
noindex: true
---

{% assign parts = site.docs | where: 'section','metadata' | sort: 'section_order' %}

{{ parts }}