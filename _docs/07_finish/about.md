---
title: About Page
stub: about-page
section: finish
section_order: 1
---

{:.py-4 .mt-4 #about-page}
***

## 1. Editing the About Page

{:.clearfix}
To edit the About page, find and open the "about.md" file which is in the Pages directory of your repository. 
{%include bootstrap/alert.md color="info float-right ml-4 py-2" text="**Markdown Resources**
- [Tutorial](https://www.markdowntutorial.com/) 
- [Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)" %} 

This is a Markdown File, extension `.md`. Markdown is a friendly way to write HTML that is being used more and more. 
Jekyll is built to use and process Markdown, so it's a good skill to learn as you get further into this type of development. 

There are a number of tutorials on the web to learn more about Markdown (see Markdown Resources box above), but to write a couple paragraphs of content, you simply need to write a few lines of text into the file.

Below is an example About page written in Markdown, in case you'd like to copy and paste from a reference. 

{:.pl-4 .bg-light .py-2 .my-4 .border}
{% raw %}
    ## About the {{ site.collection }} 

    The Devin Becker Collection of large unruly dogs consists of one dog named Rufus. 
    
    Rufus is a good boy most of the time. 

    {% include feature/item-figure.html objectid="rufus001" float="left" size="6" %}

    ### When Is Rufus a Bad Boy

    Here's list of examples of when Rufus is bad: 
    
    - when he doesn't listen to Devin
    - when he runs off into the field or down into the other neighborhood chasing cats. 

    ### Rufus is the Best

    Devin's Collection of Large Unruly Dogs is truly one of a kind. 
    
    It is much appreciated most of the time by Devin.

{% endraw %}

Note that this example uses an include command to include a featured image on the About page. Information on how to do this is discussed below.

{:.mt-4}
#### Adding an image to the About Page

In order to add an image with a caption into any about page, you just need to select the image you'd like to feature, then include it on the about page by pasting in the following code: 

{:.bg-light .p-4 .my-4 .border}
{% raw %}
    {% include item-figure.html objectid="rufus001"  %}
{% endraw %}

Or if you wanted the image to be a smaller size and float on the left:  

{:.bg-light .p-4 .my-4 .border}
{% raw %}
    {% include item-figure.html objectid="demo-psychiana548" float="left" size="2" %}
{% endraw %}

The features that you can modify in this "include" command are: 

- **objectid**: 
    - This refers to the image and will be used to grab the information for that image from the metadata spreadsheet. 
    - example --> `objectid="demo-psychiana548"`

{% include bootstrap/alert.md color="primary col-md-4 float-right ml-4 mb-4 mt-2" text="**Include Files:** 

Jekyll's include command is a really powerful feature that allows specific elements or content to be drawn into many pages (or just one) from one central location. For more on includes and other Jeykll features, check out the [Jekyll Website](https://jekyllrb.com/)" %}

- **float**: 
    - This determines which direction the image floats, left or right. Default is right.
    - Default: right
    - Options: `left` or leave blank for a 'float-right'  
    - example --> `float="left"`
- **size**:
    - This corresponds to a column measurement for the image. This is based on Bootstrap's grid, so it can be any number from 1 to 12. 
    - We'd recommend somewhere between 2 and 4. On a smaller screen, the image will fill the screen's width, but on larger screens it will float with some space around it to either the right or left.
    - Default: 3
    - Options: [1 - 12]
    - example --> `size="2"`