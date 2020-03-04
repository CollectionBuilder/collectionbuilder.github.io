---
layout: docs
title: Finish
permalink: /docs/finish.html
section: finish
step: 7
---

{% assign parts = site.docs | where: 'section','finish' | sort: 'section_order' %}

{{ parts }}