{:.py-4 .mt-4 #about}
***

## About Page

{% capture about %}
- **about-featured-image**: The objectid for the image you would like to feature on your home page.
	- If this field is left blank, CollectionBuilder will use the image featured on the site's home page
    - *Tip*: It's best to choose an image that is large and more "landscape" than "portrait," i.e. more horizontal than vertical. 
	- example --> `about-featured-image: demo-psychiana15` 
{% endcapture %}

{% include bootstrap/card.md text=about %}