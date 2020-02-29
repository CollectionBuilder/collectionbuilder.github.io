---
title: Deploy
stub: intro
section: deploy
section_order: 0
---
Depending on the type of CollectionBuilder your using, there are two ways to generate the site. **GH** users will just need to turn on the GitHub Pages option via the settings page of their repository on GitHub.com. Directions for doing that are found in the [Deploy the Collection](deploy.html#intro) section **SA** and **SKIN** users will want to use a jekyll command. Both approaches are listed below. 

{:.alert .alert-info}
NOTE: GitHub Pages will not work for **SA** and **SKIN** users, but **GH** users can use their local computer (if they've installed all the software) to serve their files in the same way that **SA** and **SKIN** users can." %}


***So ... Where are the files???!!!***

One of the strange things about developing in this way is that while Jekyll is creating html files like its 1999, knowing where those files are and how to put them somewhere else is difficult to figure out. Let's lift the veil: 

**Jekyll builds the website in a directory called "_site."**

While generating the files for development--so when you are looking at the site after entering `jekyll s` in the commandline, the links it creates are based on that development server. But you'll also need one more command to build the site for production. Typically, that comand is "jekyll build," but we've added a few extra tasks to include analytics in a separate command called `rake deploy`.

1. [Building the Site](#rake-deploy)
2. [Moving the _site Files to Your Web Server](#move-files)