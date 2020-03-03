---
layout: docs
title: Customize
permalink: /docs/customize.html
section: customize
step: 6
---

{% assign parts = site.docs | where: 'section','customize' | sort: 'section_order' %}

{{ parts }}