---
layout: docs
title: Install Software
permalink: /docs/software.html
section: software
step: 1
---

{% assign parts = site.docs | where: 'section','software' | sort: 'section_order' %}

{{ parts }}

