---
title: TimelineJS
stub: timelinejs
section: advanced
section_order: 1
---
{:.py-4 .mt-4 #timelinejs}
***

### Building a TimelineJS Feature

[TimelineJS](http://timeline.knightlab.com/) is an open source timeline builder that creates an interactive timeline based on underlying data. We've incorporated the TimelineJS code into CollectionBuilder in order to offer this feature. 

{:.alert .alert-warning}
Currently, the timelinejs feature will create a timeline based on your entire collection metadata file by default. **This will likely be too large for it to work well.** Below we detail ways to further customize and curate your timeline. 

#### Step 1: Including TimelineJS on a page

There are three basic options for including a TimelineJS feature. The instructions below detail those options. 


<div id="accordion" class="mb-4">
<div class="card">
<div class="card-header" id="headingOne">
<h5 class="mb-0">
<button class="btn btn-link text-dark" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
Inserting TimelineJS into the Home Page
</button>
</h5>
</div>
<div id="collapseOne" class="collapse" aria-labelledby="headingOne" data-parent="#accordion">
<div class="card-body" markdown="1">
1. Open the `home-infographic.html` file in the _layouts directory. 
2. You may want to edit the column sizes or arrangement of the file. The TimelineJS feature will work decently in a smaller section, but it looks best in a wider format. 
3. Add `{% raw %}{% include feature/timelinejs.html %}{%endraw%}` to the section in which you'd like the feature to appear. 
4. Save the file. 
</div>
</div>
</div>
<div class="card">
<div class="card-header" id="headingTwo">
<h5 class="mb-0">
<button class="btn btn-link collapsed text-dark" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
Replacing the Current Timeline Page
</button>
</h5>
</div>
<div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordion">
<div class="card-body" markdown="1">
1. Open the "timeline.md" page in the /pages/ directory and edit the layout variable so that it reads "full-width-page"
2. Replace the `## Collection Timeline` line with the following "include" command: `{% raw %}{% include feature/timelinejs.html %}{%endraw%}`
</div>
</div>
<div class="card">
<div class="card-header" id="headingTwo">
<h5 class="mb-0">
<button class="btn btn-link collapsed text-dark" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
Creating a New Timeline Page (+ a "Timelines" dropdown)
</button>
</h5>
</div>
<div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordion">
<div class="card-body" markdown="1">
1. Open the current "timeline.md" page, which can be found in the /pages/ directory and copy its contents. 
2. Create a new markdown file in the /pages/ directory called "timelinejs.md".
3. Paste the copied text into that page
4. Edit the markdown variables at the top: 
    - Edit the title variable so that it says `TimelineJS` (or anything other than Timeline) 
    - Edit the layout variable so that it reads `full-width-page`
    - Edit the permalink variable so that it reads `timelinejs.html` (or anything other than timeline.html, which is where the other timeline is being created)
        - NOTE: You can make the permalink whatever you'd like and Jekyll will create the page; you can even put it in a new directory (say /timeline/featured.html), just make sure to include the link you create in your config-nav.csv file, as described below
5. Replace the `## Collection Timeline` line with the following "include" command: `{% raw %}{% include feature/timelinejs.html %}{%endraw%}`
6. Save your File
7. Open the config-nav.csv in your /_data/ directory
8. Edit the file so that it includes the following three lines: 

{:.bg-light .pl-4}
```
Timelines,,
Full Timeline,/timeline.html,Timelines
TimelineJS,/timelinejs.html,Timelines
```
- This will create a dropdown menu that links to both timeline pages. 
</div>
</div>
</div>
</div>
<div class="mt-4" markdown="1">
#### Step 2: Curating Your Timeline 

The TimelineJS feature runs off of the timelinejs.json file, which can be found in the /assets/data/ directory. We recommend you edit the file so that it includes a select number of items. Below are several ways to do this. 

**Limiting the Items Included**

1. Open the timelinejs.json file, which can be found in the /assets/data/ directory.
2. You will need to edit the first line of the document so that it limits the collection.
    - limit the timeline to only include those items that are images--> `{% raw %}{%- assign items = site.data[site.metadata] | where_exp: "item","item.format contains 'image'" -%}{% endraw %}`
    - limit the timeline to only include those items that occur during a certain year--> `{% raw %}{%- assign items = site.data[site.metadata] | where_exp: "item","item.date contains '1935'" -%}{% endraw %}` 
3. There are other ways to limit the timeline as well. See below for limiting it through the creation of a curated spreadsheet.

**Creating a New Data Sheet (with new headlines)**

This method will use a new data sheet to create a curated timeline by only listing those items that contain information in a newly created field ("headline")

1. Make a copy of your current metadata file using a spreadsheet software application like Google Sheets
2. Add a column called "headline" right before the "title" column
3. Add new headlines to those items you'd like included on a timeline (or simply copy and paste the current title into the new cell)
4. Save the file as a CSV and rename it "timelinejs.csv" 
5. Add this CSV to your `_data` directory.
6. Open the timelinejs.json file, which can be found in the /assets/data/ directory.
7. Edit the first line so that it reads --> `{% raw %}{%- assign items = site.data.timelinejs | where_exp: "item","item.headline" -%}{% endraw %}`

This will generate a timeline that only includes items that have a headline. 
</div>
