---
title: Site Settings
stub: site
section: config
section_order: 2
---

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

{% capture gh-site %}
- **author**: You! The creator of the digital collection.
	- Use your GitHub username or your name. This will appear in the site's meta tags.
	- example --> `CollectionBuilder`

- **collection-date**: The date you published your site.
	- example --> `2020`
{% endcapture %}
{:.gh .typefilter}
{% include bootstrap/alert.md text=gh-site color="primary" %}

{% capture organization %}
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
{:.cdm .typefilter}
{% include bootstrap/alert.md text=organization color="secondary" %}

{% endcapture %}

{% include bootstrap/card.md title=site-title text=site-text %}