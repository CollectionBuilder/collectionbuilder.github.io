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
To edit the About page, find and open the `about.md` file which is in the Pages directory of your repository. 
{%include bootstrap/alert.md color="info float-right ml-4 py-2" text="**Markdown Resources**
- [Tutorial](https://www.markdowntutorial.com/) 
- [Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)" %} 

This is a Markdown File. Markdown is a friendly way to write HTML that is being used more and more. 
Jekyll is built to use and process Markdown, so it's a good skill to learn as you get further into this type of development. 

There are a number of tutorials on the web to learn more about Markdown (see Markdown Resources box above), and we suggest you check them out.

<div class="row">
<div class="col-md-7" markdown="1">
When you open the `about.md` file, you'll see that there is already one include command at the beginning of the file which is pulling in the page's jumbotron image: `{% raw %}{% include about/jumbotron.html %}{% endraw %}` (remember, you chose this image in the [theme.yml](theme.html#about) file). If you don't want the jumbotron on your About page, just delete this line of code.

Alternately, if you'd like to add *more* visual features to the page we've made it easy to do this too, by including templated files.
You'll find the files below in the `_includes/feature/` directory:
- `alert.md`
- `card.md`
- `item-figure.html`
- `modal.md`
</div>

<div class="col-md-5" markdown ="1">
{% include bootstrap/alert.md color="info ml-4 mb-4 mt-2" text="**Include Files:** 

Jekyll's include command is a really powerful feature that allows specific elements or content to be drawn into many pages (or just one) from one central location. For more on includes and other Jekyll features, check out the [Jekyll Website](https://jekyllrb.com/)" %}
</div>
</div>

{:.mt-4}
### Adding an image to the About Page

The `item-figure.html` include adds a [Bootstrap](https://getbootstrap.com/docs/4.4/content/figures/)-styled figure to the page.

It requires that you give a value for one variable, **objectid**, and gives you the option to add three others. These are defined below.

*Required*:
- **objectid**: The objectid of an image in your collection
    - This will be used to grab the information for that image from the metadata spreadsheet. 
    - example --> `objectid="demo_psychiana548"`

*Optional*:
- **width**: Uses Bootstrap sizing to set the image's percentage size.
    - *Options*: "`25`", "`50`", "`75`", or "`100`"
- **float**: Uses Bootstrap float utility to float the image left or right. 
    - *Options*: "`left`" or "`right`"
- **caption**: Automatically includes the title of the item (as described in your metadata).
    - This is on by default, so you don't need to add this variable to your include command if you want the caption to display.
    - If you'd like to turn the caption off, simply insert the value "`false`"

All values should be wrapped in quotation marks. See the examples below:

With only required variables:
- `{% raw %}{% include feature/item-figure.html objectid="demo_001" %}{% endraw %}`

With additional optional variables:
- `{% raw %}{% include feature/item-figure.html objectid="demo_001" width="50" float="left" caption="false" %}{% endraw %}`

The `alert.md`, `card.md`, and `modal.md` files can be included in a similar manner, but require different variables. Find these files in your repository in the `_includes/feature/` directory and open them to view a description of the variables they support. 