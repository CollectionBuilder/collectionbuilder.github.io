---
title: About CollectionBuilder
layout: page
---

{:.my-4}
CollectionBuilder is a lightweight, flexible tool for creating digital collection websites that are driven by metadata and powered by modern static web technology. 
Using three primary components—a spreadsheet of metadata, a directory of assets, and a configuration file—CollectionBuilder gives information professionals and digital scholarship practitioners agency in building and customizing digital collection websites for free. 

CollectionBuilder is designed and maintained by librarians at the University of Idaho according to the [Lib-STATIC](https://lib-static.github.io/) approach, a methodology committed to leveraging static-web technologies and librarians' specialized skills in metadata and classification to create engaging web publications.

In 2019, CollectionBuilder's development team received an IMLS-sponsored National Leadership Grants for Libraries [Planning Grant](https://www.imls.gov/grants/awarded/lg-34-19-0064-19) to refine and promote CollectionBuilder.

{:.text-center}
**Learn More About:**

{:.text-center}
<a href="#tool" class="btn btn-info mb-3 mx-1">The Tool</a>
<a href="#grant" class="btn btn-info mb-3 mx-1">The Grant</a>
<a href="#people" class="btn btn-info mb-3 mx-1">The People</a>

---
{:#tool}
## The Tool - CollectionBuilder

Over the course of our years designing digital collection interfaces, it has become apparent that the metadata itself is the most important aspect of a digital collection. As such, we (a team of librarians at the University of Idaho) have built a tool that puts the metadata forward, and uses it to build visualizations and browsing features. 

CollectionBuilder uses static web technologies to build digital collection and exhibit pages from metadata. The tool generates item pages and all its visualizations and browsing features from a metadata spreadsheet and config and theme files.

The tool uses 4 main components: 

1. [Jekyll](https://jekyllrb.com/) - a static website builder (i.e. NO SERVERS!!!) that builds websites from data files using the [Liquid](https://shopify.github.io/liquid/basics/introduction/) templating language (which you don't need to know, but which is easily readable and usable) and [Markdown](https://en.wikipedia.org/wiki/Markdown) files for content
2. [Git/GitHub](https://github.com/) - a way to collaborate, track changes, and import pre-built services
3. [Bootstrap 4](https://getbootstrap.com/) - a CSS/Javascript Package for easier development
4. Data Files - We use [Comma Separated Values (CSV) files](https://en.wikipedia.org/wiki/Comma-separated_values) that are just simple version of a spreadsheet and text files written in [YAML (.yml)](https://en.wikipedia.org/wiki/YAML), which are basically lists formatted in a specific fashion.

### Design Concept

{% include bootstrap/image.md class="col-md-8 float-right ml-3 my-2" img="dlf-presentation.jpg"%}

CollectionBuilder builds digital collection sites that encourage investigation and discovery. Our item and visualization pages are built with connections between them so that a user can follow their own interests when exploring a digital collection.

For instance, if you were interested in seeing all the images in our [Barnard Stockbridge Photography Collection](https://www.lib.uidaho.edu/digital/barstock/) pertaining to the 1910 "Big Burn" forest fire, you could [browse the collection](https://www.lib.uidaho.edu/digital/barstock/browse.html#fire) by searching for "fire" on the browse page, then, when looking at individual item pages, you could link out to the year [1910](https://www.lib.uidaho.edu/digital/barstock/timeline.html#1910) on the timeline page and see the wide variety of images collected during that year by the studio. 

And perhaps that would lead you to investigate some other [subject terms](https://www.lib.uidaho.edu/digital/barstock/subjects.html) or to focus on a particular town [via the map](https://www.lib.uidaho.edu/digital/barstock/map.html). The intention is to connect users and to uncover the accretive magic of cultural heritage collections. 

As one examines these collections more closely, we feel that one can get a larger sense of the collection and the era, as well as its connection to one's own area and time frame. 

### Methodology

We call the methodology we use to build CollectionBuilder Lib-STATIC. We've created [a little website to document the ideas that inform this approach](https://lib-static.github.io/). 

Basically, we believe that the systems libraries have been locked into, particularly concerning digital collections, serve neither the librarians/GLAM professionals that maintain them and prepare their content nor the collections we are trying to promote using them. 

CollectionBuilder prioritizes pragmatic, sustainable, and simplified approaches to infrastructure to ensure the tool is 'do-able' and approachable for digital knowledge workers in libraries and museums, empowering them to take control of their web systems.

### How It Works for Us

We use CollectionBuilder to build our digital collections on top of our CONTENTdm instance. To do this, we use the tool together with a Git-Based Workflow. Within our own CollectionBuilder-CONTENTdm repository, there is a "master" branch of CollectionBuilder from which we create specific branches to build our individual collections. The trajectory looks like this: 

1. Create a new branch for a collection from our master CollectionBuilder-contentdm repository
2. Export collection metadata from CONTENTdm as a .tsv file
2. Import the file into a Google Sheet (or other non-excel spreadsheet program)
3. Add a metadata field for "objectid" based on CONTENTdm item number and collection name
4. Save as a CSV file
5. Move the file into the "_data" directory of our branch
6. Adjust the theme and config files
7. Test and view the collection on Jekyll-generated local development server
8. When finished, build the site (using command that also adds analytics scripts)
9. Move the finished files to our web server

To see some of what we've done, go to <https://www.lib.uidaho.edu/digital/>.

Most of our collections have been built using this method in the past six months. 

---
{:#grant}
## The Grant

We are currently being funded by the Institute for Museum and Library Services (IMLS) to build, document, and promote CollectionBuilder. We hope in doing so to lay out a model for building other tools that might eventually replace other systems libraries are locked into (Lib-Guides, anyone?). 

This year's grant will let us fine-tune CollectionBuilder through our own development and through the hiring of a developer. It will also help us to develop the type of promotional materials, documentation, and other products that should help us spread the word about the tool and make it easy to adopt and use. 

The grant also provides funds for us to embed ourselves into several academic libraries and/or similar institutions to set up the technological tools and basic workflows necessary for using the tool to build digital collections more pervasively. 

***Opportunities for Collaboration***

- **Partner!** - If you, or some institution you know, might be interested in adopting this tool more seriously, we can offer a small subaward to supplement the additional work involved and one of us would visit your site to help get everything set up. 
- **Feedback!** - If you have thoughts on the documentation, tool, visualizations, user interactions, or any other features in the tool, please *please* **please** provide us with feedback. Our intention in doing workshops and presentations is to gather feedback on the tool so that when our year is up we have the best, most usable version of CollectionBuilder.
- **Contribute** - If you take to the static web development model and would like to provide contributions of your own to our tool, we would LOVE to work with you and incorporate any contributions you might make. We have a [code of conduct](https://github.com/CollectionBuilder/collectionbuilder.github.io/blob/master/CODE_OF_CONDUCT.md) for contributors.

<div class="row">
<div class="col-md-4" markdown="1">
{:.text-center}
{% include bootstrap/alert.md color="success" text="**Interested in becoming a collaborator?** We'd love to talk to you more about it! **Contact** [Olivia Wikle](mailto:omwikle@uidaho.edu) for more information." %}
</div>
<div class="col-md-8" markdown="1">
{% include bootstrap/card.md text="
- [North Carolina Digital Collections](http://digital.ncdcr.gov/) (State Library of North Carolina and State Archives of North Carolina)
- [New College Digital Collections](http://ncf.sobek.ufl.edu/archives) (New College of Florida)" header="Current CollectionBuilder Partners:" %}
</div>
</div>

Our highest hope for this project is to enable a small army of librarians to develop the type of tools and sites that keep the GLAM professionals in control and not subservient to bloated infrastructures and/or third-party contracts. We hope you will feel drawn to help us build that community. 


---
{:#people}
## People 

- Olivia Wikle, Digital Initiatives Librarian, Communications/Assessment Director for Grant
- Evan Williamson, Digital Infrastructure Librarian, Technical Director
- Devin Becker, Head of Data/Digital Services, Project Director
- Jylisa Doney, Social Sciences Librarian, Documentation Director 
- Chelsea Codling, Graduate Assistant
- Michael Decker, Graduate Assistant
