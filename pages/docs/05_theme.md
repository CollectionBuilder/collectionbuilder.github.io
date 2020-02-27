---
layout: docs
title: Theme File (/_data/theme.yml)
permalink: /docs/theme.html
step: 5
---

{% assign parts = site.docs | where: 'section','theme' | sort: 'section_order' %}

{{ parts }}