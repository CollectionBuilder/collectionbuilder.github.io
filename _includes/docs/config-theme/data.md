{:.py-4 .mt-4 #data}
***

## Data Download

{% include bootstrap/image.md img="/theme/data.jpg" %}

{% capture data-text %}

{% include bootstrap/alert.md text="For the Data section, copy and paste the first row of your collection metadata CSV (i.e. your metadata fields) into this variable. This variable determines what metadata will be made available for download via the 'Download Data' options on the Home page and on the Data page." color="success" %} 

- **metadata-export-fields**: A list of metadata fields available for export via data downloads.
	- *Tip*: paste in first row of csv 
	- Format: Comma delimited list contained between quotes
	- example --> `metadata-export-fields: "title,description,subject,date,date is approximate,source,latitude,longitude,subject (lcsh),format-original,donor,identifier,format,language,type,rights,rightsstatement,cdmid,objectid"`

- **metadata-facets-fields**: Generates a facets list download option for given fields.
	- Format: Comma delimited list contained between quotes
	- example --> `metadata-facets-fields: "subject,locations,format"`
{% endcapture %}

{% include bootstrap/card.md text=data-text %}