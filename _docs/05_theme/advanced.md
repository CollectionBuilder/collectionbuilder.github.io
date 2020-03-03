---
title: Advanced Options
stub: advanced
section: theme
section_order: 10
---

{:.py-4 .mt-4 #advanced}
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
{% include bootstrap/alert.md color="info" text="**Tip:** If your images are appearing blurry or take too long to load, try adjusting the image-sizing settings." %} 
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

These options will adjust your site's color and look.

- **navbar-color**: Choose from `navbar-light` for use with light background colors, or `navbar-dark` for dark background colors navbar-dark
	- Options:  `navbar-light`, `navbar-dark`
	- example --> `navbar-color: navbar-dark`

- **navbar-background**: Choose from the background colors for Bootstrap. 
	- Options: `bg-primary`, `bg-secondary`, `bg-success`, `bg-danger`, `bg-warning`, `bg-info`, `bg-light`, `bg-dark`, `bg-white`, `bg-dark`]
	- example --> `navbar-background: bg-dark`
{% endcapture %}
{% include bootstrap/card.md text=navbar %}

{% capture bootswatch %}
### Bootswatch:

Bootswatch creates themes for Bootstrap 4 sites. You can check them out here: <https://bootswatch.com/>. Swap themes using the options below.

- **bootswatch**: leave blank or comment out for plain bootstrap
	- Options: `cerulean`, `cosmo`, `cyborg`, `darkly`, `flatly`, `journal`, `litera`, `lumen`, `lux`, `materia`, `minty`, `pulse`, `sandstone`, `simplex`, `sketchy`, `slate`, `solar`, `spacelab`, `superhero`, `united`, `yeti`
	- example --> `bootswatch: cerulean`
{% endcapture %}
{% include bootstrap/card.md text=bootswatch %}

{% capture theme %}
### Theme Fonts:

These options change the way the fonts appear throughout your collection. If you leave any option blank, it will revert to the base Bootstrap 4 CSS style(s).

- **base-font-size**: Changes the base size for fonts throughout the site.
	- example --> `base-font-size: 1.2em`

- **text-color**: Changes the color of the base font. Probably want a shade of gray or black ... 
	- example --> `text-color: "#191919"`

- **link-color**: Changes the link color used throughout the site. Base color is a primary blue. 
	- example --> `link-color: "#17a2b8"`

- **base-font-family**: Changes the font family; if it's a google family, you'll need to adjust the _includes/header.html file as well to include the link to Google's CSS style file for that font.
	- Comment out (using `#`) for bootstrap defaults  
	- example --> `base-font-family: Georiga; serif;`
{% endcapture %}
{% include bootstrap/card.md text=theme %}