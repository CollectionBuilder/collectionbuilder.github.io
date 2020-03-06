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

Just like the About page, the Home page is composed of a number of include commands, arranged in three [Bootstrap columns](https://getbootstrap.com/docs/4.0/layout/grid/){:target="_blank" rel="noopener"}:


{% raw %}
    <div class="col-md-8">

    {% include index/description.html %}
    {% include index/carousel.html%}

    </div>
    <div class="col-md-4">  

    {% include index/time.html %}

    {% include index/featured-terms.html field="subject" title="Top Subjects" btn-color="info" featured=site.data.theme.featured-subjects max=site.data.theme.featured-subjects-max %}

    {% include index/featured-terms.html field="location" title="Locations" btn-color="outline-secondary" featured=site.data.theme.featured-locations max=site.data.theme.featured-locations-max %}

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

1. You could delete the "Time Span" feature box from the Home page by removing the `{% raw %}{% include index/time.html %}{% endraw %}` line. Deleting a line is the most common edit we make to this file. 
2. You could move the collection's description from the top left to the top right of the page by copy and pasting `{% raw %}{% include index/description.html %}{% endraw %}` from the first column into the second (and deleting it from the first).
    - You might make this change if you wanted space for your carousel to be taller and more prominent. 
    - You could then adjust the `carousel-height` variable in the [theme](theme.html#home) file. 

</div>

<div class="col-md-5" markdown ="1">
{% include bootstrap/alert.md color="primary ml-4 mb-4 mt-2" text="**Tip:**

These edits move content around, but the home page's column sizing and layout can also be adjusted. Columns follow the Bootstrap Grid, so if you're diving deeper into customizing the layout, refer to the [Bootstrap Documentation](https://getbootstrap.com/docs/4.3/layout/grid/)." %}
</div>
</div>

There are a lot of possibilities for customization here! 
CollectionBuilder is designed as a flexible template that can be adapted to the needs of a collection.
We recommend experimenting to find what works best for you.

{:.mt-4}
### Featured Terms Cards

You might have noticed that the includes for the top subjects and locations cards in the home-infographic layout look a little more complicated than the others on this page.
By default they are set up to work with options set in Home page section of the [theme.yml](theme.html#home) file, and use the metadata fields "subject" and "location".
However, you can customize them by editing the option variables, just as we did for the include commands on the About page above.

For example, `{% raw %}{% include index/featured-terms.html field="subject" title="Top Subjects" btn-color="info" featured=site.data.theme.featured-subjects max=site.data.theme.featured-subjects-max %}{% endraw %}` contains the following components:

- `index/featured-terms.html`: is the name of the file you're including. This is the general "featured terms" code that is used to calculate top terms in whichever metadata field you specify and create a card for display. The options are set using the parameter variables listed below.
- **field**: The metadata field to be used to auto-generate top terms for the card (to *not* auto-generate, use the `featured` option instead).
    - example --> `"subject"`
- **title**: The title you'd like this card to display on the Home page.
    - example --> `"Top Subjects"`
- **btn-color**: The color of the featured-term button links. You can use any [Bootstrap color](https://getbootstrap.com/docs/4.0/utilities/colors/){:target="_blank" rel="noopener"}, or specify your own color following the customization instructions in the [config-theme-color.csv](customize.html#config-colors). 
    - example --> `"info"`, `"info-outline"`
- **featured**: As an alternative to the "field" option above, provide a manually defined list of terms to feature separated by semicolon. By default this can be set using the optional `featured-subjects` value in theme.yml. If this option is used, the `field` option is ignored. 
    - example --> `"dogs;muffins;cats"`
- **max**: Indicates the maximum amount of terms to be included in the card. By default this can be set using the `featured-subjects-max` value in theme.yml.
    - example --> `3`
