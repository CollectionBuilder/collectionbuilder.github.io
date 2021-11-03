---
title: In the Wild
sectionid: wild
section_order: 7
---
## How are others using CollectionBuilder?

CollectionBuilder sites continue to proliferate around the world. Below is a list of sites we've noticed "in the wild."

{% capture wild %}
*Select digital collections from users outside of University of Idaho.*
{% for w in site.data.cb-in-wild %}
- [{{ w.title }}]({{ w.link }}), {{ w.org }}{% endfor %}
{% endcapture %}
{% include bootstrap/card.md title="CollectionBuilder in the Wild" text=wild %}