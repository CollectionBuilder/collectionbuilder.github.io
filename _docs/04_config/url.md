---
title: URL Variables
stub: url
section: config
section_order: 1
---

{:.py-4 .mt-4 #url}
***

## URL Variables

These variables should be defined based on the url you will use to serve your site:

- **url**: Represents the url where the production site will ***eventually*** reside. This will be used to generate links when you (or GitHub Pages) build the site at the end of your customization process. 
	- On GitHub Pages, `url` will follow the pattern of `<your github user name>.github.io`
	- example on GitHub Pages --> `url: https://dcnb.github.io`
	- If self hosting, the `url` will be the domain or subdomain where you will be placing the site.
	- example --> `url: https://www.lib.uidaho.edu`

- **baseurl**: Indicates the folder where your site will be located on your web server. 
	- When using GH on GitHub Pages, the `baseurl` will be the name of your project repository.
	- example on GitHub Pages --> `baseurl: /example-collection`
	- If self hosting, the `baseurl` will be the folder where you would like to host the site (if applicable). For example, if you have a project called "*pink-poodle*" that you plan to put in the "*projects*" folder on your website, you'd put `/projects/pink-poodle` down for this variable. 
	- example for a site to be at <https://www.lib.uidaho.edu/digital/boxing> --> `baseurl: /digital/boxing` 
	- ***Note: Each of your collections will have a unique project name, so you will need to adjust the `baseurl` setting for each collection you build.***

- **source-code**: Indicates the GitHub repository that hosts your CollectionBuilder project code.
	- example --> `source-code: https://github.com/CollectionBuilder`
