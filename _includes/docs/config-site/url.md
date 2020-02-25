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

{% capture cdm-url %}
- **cdm-url** (for CONTENTdm skin): This is the url for your CONTENTdm server.
	- example --> `cdm-url: https://cdm12345.contentdm.oclc.org`
{% endcapture %}
{:.cdm .typefilter}
{% include bootstrap/alert.md text=cdm-url color="secondary" %}

- **source-code**: Indicates the GitHub repository that hosts your CollectionBuilder code.
	- example --> `source-code: https://github.com/CollectionBuilder`
{% endcapture %}

{% include bootstrap/card.md title=var-title text=var-text %}