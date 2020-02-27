---
title: Locations Page
stub: locations
section: theme
section_order: 7
---

{:.py-4 .mt-4 #locations}
***


## Locations Page

{% include bootstrap/image.md img="/theme/locations.jpg" %}

{% capture location-text %}

This page functions exactly as the Subjects page does. 

- **locations-fields**: Choose metadata fields from your collection metadata CSV to be included in the Locations page tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- When this field is left blank, locations will not be generated and the tag cloud on the Locations page will be blank. 
	- ***Important note:*** You must also remove the "Locations" line from the [_data/config-nav.csv](customize#config-nav) in order to remove the Locations page from the site completely.
	- example --> `location;stadium`

- **locations-min**: Minimum number of times a location term must appear before being displayed in the tag cloud. 
	- Use this to improve load and build times. Too many terms = slow load time!
	- Range: `1` - `30` (note that a really large number will likely make no locations appear)
	- example --> `location-min: 1`

- **locations-stopwords**: A set of words/phrases to be removed from the tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `stopwords: Moscow;Pullman`
{% endcapture %}

{% include bootstrap/card.md text=location-text %}