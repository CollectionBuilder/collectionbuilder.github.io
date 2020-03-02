---
title: Additional Variables
stub: additional
section: config
section_order: 4
---

{:.py-4 .mt-4 #add}
***

## Additional Variables

{:.alert .alert-success}
For **all user-types**, the following settings in **_config.yml** are optional. Your site will work successfully without changing the variables below.

{% include bootstrap/card.md title="Google Analytics" text="Fill in your Google Analytics ID, if you have one: 
- **google-analytics-id**: Enter your Google Analytics ID here." %}

{% include bootstrap/card.md title="Robots Exclude" text=" 
- **noindex**: Set to true if you do NOT want Google to index your site
    - example -> `noindex: true`" %}


{% capture add-title %}
Build Settings
{% endcapture %}

{% capture add-text %}
These are Git- and Liquid-based variables to help with building the site and recording the changes via Git. You should probably just leave them as they are. 

- **exclude**: Tells git which files and folders not to track when tracking the changes. 

- **sass**: Controls how the CSS is built when the site is being rendered. 
{% endcapture %}

{% include bootstrap/card.md title=add-title text=add-text %}
