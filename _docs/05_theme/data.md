---
title: Data Download
stub: data
section: theme
section_order: 9
---

{:.py-4 .mt-4 #data}
***

<div class="row" markdown="1">
## Data Download

{% include bootstrap/image.md img="/theme/data.jpg" %}

<div class="col-md-8" markdown="1">
- **metadata-export-fields**: A list of metadata fields available for export via data downloads.
	- Paste in first row of csv 
	- Format: Comma delimited list contained between quotes
	- example --> `metadata-export-fields: "title,description,subject,date,date is approximate,source,latitude,longitude,subject (lcsh),format-original,donor,identifier,format,language,type,rights,rightsstatement,cdmid,objectid"`

- **metadata-facets-fields**: Generates a facets list download option for given fields.
	- Format: Comma delimited list contained between quotes
	- example --> `metadata-facets-fields: "subject,locations,format"`
</div>

<div class="col-md-4" markdown ="1">
{% include bootstrap/alert.md color="info" text="**Tip:** For the **metadata-export-fields** section, copy and paste the first row of your collection metadata CSV (i.e. your metadata fields) into this variable. 

This variable determines what metadata will be made available for download via the 'Download Data' options on the Home page and on the Data page." %} 
</div>
</div>