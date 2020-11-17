---
layout: about
title: Advanced Workshop - Timeline Edits Step Thru
permalink: /advanced-steps.html
---

# Advanced Topics Step Thru

These steps will take you through 
- [Editing the home page](#edit-home-infographic-layout)
- [Editing the repository on your local computer](#edit-the-repository-on-your-desktop) 
- [Adding a TimelineJS Feature](#add-timelinejs-feature)
- [Editing the Timeline visualization to accommodate other data](#change-timeline-visualization-to-feature-other-data)

{:.mt-5}
## Edit home-infographic layout

The **home-infographic.html** file in the _layouts folder controls what features appear in your front page. Once you open that file, you'll see a number of ["include" commands](https://jekyllrb.com/docs/includes/) that port in different features into the home page. 

- Maybe locations aren't that important to this collection, but you think material type, aka item_information, is. Let's change the locations card on the front page to feature item_information and change the title of that card to reflect the change. 

- And we need to make room for a larger carousel, so let's move the description into the narrow row. 

- And let's delete the subjects card for now, just to focus on the material type. 

Here's how that should look:

{%raw%}
```
---
layout: page
---
{%- assign items = site.data[site.metadata] -%}
<div class="row">
  <div class="col-md-8">

    {% include index/carousel.html %}
  
  </div>
  <div class="col-md-4">  
    {% include index/description.html %}

    {% include index/time.html %}

    {% include index/featured-terms.html field="item_information" title="Material Type" btn-color="outline-secondary"  max=6 %}

    {% include index/objects.html %}

  </div>
  <div class="col-md-12">

    {% include index/data-download.html %}

  </div>
</div>
```
{% endraw %}

The home-infographic layout, and all pages in CollectionBuilder are styled using bootstrap, particularly using its grid feature. More on bootstrap grid --> https://getbootstrap.com/docs/4.5/layout/grid/

{:.mt-5}
## Edit the Repository on Your Desktop

This step requires your [downloading some software](https://collectionbuilder.github.io/docs/software.html) and working on your computer. However, all the steps below can also be accomplished via the web interface. I'm just using my own computer to show the changes more quickly. 

At base, if you can download Git, GitHub Desktop, and Visual Studio Code (all are easy to install), you can at least edit your files and push them to your repository. If you want to see your changes on a test server before pushing them, you'll need to install Ruby and Jekyll. 

**Note on Using Ruby/Jekyll via the Commandline**

To start a Jekyll server, the typical command is `jekyll s`. If you start working in this way, you will get used to that command. However, you'll also run into issues where the "gems" loaded when you load Jekyll might be out of step with the gems you have installed on your computer. This will cause error messages in the timeline. There are a couple of ways to remedy this issue: 

1. Type `bundle exec jekyll s` -- bunlder handles all your gems, and by typing the jekyll command this way, bundler will make sure to operate within the paremeters defined by the repository you're working in. 
2. Type `bundle update` -- this will update the gems on your computer to match the gems in the repository. If you haven't updated your gems in a while, this is a good thing to type. It will most likely fix your problem, after which you can simply type `jekyll s` again and move forward. 

{:.mt-5}
## Add TimelineJS Feature

To add the timeline feature to the front page, you'll need to edit "home-infographic.html" in the _layouts directory by adding the below: 

{%raw%}
```
  <div class="col-md-12">
    
    {% include feature/timelinejs.html %}

  </div>
```
{%endraw%}


This creates a full width div that will include the code to display a timelinejs feature.

More detail on this is on our documentation page: [https://collectionbuilder.github.io/docs/advanced.html#timelinejs](https://collectionbuilder.github.io/docs/advanced.html#timelinejs)

{:.mt-5}
## Curate TimelineJS Items

You probably don't want the whole collection included, so you'll want to edit that. To do that, you need to edit the **timelinejs.json** file in the **/assets/data/** folder. 

Look at the JSON object and see how various pieces are being constructed. You can adjust the title media and text portions to style the first slide of your timeline. 

At the top, you can adjust what's included by defining which items are included in the array that is generating the json object below. To do that, you'll use "where" expressions, which are part of the liquid filtering mechanism in jekyll. 

{:.mt-5}
### Filter timeline objects using where and where_exp

There are two types of where expresions. [The Basic "where:"](https://shopify.github.io/liquid/filters/where/) and [the more powerful where_exp](https://jekyllrb.com/docs/liquid/filters/#where-expression)

(These are liquid expressions. You can see a cheatsheet of those here: https://learn.cloudcannon.com/jekyll-cheat-sheet/)

So let's do a few ... 

**Just Images**

{% raw %}
`{%- assign items = site.data[site.metadata] | where: "format","image/jpg" -%}`{% endraw %}

- The above will only include items that are of the format "image/jpg" 

---

**Just Items With Non-Approximate Dates**

{:.mt-4}{% raw %}
`{%- assign items = site.data[site.metadata] | where_exp: "item","item.date-is-approximate? == nil" -%}`{% endraw%}

(is the same as)

{% raw %}
`{%- assign items = site.data[site.metadata] | where_exp: "item","item.date-is-approximate? != "yes" -%}`{% endraw%}

- Both the above do the same thing --> They only include items whose `date-is-approximate?` field is empty (or doesn't say "yes")

---

**Just Items with 'God' in the Subjects**

{% raw %}
`{%- assign items = site.data[site.metadata] | where_exp: "item","item.subject contains 'God'" -%}`{% endraw%}

- This will only include items that have "God" in the subject field (as part of any subject)

See the advanced topic documentation for other ways to include timelines, including in place of timeline page and as an additional page. 

{:.mt-5}
### [Liquid Operators](https://shopify.github.io/liquid/basics/operators/)

| Operator | Result |
| --- | --- |
| == | equals
| != | does not equal
| > | greater than
| < | less than
| >= | greater than or equal to
| <= | less than or equal to
| or | logical or
| and | logical and


{:.mt-5}
## Change timeline visualization to feature other data

First step is to change from the Psychiana collection to the Watkins Collection

1. If you're working on your own computer, shut down the server by clicking CTRL + C in the terminal.
2. Download [Watkins metadata](https://docs.google.com/spreadsheets/u/1/d/1mThECwBYaUdvUrSbc9d2wbjedpYyvVD89jJ15R-7Qmo/edit?usp=sharing). 
3. Change _config.yml metadata variable to watkins. 
4. Restart server by typing `jekyll s` or `bundle exec jekyll s`

All items in this collection are from 1890, and we don't have months, so .... 

*The timeline isn't very helpful.*

Let's get rid of it, and fix up our timeline page so that it's different. 

- Remove Timeline feature from home-infographic.html by removing the include command that includes the "feature/time.html" file. 

- Now open the **timeline.html** file layout and change the map option at the top from "date" to "depth" -- this is how it should look

{% raw %}
`{%- assign raw-dates = site.data[site.metadata] | map: 'depth' | compact | uniq -%}`{% endraw%}

- Now you'll need to make sure that connects to the visualization below. Find where the items are defined for each rown in the HTML below. You can search for the only "where_exp" on the page. 

- Change that so that `item.date contains year` becomes `item.depth contains year`

{% raw %}
`{%- assign inYear = items | where_exp: 'item', 'item.depth contains year' -%}`{% endraw%}

*Note: We are keeping the `year` variable constant here so as not to have to edit all the code and risk messing it up somewhere. You can, however, go through and edit all the `year` variables on the page to become `depth` if you like to keep things readable.*

{:.mt-5}
### Change the page title and navigation to rename the timeline feature

So now that we are looking at depth rather than years, we'll likely want to change the way that displays on the page. 

- Change **_data/config-nav.csv** so that instead of the line `Timeline,/timeline.html` it should read `Depth,/depth.html`

- Then change **/pages/timeline.md** so that the page is titled differently and that the page creats a different url, using the powerful [permalink option](https://jekyllrb.com/docs/permalinks/). You can still keep the file named timeline.md, or you can change it. 

You'll want the page to look like this: 

{% raw %}
```
---
title: Depth
layout: timeline
permalink: /depth.html
# a timeline visualization will be added below the content in this file
---

{:.mt-5}
## Collection Depth
```
{% endraw%}

{:.mt-5}
### A Really Annoying issue with sorting 3- and 4-digit numbers

Obviously we have some issues here. 1000ft is not getting sorted correctly. This is an issue with a lot of programming languages, and also an issue with dates, if they're long enough. 

So, a couple ways to adjust this. 

1. Change the metadata so that all are four digit numbers. So "100" would become "0100" -- this is obviously not idea. 
2. Adjust the numbers in the processing at the top to make sure they are all four digitis. 

*NOTE: This is getting really deep, so if you don't want to edit this, that's fine*

{% raw %}
`{%- capture clean-years -%}{% for date in raw-dates %}{% if date contains "000" %}{{ date | strip | split: "-" | first }}{% else %}{{ date | strip | prepend: "0"}}{% endif %}{% unless forloop.last %};{% endunless %}{%- endfor -%}{%- endcapture -%}`{% endraw%}

Once you do this, you'll see that nothing shows up. However, if you switch the where_exp to where the year contains the item.depth, it should work. 

{% raw %}
`{%- assign inYear = items | where_exp: 'item', 'year contains item.depth' -%}`{% endraw%}

Then, you'll likely want to adjust the display below so that the four digit numbers that start with a zero are only displayed as the three digit number they originated as. 

{% raw %}
{% if year contains '000'%}{{year}}ft{% else %}{{ year | slice: 1,3 }}ft{% endif %}

You'll also need to adjust the dropdown so that it does the same thing for display. 

Finally, say you wanted to do something really cool and make it look like as you were going down the page, you were also going down in depth ... 

This is where you can [use the cycle command](https://shopify.github.io/liquid/tags/iteration/#cycle) like such
{% raw %}
`<tr id="{{ year }}" style='background-color: {% cycle "#FFFFFF","#E7E6DD","#B9B8B1","#94938E","#767672","#5E5E5B","#4B4B49","#3C3C3A","#30302E","#262625","#1E1E1E","Black"%}''>`{% endraw%}

{:.mt-5}
## Change Timeline Visualization to Include Words Rather than Numbers

What if you don't want to do depth, or you have something else ... 

Change `depth` to `mine`

Nothing's showing up, and you can see why -- the former processing code got rid of the space between the words. Let's find that part and remove it. 

This

{% raw %}
`{%- assign uniqueYears = clean-years | remove: " " | split: ";" | uniq | sort -%}`{% endraw%}

becomes

{% raw %}
`{%- assign uniqueYears = clean-years  | split: ";" | uniq | sort -%}`{% endraw%}

And it should work!






