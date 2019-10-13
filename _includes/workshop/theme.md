The **theme.yml** file controls CollectionBuilder's display options. These variables impact every page the site builds, so you should be sure to go through each one as you create your site.

{% include bootstrap/alert.md text="Before you start, locate and open the **theme.yml** file in the repository's **_data** folder.

This file controls bits of almost every page used, including: " color="success" %}

- [Home Page](#home)
- [Browse Page](#browse)
- [Item Page](#item)
- [Map Page](#map)
- [Subjects Page](#subjects)
- [Locations Page](#locations)
- [Timeline Page](#timeline)
- [Data Page](#data)
- [Advanced Theme Options](#advanced)

{:.py-4 .mt-4 #home}
***

## Home Page

{% include bootstrap/image.md img="/theme/home.jpg" %}

{% capture home-text %}

{% include bootstrap/alert.md text="**Note:** The features that display on the home page can be customized via the 'home-infographic.html' file in the layouts folder. More on customizing that file can be found in our [finishing section](finishing.html#home)" color="success" %} 

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

- **carousel-type**: Determines the type of object you'd like shown in the carousel on the home page.
	- Options: `image`,`pdf`,`youtube`,`thumbs`
	- example --> `carousel-type: image`

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

{:.py-4 .mt-4 #browse}
***

## Browse Page

{% include bootstrap/image.md img="/theme/browse.jpg" %}

{% include bootstrap/card.md text="See our [Customizations page](customization.html) and the `config-browse.csv` in the **_data** folder to configure the Browse page." %}


{:.py-4 .mt-4 #item}
***

## Item Page 

{% include bootstrap/image.md img="/theme/item.jpg" %}

{% capture item-text %}
- **browse-buttons**: Adds previous/next arrows to items, but doubles build time. 
	- *Tip*: We usually add these at the end. They're a nice feature for improved browsing, as they let users use the mouse or the right and left arrow keys to move through the collection. 
	- Options: `true`, `false`
	- example --> `browse-buttons: true`
{% endcapture %}

{% include bootstrap/card.md text=item-text %}

{:.py-4 .mt-4 #map}
*** 

## Map Page

{% include bootstrap/image.md img="/theme/map.jpg" %}

{% capture map-text %}
- **latitude**: Determines the center of map.
	- example --> `latitude: 46.727485 `

- **longitude**: Determines the center of map.
	- example --> `longitude: -117.014185`

- **zoom-level**: Determines the zoom level for your map. The higher the number, the more zoomed-in you'll be. 
	- Range: any whole number between [`0` - `18`]
	- example --> `zoom-level: 5`

**The fields below determine *map search* and *map cluster* features. For larger collections with many items at one spot, we recommend turning on the map-cluster option and turning off the map-search feature.**

- **map-search**: Enables a user to search the map via the large magnifying glass on the top right. 
	- Not suggested for large collections.
	- Options: `true`, `false`
	- example --> `map-search: true`

- **map-search-fuzziness**: Allows for less precision with search terms. 
	- Range:
		- `0` = exact match only
		- `1` = anything
	- example --> `map-search-fuzziness: 0.35`

- **map-cluster**: Clusters markers that are near each other.
	- Suggested for large collections or for collections with many items in same location.
	- Options: `true`, `false`
	- example --> `map-cluster: true`

- **map-cluster-radius**: Determines the size of clusters
	- Range: `10` to `80`
	- example --> `map-cluster-radius: 25`
{% endcapture %}

{% include bootstrap/card.md text=map-text %}

{% capture mapalert %}
*Tip*: A user can change the layer the map is using by clicking on the Layer button at the top right of the map. The map can be searched by clicking on the magnifying glass just below the layers option at the top right. 
{% endcapture %}


{:.py-4 .mt-4 #subjects}
***

## Subjects Page

{% include bootstrap/image.md img="/theme/subjects.jpg" %}

{% capture subject-text %}
- **subjects-page**: Turns subject generation on (`true`) or off (`false`). 
	- `false` lowers dev build time (Note: If you turn it off, the page won't work!!)
	- Options: `true`, `false`
	- example --> `subjects-off: false`

- **subjects-fields**: Chooses metadata fields from your collection metadata CSV to be included in the Subjects page tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `subject;creator`

- **subjects-min**: Minimum number of times a subject term must appear before being displayed in the tag cloud. 
	- Use this to improve load and build times. Too many terms = slow load time!
	- Range: `1` - `30` (note that a really large number will likely make no subjects appear)
	- example --> `subject-min: 4`

- **subjects-stopwords**: A set of words/phrases to be removed from the tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `stopwords: boxers;boxing;boxer`
{% endcapture %}

{% include bootstrap/card.md text=subject-text %}

{:.py-4 .mt-4 #locations}
***


## Locations Page

{% include bootstrap/image.md img="/theme/locations.jpg" %}


{% capture location-text %}

{% capture location %}
***Important note:*** In order to have this page appear on your site, you must also add a row in the [_data/config-nav.csv](customization.html#config-nav) that reads: `Locations,locations.html`.
{% endcapture %}

{% include bootstrap/alert.md text=location color="success" %}

This page functions exactly as the Subjects page does. 

- **locations-page**: Turns location generation on (`true`) or off (`false`). 
	- Options: `true`, `false`
	- example --> `locations-off: false`

- **locations-fields**: Chooses metadata fields from your collection metadata CSV to be included in the Location page tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `location;stadium`

- **locations-min**: Minimum number of times a location term must appear before being displayed in the tag cloud. 
	- Use this to improve load and build times. Too many terms = slow load time!
	- Range: `1` - `30` (note that a really large number will likely make no subjects appear)
	- example --> `location-min: 1`

- **locations-stopwords**: A set of words/phrases to be removed from the tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `stopwords: Moscow;Pullman`
{% endcapture %}

{% include bootstrap/card.md text=location-text %}

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

{:.py-4 .mt-4 #data}
***

## Data Download

{% include bootstrap/image.md img="/theme/data.jpg" %}

{% capture data-text %}

{% include bootstrap/alert.md text="For the Data section, copy and paste the first row of your collection metadata CSV (i.e. your metadata fields) into this variable. This variable determines what metadata will be made available for download via the 'Download Data' options on the Home page and on the Data page." color="success" %} 

- **metadata-export-fields**: A list of metadata fields available for export via data downloads.
	- *Tip*: paste in first row of csv 
	- Format: Comma delimited list contained between quotes
	- example --> `metadata-export-fields: "title,description,subject,date,date is approximate,source,latitude,longitude,subject (lcsh),format-original,donor,identifier,format,language,type,rights,rightsstatement,cdmid,objectid"`

- **metadata-facets-fields**: Generates a facets list download option for given fields.
	- Format: Comma delimited list contained between quotes
	- example --> `metadata-facets-fields: "subject,locations,format"`
{% endcapture %}

{% include bootstrap/card.md text=data-text %}

{:.py-4 .mt-4 #advanced}
***

# Advanced Theme Options

{:.py-4 .mt-4}

## Images 

{% include bootstrap/image.md img="/theme/images.jpg" %}

{% capture images-text %}

{% capture imagesalert %}
This is a CONTENTdm-specific variable section for adjusting size of images used throughout the site. 

*Tip*: If your images are appearing blurry or take too long to load, try adjusting the image-sizing settings.
{% endcapture %}

{% include bootstrap/alert.md text=imagesalert color="success" %} 

- **image-percentage-large**:
	- Default `70`
	- example --> `image-percentage-large: 50`

- **image-percentage-medium**: 
	- Default `40` 
	- example --> `image-percentage-medium: 30`

- **image-percentage-small**
	- Default `20`
	- example --> `image-percentage-small: 10`
{% endcapture %}

{% include bootstrap/card.md text=images-text %}

{:.py-4 .mt-4 #bootstrap}
***

## Bootstrap Themes

{% include bootstrap/image.md img="/theme/advanced.jpg" %}

{% capture theme-text %}

### Theme Options:

{% include bootstrap/alert.md text="These options will adjust your site's color and look." color="success" %} 


- **navbar-color**: Choose from `navbar-light` for use with light background colors, or `navbar-dark` for dark background colors navbar-dark
	- Options:  `navbar-light`, `navbar-dark`
	- example --> `navbar-color: navbar-dark`

- **navbar-background**: Choose from the background colors for Bootstrap. 
	- Options: `bg-primary`, `bg-secondary`, `bg-success`, `bg-danger`, `bg-warning`, `bg-info`, `bg-light`, `bg-dark`, `bg-white`, `bg-dark`]
	- example --> `navbar-background: bg-dark`

### Theme Fonts:

{% include bootstrap/alert.md text="These options change the way the fonts appear throughout your collection. If you leave any option blank, it will revert to the base Bootstrap 4 CSS style(s)." color="success"%}

- **base-font-size**: Changes the base size for fonts throughout the site.
	- example --> `base-font-size: 1.2em`

- **text-color**: Changes the color of the base font. Probably want a shade of gray or black ... 
	- example --> `text-color: "#191919"`

- **link-color**: Changes the link color used throughout the site. Base color is a primary blue. 
	- example --> `link-color: "#17a2b8"`

- **base-font-family**: Changes the font family; if it's a google family, you'll need to adjust the _includes/header.html file as well to include the link to Google's CSS style file for that font.
	- Comment out (using `#`) for bootstrap defaults  
	- example --> `base-font-family: Georiga; serif;`

### Bootswatch:

{% include bootstrap/alert.md text="Bootswatch creates themes for Bootstrap 4 sites. You can check them out here: <https://bootswatch.com/>."  color="success"%}

- **bootswatch**: leave blank or comment out for plain bootstrap
	- Options: `cerulean`, `cosmo`, `cyborg`, `darkly`, `flatly`, `journal`, `litera`, `lumen`, `lux`, `materia`, `minty`, `pulse`, `sandstone`, `simplex`, `sketchy`, `slate`, `solar`, `spacelab`, `superhero`, `united`, `yeti`
	- example --> `bootswatch: cerulean`

{% endcapture %}

{% include bootstrap/card.md text=theme-text %}




{:.py-4 .mt-4}
***

