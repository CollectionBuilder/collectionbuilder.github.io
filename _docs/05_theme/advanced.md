---
title: Advanced Options
stub: advancedoptions
section: theme
section_order: 10
---

{:.py-4 .mt-4 #advancedoptions}
***

# Advanced Theme Options

{:.py-4 .mt-4}

## Images 

{% include bootstrap/image.md img="/theme/images.jpg" %}

{% capture image-card %}

<div class="row" markdown="1">

<div class="col-md-8" markdown="1">
### Image Size:

**CDM-Users only**: This is a *CONTENTdm-specific* variable section for adjusting size of images used throughout the site.
CollectionBuilder uses the IIIF API to retrieve images using a percentage size option. 
The percentage must be 10% or greater.

- **image-percentage-large**:
	- Default `70`
	- example --> `image-percentage-large: 50`

- **image-percentage-medium**: 
	- Default `40` 
	- example --> `image-percentage-medium: 30`

- **image-percentage-small**
	- Default `20`
	- example --> `image-percentage-small: 10`
</div>

<div class="col-md-4" markdown ="1">
{% include bootstrap/alert.md color="info" text="**Tip:** If your images are appearing blurry or take too long to load, try adjusting the image-sizing settings. The appropriate percentage depends on the full size of images contained in your CDM repository and may require some experimentation." %} 
</div>
</div>
{% endcapture %}
{% include bootstrap/card.md text=image-card %}

{:.py-4 .mt-4 #bootstrap}
***

## Bootstrap Themes

{% include bootstrap/image.md img="/theme/advanced.jpg" %}

{% capture navbar %}
### Navbar Options:

These options will adjust the basic colors of your site's navigation bar (see [Bootstrap navbar docs](https://getbootstrap.com/docs/4.4/components/navbar/){:target="_blank" rel="noopener"} for details).

- **navbar-color**: Choose from `navbar-light` for use with light background colors, or `navbar-dark` for dark background colors.
	- Options:  `navbar-light`, `navbar-dark`
	- example --> `navbar-color: navbar-dark`

- **navbar-background**: Choose from Bootstrap's background colors.
	- Options: `bg-primary`, `bg-secondary`, `bg-success`, `bg-danger`, `bg-warning`, `bg-info`, `bg-light`, `bg-dark`, `bg-white`, `bg-dark`
	- example --> `navbar-background: bg-dark`

{% endcapture %}
{% include bootstrap/card.md text=navbar %}

{% capture bootswatch %}
### Bootswatch:

[Bootswatch](https://bootswatch.com/){:target="_blank" rel="noopener"} creates unique themes for Bootstrap-based sites. 
Swap out the default Bootstrap for a Bootswatch version using the options below as a fun way to demonstrate the power of CSS to transform look and feel. 

- **bootswatch**: leave blank or comment out for plain bootstrap
	- Options: `cerulean`, `cosmo`, `cyborg`, `darkly`, `flatly`, `journal`, `litera`, `lumen`, `lux`, `materia`, `minty`, `pulse`, `sandstone`, `simplex`, `sketchy`, `slate`, `solar`, `spacelab`, `superhero`, `united`, `yeti`
	- example --> `bootswatch: cerulean`

{% endcapture %}
{% include bootstrap/card.md text=bootswatch %}

{% capture theme %}
### Theme Fonts:

These options change the way the fonts appear throughout your collection. 
If you leave any option blank, it will revert to the CollectionBuilder defaults.

- **base-font-size**: Changes the base size for fonts throughout the site.
	- example --> `base-font-size: 1.2em`
- **text-color**: Changes the color of the base font. Probably want a shade of black ... 
	- example --> `text-color: "#191919"`
- **link-color**: Changes the link color used throughout the site. Base color is a primary blue. 
	- example --> `link-color: "#17a2b8"`
- **base-font-family**: Changes the font family
	- If it's a google family, you'll need to use the font-cdn option below to add the style sheet link to the site.
	- example --> `base-font-family: Georiga; serif;`
- **font-cdn**: This lets you add fonts from Google Fonts or other online resources provided by a content delivery network (cdn). These are typically provided by the service you are using. 
	- example --> `font-cdn: <link href="https://fonts.googleapis.com/css?family=Roboto&display=swap" rel="stylesheet">`

{% endcapture %}
{% include bootstrap/card.md text=theme %}