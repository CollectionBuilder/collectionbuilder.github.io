---
title: Home Page
stub: home-page
section: polish
section_order: 2
---

{:.py-4 .mt-4 #home-page}
***

## 2. Editing the Home Page

You may finish your collection and realize, for instance, you might not want the Locations card on the home page of your collection. In order to adjust that page, you need to edit a page in the _layouts folder called "home-infographic.html."

The "home-infographic.html" file looks like this: 

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
In order to edit what appears, you will need to either delete a line or rearrange the include commands like so: 

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
{% include bootstrap/alert.md color="primary col-md-5 float-right ml-4 mb-4 mt-2" text="**Tip:**

These edits move content around, but the home page's column sizing and layout can also be adjusted. Columns follow the Bootstrap Grid, so if you're diving deeper into customizing the layout's size, refer to the [Boostrap documentation](https://getbootstrap.com/docs/4.3/layout/grid/)." %}

{:.mt-4}
This example accomplishes several edits:  

1. It deletes the "location" feature from the original home page
2. It moves the description from the top left to the top right of the page.
    - You might make this change if you wanted your carousel to be taller and more prominent. 
    - You could then adjust the `carousel-height` variable in the [theme](theme.html#home-page) file. 
3. It moves the timeline feature to the bottom of the right column.

You often might need to delete one line of this file. We find we often delete {% raw %}`{% include index/locations.html %}`{% endraw %}.