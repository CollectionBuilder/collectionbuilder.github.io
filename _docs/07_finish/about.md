---
title: About Page
stub: about-page
section: finish
section_order: 1
---

{:.py-4 .mt-4 #about-page}
***

## 1. Editing the About Page

To edit the About page, find and open the `about.md` file which is in the Pages directory of your repository. 

{%include bootstrap/alert.md color="info float-right ml-4 py-2" text="**Markdown Resources**
- [Tutorial](https://commonmark.org/help/tutorial/)
- [On GitHub](https://help.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax)
- [Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)" %} 

[Markdown](https://daringfireball.net/projects/markdown/syntax){:target="_blank" rel="noopener"} is a quick and easy standard to write documents that can be converted into HTML for the web. 
Because of it's simplicity, Markdown is used by many websites for creating content or allowing users to format comments.
In fact all of the CollectionBuilder docs are written in Markdown. 

Jekyll has Markdown support built in, so it's a good skill to learn as you get further into this type of development. 
There are a number of tutorials on the web to learn more (see Markdown Resources box above), and we suggest you check them out.

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

Jekyll's include command is a really powerful feature that allows specific elements or content to be drawn into pages from one central location. For more on includes and other Jekyll features, check out the [Jekyll docs](https://jekyllrb.com/docs/)" %}
</div>
</div>

{:.mt-4}
### Adding an image to the About Page

The `item-figure.html` include adds a [Bootstrap-styled figure](https://getbootstrap.com/docs/4.4/content/figures/){:target="_blank" rel="noopener"} to the page.

It requires that you give a value for one variable, **objectid**, and gives you the option to add three other options. 
These are defined below.

*Required*:

- **objectid**: The objectid of an image in your collection that will be used to grab the information for that item from the collection metadata. 
    - example --> `objectid="demo_psychiana548"`

*Optional*:
- **width**: Uses Bootstrap sizing to set the image's percentage size.
    - *Options*: `25`, `50`, `75`, or `100`
- **float**: Uses Bootstrap float utility to float the image left or right. 
    - *Options*: `left` or `right`
- **caption**: By default the figure include automatically adds the title of the item from your metadata. This option is used *only* if you would like to override the default title. To replace the title, you can either add the text for an alternative caption *or* give the value `false` to not include any caption.
    - To manually set the caption, provide the text, e.g. `caption="Example caption"`
    - If you'd like to turn the caption off use `caption=false`

For example, adding a figure with only required variables:
- `{% raw %}{% include feature/item-figure.html objectid="demo_001" %}{% endraw %}`

With additional optional variables:
- `{% raw %}{% include feature/item-figure.html objectid="demo_001" width="50" float="left" caption=false %}{% endraw %}`

If you use the `float` option, you may want to "clear" the float at some point below. 
This can be done by adding `<div class="clearfix"></div>` on it's own line.

The `alert.md`, `card.md`, and `modal.md` files can be included in a similar manner, but require different variables. Find these files in your repository in the `_includes/feature/` directory and open them to view a description of the options. 
