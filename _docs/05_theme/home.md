---
title: Home Page
stub: home
section: theme
section_order: 1
---

{:.py-4 .mt-4 #home}
***

## Home Page

{% include bootstrap/alert.md text="**Note:** The features that display on the home page can be customized via the 'home-infographic.html' file in the layouts folder. More on customizing that file can be found in our [finishing section](finish.html#home-page)" color="success" %} 

Home Page Banner:

- **featured-image**: This is the image that appears at the top of the home page of your collection. It can be ***one*** of the following:  
	- the objectid for the image from this collection that you would like to feature on your home page
		- example --> `featured-image: demo_psychiana15`
	- ***OR*** a relative location of an image in your repository
		- example --> `featured-image:  /images/palouse.jpg`
	- ***OR*** a full URL to an image elsewhere.  
		- example --> `featured-image: https://ctrl-shift.org/images/splash/armantrout.jpg`
	- if you leave `featured-image` blank or comment it out, the home page of your collection will have the standard page banner with no image background.

{% include bootstrap/alert.md text="**Tip**: It's best to choose a large image for the featured image, one that is more 'landscape' than 'portrait,' i.e. more horizontal than vertical." color="info"%}

- **home-title-y-padding**: Determines how much of your featured image is visible by adding padding above and below the collection banner. 
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
#### CDM and SA Only:
- **carousel-type**: Determines the type of object you'd like shown in the carousel on the home page.
	- Options: `image`,`pdf`,`youtube`,`thumbs`
	- example --> `carousel-type: image`
{% endcapture %}
{% include bootstrap/alert.md text=carousel-type color="secondary" %}

- **featured-subjects**: Generates home page "subject" buttons for select subjects.
	- If left blank, automatically generates top 5 subjects. (We typically leave it blank.)
	- To customize, list your own curated subjects. Separate multiple subjects with a semicolon(';'). 
	- example --> `featured-subjects: corn;soy;basketball`

- **featured-subjects-max**: Sets number of top subjects to display if **featured-subjects** is auto-generated
	- Default: `5`
	- example --> `featured-subjects-max: 6`

- **featured-locations**: Generates home page "location" buttons for select locations.
	- If left blank, automatically generates top 5 locations.  
	- To customize, list your own curated locations. Separate multiple locations with a semicolon(';'). 
	- example --> `featured-locations: University of Idaho; Sacramento, California;`

- **featured-locations-max**: Sets number of top locations to display if **featured-locations** is auto-generated
	- Default: `5`
	- example --> `featured-locations-max: 4`