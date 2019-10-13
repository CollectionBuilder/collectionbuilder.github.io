Once you've adjusted all of your pages, you will likely want to adjust the about page to include more than a single paragraph about the collection.  You might also like to move or delete various features on the home page.  

## Writing an About Page

By default, the about page will be populated by the description you add to the _config.yml file. To edit the content, go to the "about.md" file which is in the root of your repository. 

This is a markdown file. Markdown is a friendly way to write HTML. There are a number of tutorials on the web to learn more about Markdown, but to simply write a few paragraphs, you need to just write a few paragraphs into the file. If you'd like to add another section with a header, you can write the header and start it with three hash tags and a space `### `. 

An example would be `### About the Creation of the Collection` or `### On Being`. These would be rendered in HTML as <h3> elements. 

A markdown tutorial and cheat sheet: 

- <https://www.markdowntutorial.com/> - step by step, with a try it out feature
- <https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet> - a good cheat sheet. 

### Adding an image to the About Page

We've added a way to add an image with a caption into any about page. You just need to select the image you'd like to feature, then include it on the about page by pasting in the following code: 

{:.pl-4}
{% raw %}
    {% include item-figure.html objectid="demo-psychiana548" %}
{% endraw %}

The features that you can modify in this includes are: 

- **objectid** - This refers to the image and will be used to grab the information for that image from the metadata sheet. 
    - example --> `objectid="demo-psychiana548"`
- **float** - This determins which direction the image floats, left or right. Default is right.
    - Default: right
    - Options: `left` or leave blank for a 'float-right'  
    - example --> `float="left"`
- **size** - This corresponds to a column measurement for the image. This is based on Bootstrap's grid, so it can be any number from 1 to 12. We'd recommend somwhere between 2 and 4. On a smaller screen, the image will fill the screen's width, but on larger screens it will float with some space around it to either the right or left.
    - Default: 3
    - Options: [1 - 12]
    - example --> `size="2"`

## Determining the Content and Layout of the Home Page

You may finish your collection and realize, for instance, you might not want the Locations card on the home page of your collection. In order to adjust that page, you need to edit a page in the _layouts folder called "home-infographic.html."

The file looks like this: 

{:.pl-4}
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

In order to edit what appears, you will need to either delete a line or rearrange the include commands like so: 

{:.pl-4}
{% raw %}
    <div class="col-md-8">


    {% include index/carousel.html%}

    </div>
    <div class="col-md-4">  

    {% include index/description.html %}
    {% include index/time.html %}
    {% include index/subjects.html %}
    {% include index/objects.html %}

    </div>
    <div class="col-md-12">

    {% include index/data-download.html %}

    </div>

{% endraw %}

This example removes the "location" card from the original home page and moves the description to the top right of the page. You might make this change if you wanted your carousel to be taller and more prominent. You often might need to delete one line of this file. We find we often delete {% raw %}`{% include index/locations.html %}`{% endraw %}.

You can also adjust the sizing of the columns. These follow the Bootstrap Grid, so if you're diving deeper into customizing the layout's size, refer to the [Boostrap documentation](https://getbootstrap.com/docs/4.3/layout/grid/).



