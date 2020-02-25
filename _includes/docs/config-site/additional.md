{:.py-4 .mt-4 #add}
***


## Additional Variables

{% include bootstrap/image.md img="/config/add.jpg" %}

{% capture addalert %}
The following is for informational purposes only. You don't need to change anything else in **_config.yml**.
{% endcapture %}

{% include bootstrap/alert.md text=addalert color="info" %}

{% capture add-title %}
These are Git- and Liquid-based variables to help with building the site and recording the changes via Git. You should probably just leave them as they are. 
{% endcapture %}

{% capture add-title %}
These are Git- and Liquid-based variables to help with building the site and recording the changes via Git. You should probably just leave them as they are. 
{% endcapture %}

{% capture add-text %}
{% capture profile %}
- **profile**: Allows Liquid to determine bottlenecks via a commandline command.
{% endcapture %}
{:.cdm .typefilter}
{% include bootstrap/alert.md text=profile color="secondary" %}

- **exclude**: Tells git which files and folders not to track when tracking the changes. 

- **sass**: Controls how the CSS is build when the site is being rendered. 
{% endcapture %}

{% include bootstrap/card.md title=add-title text=add-text %}

{:.py-4 .mt-4}
***