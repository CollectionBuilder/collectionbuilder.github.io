---
layout: docs
title: Theme File
permalink: /docs/theme.html
section: theme
step: 5
noindex: true
---

{% assign parts = site.docs | where: 'section','theme' | sort: 'section_order' %}

{{ parts }}