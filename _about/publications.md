---
title: Publications
sectionid: publications
section_order: 7
---

## Where can I learn more?

We've presented and written **_a lot_** about CollectionBuilder. Below is a list of our publications, workshops, and presentations. 

{% capture publications %}
{% assign pubs = site.data.cb-publications | where: 'type','Article' %}
{% for p in pubs %}
- {{ p.authors }}, **"{{ p.title }}"**, {{ p.publication }}, {{ p.date }}{% if p.link %}, <{{ p.link }}>{% endif %}{% endfor %}
{% endcapture %}
{% include bootstrap/card.md title="CollectionBuilder Publications" text=publications %}

{% capture presentations %}
{% for p in site.data.cb-publications %}{% unless p.type == "Article" %}
- *{{ p.type }}:* {{ p.authors }}, **"{{ p.title }}"**, {{ p.publication }}, {{ p.date }}{% if p.link %}, <{{ p.link }}>{% endif %}{% endunless %}{% endfor %}
{% endcapture %}
{% include bootstrap/card.md title="CollectionBuilder Presentations and Workshops" text=presentations %}