---
title: Deploying the Collection
step: 8
---

***So ... Where are the files???!!!***

One of the strange things about developing in this way is that while Jekyll is creating html files like its 1999, knowing where those files are and how to put them somewhere else is difficult to figure out. Let's lift the veil: 

**Jekyll builds the website in a directory called "_site."**

While generating the files for development--so when you are looking at the site after entering `jekyll s` in the commandline, the links it creates are based on that development server. But you'll also need one more command to build the site for production. Typically, that comand is "jekyll build," but we've added a few extra tasks to include analytics in a separate command called `rake deploy`

### Google Analytics and the 'rake deploy' command



### Moving the _site/ Files to Your Web Server




{:.card alert-secondary #jekyll-note}
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

