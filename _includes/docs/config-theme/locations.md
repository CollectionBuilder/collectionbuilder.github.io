{:.py-4 .mt-4 #locations}
***


## Locations Page

{% include bootstrap/image.md img="/theme/locations.jpg" %}


{% capture location-text %}

{% capture location %}
***Important note:*** In order to have this page appear on your site, you must also add a row in the [_data/config-nav.csv](customization.html#config-nav) that reads: `Locations,locations.html`.
{% endcapture %}

{% include bootstrap/alert.md text=location color="success" %}

This page functions exactly as the Subjects page does. 

- **locations-page**: Turns location generation on (`true`) or off (`false`). 
	- Options: `true`, `false`
	- example --> `locations-off: false`

- **locations-fields**: Chooses metadata fields from your collection metadata CSV to be included in the Location page tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `location;stadium`

- **locations-min**: Minimum number of times a location term must appear before being displayed in the tag cloud. 
	- Use this to improve load and build times. Too many terms = slow load time!
	- Range: `1` - `30` (note that a really large number will likely make no subjects appear)
	- example --> `location-min: 1`

- **locations-stopwords**: A set of words/phrases to be removed from the tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `stopwords: Moscow;Pullman`
{% endcapture %}

{% include bootstrap/card.md text=location-text %}