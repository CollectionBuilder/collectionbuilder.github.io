---
title: Build the Site
stub: build
section: deploy
section_order: 2
---

{:.py-4 .mt-4 #build}
***

{% include bootstrap/alert.md color="warning" text="#### **CDM & SA Users**:" %}

### 1. Building the Site 

***So ... Where are the files???!!!***

Jekyll creates html files like it's 1999, but on first using the generator, it's hard to know  where those files actually are and how you might move them to another server. Let's lift the veil: 

**Jekyll builds the website in a directory called "_site"** while generating the files for development and for production. When your generating a test site using `jekyll s` in the commandline, Jekyll builds all the pages with links that are based on that development server, using urls that often start with `http://127.0.0.1:4000/`. 

To build the site for production, you'll need one additional command. Typically, that command is `jekyll build`, but we've added a few extra tasks to include analytics in a separate command called `rake deploy`. Here are the steps to implement it:


#### Build using "`rake deploy`"

When you are ready to build your site, go to the terminal in VS Code and click `CTRL C` to stop your development server. 

Then, type `rake deploy` into the terminal and push 'Enter' on your keyboard. This does two things: 

1. It builds the site with the appropriate (full) links. 
    - (so www.lib.uidaho.edu/digital/boxing/browse.html rather than http://127.0.0.1:4000/digital/boxing/browse.html)
2. It adds Google Analytics code based on the variable you added in the [_config.yml file](config.html#additional). 
    - Waiting until the end to add the analytics prevents false hits on your analytics account.

If you didn't add analytics, that's fine too. `rake deploy` will build your site just the same as `jekyll build` does, so you can use either.

{% include bootstrap/alert.md color="info" text="#### A Note on Google Analytics

We don't necessarily recommend adding Google Analytics to your website. We assume, however, that a large number of our eventual users might use the tool to collect web statistics (we do in many of our sites). 

If you're interested in an analytics tool that doesn't track your users, we've enjoyed looking at [Matomo](https://matomo.org/) recently, and we intend to add more analytics options to CollectionBuilder in the future"  %}