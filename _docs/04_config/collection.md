---
title: Collection Settings
stub: coll
section: config
section_order: 3
---

{:.py-4 .mt-4 #coll}
***

## Collection Settings

These are settings specific to your collection:

- **metadata**: The filename (not including the extension) of your CSV metadata file. 
	- ***Note: This should be the same entry as "data" in the page gen variables below.***
	- example --> `metadata: boxing`

{:.alert .alert-info}
**GH users**: At this point you can skip to the [Additional Variables](#additional) section below.

#### Required Settings for CDM

- **cdm-collection-id**: The name of your CONTENTdm collection (a collection alias assigned by a collection's creator in CONTENTdm).    
    - example --> `cdm-collection-id: boxing` 

- **cdm-url** (for CONTENTdm skin): This is the url for your CONTENTdm server.
	- example --> `cdm-url: https://cdm12345.contentdm.oclc.org`

{% capture pagegen-title %}
Page Generation Settings
{% endcapture %}

{% capture pagegen-text %}
**For CDM and SA users**: The following variables are used by the "Page Gen" plugin included with CollectionBuilder.
The plugin generates individual HTML pages for each item (row) in your collection's metadata (CSV):

{:.pt-1}
- **data**: The name of your metadata file. 
	- ***This should be the same entry as "metadata" above***
	- example --> `data: boxing`

{:.typefilter .alert .alert-warning}
**Important! -->** **CDM and SA Users**, you *must* change the data field in 'Page Gen' to reflect the metadata CSV the collection is using. ***This should be the same entry as "metadata" above***.

"Data" is the only field you need to change. Leave the following fields the way they are in the default _config.yml template you downloaded:

- **template**: The layout of the pages generated. 
	- CollectionBuilder entry --> `items`

- **name**: Determines how the url will be written. For CollectionBuilder, we use is the "*objectid*" metadata field to generate the url.
	- CollectionBuilder entry --> `objectid`

- **dir**: Determines the directory or folder in which the item pages are stored when the site is built. 
	- CollectionBuilder entry --> `items`

- **extension**: Determines the extension of each generated page. For us, `html` means our item pages will end as '.html' 
	- CollectionBuilder entry --> `html`

{:.alert}
"Page Gen" used by CollectionBuilder is a modified version of the Jekyll plugin [jekyll-datapage_gen](https://github.com/avillafiorita/jekyll-datapage_gen) created by Adolfo Villafiorita. Thank you Adolfo!

{% endcapture %}

{:.cdm .typefilter}
{% include bootstrap/card.md header=pagegen-title text=pagegen-text %}