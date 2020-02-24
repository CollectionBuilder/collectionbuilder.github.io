{:.py-4 .mt-4 #timeline}
***


## Timeline Page

{% include bootstrap/image.md img="/theme/timeline.jpg" %}

{% capture timeline-text %}

{% include bootstrap/alert.md text="The Timeline page is built by year, with each year a row where thumbnail versions of the items appear. **This section will let you determine which years are in the dropdown button at the top right of the Timeline page. This button allows a user to jump down the page.** " color="success" %} 

- **year-navigation**: Sets the years to appear in Timeline dropdown nav. 
	- *Tip*: If left blank, these will auto-generate. (We recommend leaving this blank.)
	- example --> `year-navigation: 1900;1905;1910;1915;1920`

- **year-nav-increment**: Sets the increment at which the years in the Timeline dropdown nav are automatically generated. 
	- Default: `5`
	- example --> `year-nav-increment: 7`
{% endcapture %}

{% include bootstrap/card.md text=timeline-text %}