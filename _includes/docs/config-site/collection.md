{:.py-4 .mt-4 #coll}
***


## Collection Settings

{% include bootstrap/image.md img="/config/coll.jpg" %}

{% capture coll-title %}
These are settings specific to your CONTENTdm collection:
{% endcapture %}

{% capture coll-text %}
- **cdm-collection-id**: The name of your CONTENTdm collection (a collection alias assigned by a collection's creator in CONTENTdm).    
    - example --> `cdm-collection-id: boxing` 

- **metadata**: The filename (not including the extension) of your CSV metadata file. 
	- ***Note: This should be the same entry as "data" in the page gen variables below.***
	- example --> `title: boxing`
{% endcapture %}

{% include bootstrap/card.md title=coll-title text=coll-text %}

{% capture pagegen-title %}
The following Page Gen variables read your metadata file and build individual html pages based on that metadata:
{% endcapture %}

{% capture pagegen-text %}
- **data**: The name of your metadata file. (This is different for every collection).
	- ***Note: This should be the same entry as "metadata" above***
	- example --> `title: boxing`

"Data" is the only field you need to change. Leave the following fields the way they are in the _config.yml template you downloaded:

- **template**: The layout of the pages generated. 
	- CollectionBuilder entry --> `items`

- **name**: Determines how the url will be written. For CollectionBuilder, we use is the "*objectid*" metadata field to generate the url.
	- CollectionBulider entry --> `objectid`

- **dir**: Determines the directory or folder in which the item pages are stored when the site is built. 
	- CollectionBuilder entry --> `items`

- **extension**: Determines the extension of each generated page. For us, `html` means our item pages will end as '.html' 
	- CollectionBuilder entry --> `html`

{% endcapture %}

{% include bootstrap/card.md title=pagegen-title text=pagegen-text %}

{% include bootstrap/card.md title="The last variable to fill in is the Google Analytics ID, if you have one:" text="- **google-analytics-id**: Enter your Google Analytics ID here." %}

{% capture pagealert %}
**Important!:** You *must* change the data field in **Page Gen** to reflect the metadata CSV the collection is using. ***This should be the same entry as "metadata" above***
{% endcapture %}

{% include bootstrap/alert.md text=pagealert color="success" %}