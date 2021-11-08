---
title: Publications
sectionid: publications
section_order: 8
---

## Where can I learn more?

We've presented and written ***a lot*** about CollectionBuilder. Below is a list of our publications, workshops, and presentations. 

{% capture publications %}
{% for p in site.data.cb-publications %}
- *{{ p.type }}:* {{ p.authors }}, **"{{ p.title }}"**, {{ p.publication }}, {{ p.date }}{% if p.link %}, <{{ p.link }}>{% endif %}{% endfor %}
{% endcapture %}
{% include bootstrap/card.md title="CollectionBuilder Presentations" text=publications %}

