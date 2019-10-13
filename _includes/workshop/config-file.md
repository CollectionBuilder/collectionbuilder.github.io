
Our CONTENTdm skin uses the CONTENTdm API to generate the images, pdfs, and other downloadable files that make up your CollectionBuilder collection. To connect your CONTENTdm collection to CollectionBuilder, use the **_config.yml** file. 

The instructions below outline the edits you need to make to this file so that it connects to CONTENTdm. 

{% include bootstrap/alert.md text="Before you start, locate and open the **_config.yml** file in the base of your repository." color="success" %}

- [URL Variables](#url-var)
- [Site Settings](#site)
- [Collection Settings](#coll)
- [Additonal Variables](#add)

{:.py-4 .mt-4 #url-var}
***


## URL Variables

{% include bootstrap/image.md img="/config/urlvar.jpg" %}

{% capture var-title %}
These variables should be defined based on the url you will use to serve your site:
{% endcapture %}

{% capture var-text %}
- **url**: Represents the url where the site will ***eventually*** reside. This will be used to generate links when you build the site at the end of your customization process. 
	- example --> `url: https://www.lib.uidaho.edu`
	- example --> `url: https://dcnb.github.io`

- **baseurl**: Indicates the folders where your site will be located on your web server. 
	- For example, if you have a project called "*pink-poodle*" that you plan to put in the "*projects*" folder on your website, you'd put `/projects/pink-poodle` down for this variable. 
	- example --> `baseurl: /digital/boxing` 
	- ***Note: Each of your collections will have a unique project name, so you will need to adjust the **baseurl** setting for each collection you build.***

- **cdm-url**: This is the url for your CONTENTdm server.
	- example --> `cdm-url: https://cdm12345.contentdm.oclc.org`

- **source-code**: Indicates the GitHub repository that hosts your CollectionBuilder code.
	- example --> `source-code: https://github.com/CollectionBuilder`
{% endcapture %}

{% include bootstrap/card.md title=var-title text=var-text %}

{:.py-4 .mt-4 #site}
***


## Site Settings

{% include bootstrap/image.md img="/config/site.jpg" %}

{% capture site-title %}
These are the primary settings of your site:
{% endcapture %}

{% capture site-text %}
- **title**: The title of your digital collection. 
	- This will appear as the title on the home page and on every other page's header. 
	- example --> `title: Donald R. Theophilus Boxing Photograph Collection`

- **tagline**: A descriptive subtitle of the digital collection.
	- This will appear underneath the title on the home page and on every other page's header.
	- example --> `tagline: Photographs of University of Idaho Boxers and Boxing Teams, 1934 - 1953`

- **description**: One or two sentences of explanatory text about the collection.
	- Appears on the home page under the featured image.
	-  example --> `description: "A digital collection comprised of 52 photographs of boxers and boxing teams from the University of Idaho"`

- **organization-name**: The name of your organization.
	- Used to reference your organization in the site's citation, and serves as alternate text for your organization logos.
	- example --> `"Digital Initiatives, University of Idaho Library"`

- **organization-link**: A link to your organization's homepage.
	- This is the url connected to your organization name.
	- example --> `https://www.lib.uidaho.edu/digital/`

- **organization-logo-nav**: The image source for your organization logo that appears above your site title. 
	- This image will appear above the **title** on your collection's homepage. This logo is connected to the **organization-link** url you entered above.
	- example --> `https://www.lib.uidaho.edu/media/digital/bannerlogo_allwhite.png`

- **organization-logo-banner**: The image source for your organization logo that appears at the top right of the screen on all pages *except* the home page.
	- This logo is connected to the **organization-link** url you entered above.
	- example --> `https://www.lib.uidaho.edu/media/digital/justdi_logo_sm.png`

{% endcapture %}

{% include bootstrap/card.md title=site-title text=site-text %}

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

{:.py-4 .mt-4 #add}
***


## Additional Variables

{% include bootstrap/image.md img="/config/add.jpg" %}

{% capture addalert %}
The following is for informational purposes only. You don't need to change anything else in **_config.yml**.
{% endcapture %}

{% include bootstrap/alert.md text=addalert color="success" %}

{% capture add-title %}
These are Git- and Liquid-based variables to help with building the site and recording the changes via Git. You should probably just leave them as they are. 
{% endcapture %}

{% capture add-title %}
These are Git- and Liquid-based variables to help with building the site and recording the changes via Git. You should probably just leave them as they are. 
{% endcapture %}

{% capture add-text %}
- **Profile**: Allows Liquid to determine bottlenecks via a commandline command.

- **exclude**: Tells git which files and folders not to track when tracking the changes. 

- **sass**: Controls how the CSS is build when the site is being rendered. 
{% endcapture %}

{% include bootstrap/card.md title=add-title text=add-text %}

{:.py-4 .mt-4}
***