---
title: Home Page
stub: home-page
section: finish
section_order: 2
---

{:.py-4 .mt-4 #home-page}
***

## 2. Editing the Home Page

You may finish your collection and realize, for instance, you do not want the Locations card on the home page of your collection. In order to adjust the home page, you need to edit a page in the _layouts folder called "home-infographic.html."

**For CDM and SA users**, the "home-infographic.html" file looks like this: 

{:.pl-4 .bg-light .py-2 my-4}
{% raw %}
    <div class="col-md-8">

    {% include index/description.html %}
    {% include index/carousel.html%}

    </div>
    <div class="col-md-4">  

    {% include index/time.html %}
    {% include index/subjects.html %}
    {% include index/locations.html %}
    {% include index/objects.html %}

    </div>
    <div class="col-md-12">

    {% include index/data-download.html %}

    </div>

{% endraw %}

{:.mt-4}
**For GH users**, the "home-infographic.html" file is almost exactly the same but has a different include command for subjects and locations: 

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
**No matter which version of CollectionBuilder you're using, you can edit this file in the same way**. In order to edit what appears, you will need to either delete a line or rearrange the include commands like so: 

{:.pl-4 .bg-light .py-2 my-4}
{% raw %}
    <div class="col-md-8">


    {% include index/carousel.html%}

    </div>
    <div class="col-md-4">  

    {% include index/description.html %}
    {% include index/subjects.html %}
    {% include index/objects.html %}
    {% include index/time.html %}

    </div>
    <div class="col-md-12">

    {% include index/data-download.html %}

    </div>

{% endraw %}

{:.mt-4}
<div class="row">
<div class="col-md-7" markdown="1">

This example accomplishes several edits:  

1. It deletes the "location" feature from the original home page
2. It moves the description from the top left to the top right of the page.
    - You might make this change if you wanted your carousel to be taller and more prominent. 
    - You could then adjust the `carousel-height` variable in the [theme](theme.html#home) file. 
3. It moves the timeline feature to the bottom of the right column.

You might find that you need to delete one line of this file. We find we often delete {% raw %}`{% include index/locations.html %}`{% endraw %} for collections without location metadata.
</div>

<div class="col-md-5" markdown ="1">
{% include bootstrap/alert.md color="primary ml-4 mb-4 mt-2" text="**Tip:**

These edits move content around, but the home page's column sizing and layout can also be adjusted. Columns follow the Bootstrap Grid, so if you're diving deeper into customizing the layout's size, refer to the [Bootstrap Documentation](https://getbootstrap.com/docs/4.3/layout/grid/)." %}
</div>
</div>
