Once you've adjusted all of your pages, you will likely want to adjust the "About" page to include more than a single paragraph about the collection.  You might also like to move or delete various features on the home page. 

1. [Editing the About Page](#about-page)
2. [Editing the Home Page](#home-page)

{:.py-4 .mt-4 #about-page}
***

## 1. Editing the About Page

To edit the about page, find and open the "about.md" file which is in the root of your repository with the readme, index, and other base files. 
{%include bootstrap/alert.md color="info float-right col-md-3 ml-4 py-2" text="**Markdown Resources**
- [Tutorial](https://www.markdowntutorial.com/) 
- [Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)" %} 

This is a Markdown File, extension ".md". Markdown is a friendly way to write HTML that is being used more and more.  (FYI: This entire website has been written in markdown.) Jekyll is built to use and process Markdown, so it's a good skill to learn as you get further into this type of development. 

There are a number of tutorials on the web to learn more about Markdown (see Markdown Resources box), but to simply write a few paragraphs, you need to just write a few paragraphs into the file.

Below is an example about page written in Markdown, using the include item-figure.html command discussed below, in case you'd like to copy and paste from a reference. 

{:.pl-4 .bg-light .py-2 my-4 mb-4}
{% raw %}
    ## About the {{site.collection}} 

    The Devin Becker Collection of large unruly dogs consists of one dog named Rufus. 
    
    Rufus is a good boy most of the time. 

    {% include item-figure.html objectid="rufus001" float="left" size="6"%}

    ### When Is Rufus a Bad Boy

    Here's list of examples of when Rufus is bad: 
    
    - when he doesn't listen to Devin
    - when he runs off into the field or down into the other neighborhood chasing cats. 

    ### Rufus is the Best

    Devin's Collection or Large Unruly Dogs is truly one of a kind. 
    
    It is much appreciated most of the time by Devin.

{% endraw %}

{:.mt-4}
#### Adding an image to the About Page

In order to add an image with a caption into any about page, you just need to select the image you'd like to feature, then include it on the about page by pasting in the following code: 

{:.pl-4}
{% raw %}
    {% include item-figure.html objectid="demo-psychiana548" %}
{% endraw %}

Or if you wanted the image a smaller size and floating on the left:  

{% raw %}
    {% include item-figure.html objectid="demo-psychiana548" float="left" size="2" %}
{% endraw %}

The features that you can modify in this "include" command are: 

- **objectid**: 
    - This refers to the image and will be used to grab the information for that image from the metadata sheet. 
    - example --> `objectid="demo-psychiana548"`

{% include bootstrap/alert.md color="primary col-md-4 float-right ml-4 mb-4 mt-2" text="**Include Files:** 

Jekyll's include command is a really powerful feature that allows specific elements or content to be drawn into many pages (or just one) from one central location. For more on includes and other Jeykll features, check out the [Jekyll Website](https://jekyllrb.com/)" %}

- **float**: 
    - This determins which direction the image floats, left or right. Default is right.
    - Default: right
    - Options: `left` or leave blank for a 'float-right'  
    - example --> `float="left"`
- **size**:
    - This corresponds to a column measurement for the image. This is based on Bootstrap's grid, so it can be any number from 1 to 12. 
    - We'd recommend somewhere between 2 and 4. On a smaller screen, the image will fill the screen's width, but on larger screens it will float with some space around it to either the right or left.
    - Default: 3
    - Options: [1 - 12]
    - example --> `size="2"`

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





