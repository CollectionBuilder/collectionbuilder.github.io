---
title: Move the Files
stub: move
section: deploy
section_order: 3
---

{:.py-4 .mt-4 #move}
***

{% include bootstrap/alert.md color="warning" text="#### **CDM & SA Users**:" %}

### 2. Moving the _site Files to Your Web Server

Once you've completed the build process, the web files you need will all be in your `_site` directory. 

1. Open the `_site` directory using your file explorer or finder.
2. Copy everything you'd like to move into a production site.
3. Paste the copied files and folders into the directory on your web server you'd like to serve this site from. 

*Note: If you'd like to serve this up from a GitHub Pages enabled repository, that is also possible. Talk to us.*

{% include bootstrap/alert.md color="success" text="That's it. You've Done It. And hopefully now you can do it again (and again and again), and after awhile, teach others this development model and/or tool as well. Please let us know if we can help! ([Evan](mailto:ewilliamson@uidaho.edu) has time, I'm sure.)" %}

<!--<div class="alert-warning p-4">
{%capture noteonjekyll %}
#### Note on Jekyll

Jekyll will work its Jekyll/Liquid/Markdown magic on any file in a folder that starts with an underscore ('_') or any file that starts with a YML portion, which starts on the first line with a "---" and ends after the assigned metadata (or no assigned metadata) with another line reading "---"

I'll provide this page's YML as an example:

{:.ml-4}
    `---`
    `title: Deploying the Collection`
    `step: 8`
    `---`

Then everything I'm writing here is below that. 

Jekyll uses that metadata to create the page, or any of the other commands you might need. 
{%endcapture%}
{{noteonjekyll | markdownify}}
</div>-->
