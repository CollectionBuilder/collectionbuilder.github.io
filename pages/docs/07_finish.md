---
layout: docs
title: Finish
permalink: /docs/polish.html
section: finish
step: 7
---

{% assign parts = site.docs | where: 'section','finish' | sort: 'section_order' %}

{{ parts }}