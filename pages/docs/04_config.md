---
layout: docs
title: Config File
permalink: /docs/config.html
section: config
step: 4
---

{% assign parts = site.docs | where: 'section','config' | sort: 'section_order' %}

{{ parts }}