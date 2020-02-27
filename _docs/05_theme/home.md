---
title: Home Page
stub: home
section: theme
section_order: 1
---

{:.py-4 .mt-4 #home}
***

## Home Page

{% include bootstrap/image.md img="/theme/home.jpg" %}

{% capture home-text %}

{% include bootstrap/alert.md text="**Note:** The features that display on the home page can be customized via the 'home-infographic.html' file in the layouts folder. More on customizing that file can be found in our [finishing section](finishing.html#home)" color="info" %} 

Home Page Banner:

- **featured-image-objectid**: The objectid for the image you would like to feature on your home page. 
	- *Tip*: It's best to choose an image that is large and more "landscape" than "portrait," i.e. more horizontal than vertical. 
	- example --> `featured-image-objectid: demo-psychiana15`

- **featured-image-link**: Only use this field if you are *NOT* using an image in your collection as your featured image. Leave blank if you enter a number above for a CONTENTdm image. 
	- This will likely be a link to an outside photograph.
	- example --> `featured-image-link: https://www.example.com/picture.jpg`

- **home-title-y-padding**: Determines how much of your featured image is visible. 
	- A smaller number will feature a smaller amount of the image.
	- Range: `2em` - `20em`
	- example --> `home-title-y-padding: 12em`

- **home-banner-image-position**: Determines what portion of the image will appear. 
	- Options: `top`, `center`, `bottom`
	- example --> `home-banner-image-position: bottom`

Home Page Features:

- **carousel-height**: Determines the height of the carousel on the home page.
	- Indicates pixels, but don't include "px" in your input.
	- example --> `carousel-height: 500`

{% capture carousel-type %}
- **carousel-type**: Determines the type of object you'd like shown in the carousel on the home page.
	- Options: `image`,`pdf`,`youtube`,`thumbs`
	- example --> `carousel-type: image`
{% endcapture %}
{:.cdm .typefilter}
{% include bootstrap/alert.md text=carousel-type color="secondary" %}

- **featured-subjects**: Generates home page "subject" buttons for select subjects.
	- If left blank, automatically generates top 5 subjects. 
	- To customize, list your own curated subjects. Separate multiple subjects with a semi-colon(';'). 
	- example --> `featured-subjects: corn;soy;basketball`

- **featured-subjects-max**: Sets number of top subjects to display if **featured-subjects** is auto-generated
	- Default: `5`
	- example --> `featured-subjects-max: 6`

- **featured-locations**: Generates home page "location" buttons for select locations.
	- If left blank, automatically generates top 5 locations. 
	- To customize, list your own curated locations. Separate multiple locations with a semi-colon(';'). 
	- example --> `featured-locations: University of Idaho; Sacramento, California;`

- **featured-locations-max**: Sets number of top locations to display if **featured-locations** is auto-generated
	- Default: `5`
	- example --> `featured-locations-max: 4`

{% endcapture %}

{% include bootstrap/card.md text=home-text %}