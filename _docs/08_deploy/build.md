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

Jekyll creates the web like it's 1999, outputting a folder of HTML, CSS, and other static assets as a complete site--but on first using the generator, it's hard to know  where those files actually are and how you might move them to another server. 
Let's lift the veil: 

**Jekyll outputs the complete website in a directory called "_site"** while generating the files for development or for production. 
When you're generating a test site using `jekyll s` on the commandline, Jekyll automatically builds all the pages with links based on the development server, by default using urls that start with `http://127.0.0.1:4000/`. 

To build the site for production, you'll need to `jekyll build` instead. 
In contrast to the development server, `jekyll build` generates the complete site using the real world URLs configured in your [_config.yml](config.html#url).

However, CollectionBuilder only adds some features when the site is built using the Jekyll ["production" environment](https://jekyllrb.com/docs/configuration/environments/){:target="_blank" rel="noopener"} (which is the default when generated on GitHub Pages). 
The environment can be added to the commandline, as `JEKYLL_ENV=production jekyll build`, but to make it easier to use CollectionBuilder provides the `rake deploy` command as an alternative.

#### Build using "rake deploy"

When you are ready to build your site, go to your terminal and click `CTRL C` to stop the development server. 

Then, type `rake deploy` into the terminal and push 'Enter' on your keyboard. 
This does three important things: 

1. It builds the site with the appropriate (full) links. 
    - (so https://www.lib.uidaho.edu/digital/boxing/browse.html rather than http://127.0.0.1:4000/digital/boxing/browse.html)
2. It add rich meta markup for items pages including [Open Graph](https://opengraphprotocol.org/){:target='_blank' rel='noopener'}, [Dublin Core](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/){:target='_blank' rel='noopener'}, and [Schema](https://schema.org/){:target='_blank' rel='noopener'} (as configured in [config-metadata.csv](customize.html#config-metadata)).
3. It adds Google Analytics code *if* you have added a `google-analytics-id` in the [_config.yml file](config.html#additional). 
    - Waiting until final deployment to add the analytics prevents false hits on your analytics account.

{% include bootstrap/alert.md color="info" text="#### A Note on Google Analytics

We don't necessarily recommend adding Google Analytics to your website. We assume, however, that a large number of our eventual users might use the tool to collect web statistics (we do in many of our sites). 

If you're interested in an analytics platform that doesn't sell your users' data, we've enjoyed [Matomo](https://matomo.org/){:target='_blank' rel='noopener'} recently, and we intend to add more analytics options to CollectionBuilder in the future."  %}
