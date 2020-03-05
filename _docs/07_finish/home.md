---
title: Home Page
stub: home-page
section: finish
section_order: 2
---

{:.py-4 .mt-4 #home-page}
***

## 2. Editing the Home Page

You may finish your collection and realize that you want to remove or shift around the content on your Home page. 
To access the content on this page, you'll need to locate the `home-infographic.html` file in the `_layouts/` directory.

Just like the About page, the Home page is composed of a number of include commands, arranged in three [Bootstrap](https://getbootstrap.com/docs/4.0/layout/grid/) columns:

{:.pl-4 .bg-light .py-2 my-4}
{% raw %}
    <div class="col-md-8">

    {% include index/description.html %}
    {% include index/carousel.html%}

    </div>
    <div class="col-md-4">  

    {% include index/time.html %}

    {% include index/featured-terms.html title="Top Subjects" featured=site.data.theme.featured-subjects field="subject" max=site.data.theme.featured-subjects-max btn-color="info" %}

    {% include index/featured-terms.html title="Locations" featured=site.data.theme.featured-locations field="location" max=site.data.theme.featured-locations-max btn-color="outline-secondary" %}

    {% include index/objects.html %}

    </div>
    <div class="col-md-12">

    {% include index/data-download.html %}

    </div>

{% endraw %}

{:.mt-4}
<div class="row">
<div class="col-md-7" markdown="1">

You can easily delete an include command or move it to another location in the file to change the look of your Home page.  
For instance:

1. You could delete the "timeline" feature from the Home page by removing the `{% raw %}{% include index/time.html %}{% endraw %}` line. Deleting a line is the most common edit we make to this file. 
2. You could move the collection's description from the top left to the top right of the page by copy and pasting `{% raw %}{% include index/description.html %}{% endraw %}` from the first column into the second (and deleting it from the first).
    - You might make this change if you wanted space for your carousel to be taller and more prominent. 
    - You could then adjust the `carousel-height` variable in the [theme](theme.html#home) file. 

</div>

<div class="col-md-5" markdown ="1">
{% include bootstrap/alert.md color="primary ml-4 mb-4 mt-2" text="**Tip:**

These edits move content around, but the home page's column sizing and layout can also be adjusted. Columns follow the Bootstrap Grid, so if you're diving deeper into customizing the layout's size, refer to the [Bootstrap Documentation](https://getbootstrap.com/docs/4.3/layout/grid/)." %}
</div>
</div>

There are a lot of possibilities for customization here! 
We recommend experimenting with your collection to find what works best for you.

{:.mt-4}
### Featured Terms Cards

You might have noticed that the includes for the top subjects and locations cards look a little more complicated than the others on this page.
These simply include a few variables you need to define, just as we did for the include commands on the About page above.

For example, `{% raw %}{% include index/featured-terms.html title="Top Subjects" featured=site.data.theme.featured-subjects field="subject" max=site.data.theme.featured-subjects-max btn-color="info" %}{% endraw %}` contains the following components:

- `index/featured-terms.html`: The name of the file of code you're including. This is a general "featured terms" file that is used to calculate top terms in whichever metadata field you specify (it's used by default with both subjects and locations but you can change these to any fields you want).
- **title**: The custom title you'd like this card to display on the Home page.
    - example --> "`Top Subjects`"
- **field**: The metadata field you'd like to be used for this featured terms card. 
    - example --> "`subject`"
- **btn-color**: The color of the featured-term buttons. You can use any [Bootstrap](https://getbootstrap.com/docs/4.0/utilities/colors/) color or specify your own color following the customization instructions in the [config-theme-color.csv](customize.html#config-colors). 
    - example --> "`info`"

{% include bootstrap/alert.md color="warning" text="Note that there are two more variables in this include that you **DO NOT** need to define here.
These are defined in the home page section of the [theme.yml](theme.html#home) file:
- **featured**: Includes featured terms that you defined in `theme.yml`, instead of generating top terms.
- **max**: Indicates the maximum amount of terms included in the featured terms card, as defined in `theme.yml`." %}
