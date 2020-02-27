---
title: Item Page
stub: item
section: theme
section_order: 4
---

{:.py-4 .mt-4 #item}
***

## Item Page 

{% include bootstrap/image.md img="/theme/item.jpg" %}

{% capture item-text %}
- **browse-buttons**: Adds previous/next arrows to items, but doubles build time. 
	- *Tip*: We usually add these at the end. They're a nice feature for improved browsing, as they let users use the mouse or the right and left arrow keys to move through the collection. 
	- Options: `true`, `false`
	- example --> `browse-buttons: true`
{% endcapture %}

{% include bootstrap/card.md text=item-text %}